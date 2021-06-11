---
title: Оптимизация запросов виртуальных таблиц Dataverse
description: Оптимизация и устранение неполадок с производительностью запросов к виртуальной таблице Dataverse
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054916"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="8c64d-103">Оптимизация запросов виртуальных таблиц Dataverse</span><span class="sxs-lookup"><span data-stu-id="8c64d-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="8c64d-104">Расход</span><span class="sxs-lookup"><span data-stu-id="8c64d-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="8c64d-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="8c64d-105">Overview</span></span>

<span data-ttu-id="8c64d-106">При использовании виртуальных таблиц Dataverse для разработки интеграций и других подключений к данным с помощью Dynamics 365 Human Resources могут возникнуть проблемы с производительностью запросов к виртуальным таблицам.</span><span class="sxs-lookup"><span data-stu-id="8c64d-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="8c64d-107">Медленное выполнение запроса может происходить на различных клиентах или интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="8c64d-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="8c64d-108">Например, эта проблема могла возникнуть в следующих обстоятельствах:</span><span class="sxs-lookup"><span data-stu-id="8c64d-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="8c64d-109">При запросе виртуальной таблицы через веб-API Dataverse</span><span class="sxs-lookup"><span data-stu-id="8c64d-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="8c64d-110">При создании приложения Power App для виртуальной таблицы</span><span class="sxs-lookup"><span data-stu-id="8c64d-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="8c64d-111">При создании отчета Power BI по виртуальной таблице</span><span class="sxs-lookup"><span data-stu-id="8c64d-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="8c64d-112">Все эти интерфейсы могут решить проблему производительности.</span><span class="sxs-lookup"><span data-stu-id="8c64d-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="8c64d-113">Одной из причин низкой производительности виртуальных таблиц Dataverse для Human Resources являются столбцы внешнего ключа виртуальной таблицы, связанные с [свойствами навигации](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) таблицы.</span><span class="sxs-lookup"><span data-stu-id="8c64d-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="8c64d-114">Когда для виртуальной таблицы создаются свойства навигации, столбец внешнего ключа автоматически добавляется в таблицу для представления значения ключа для соответствующего столбца ключа виртуальной таблицы.</span><span class="sxs-lookup"><span data-stu-id="8c64d-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="8c64d-115">Например, столбец **_mshr_fk_person_id_value** добавляется в сущность **mshr_hcmworkerbaseentity** с помощью свойства внешнего ключа из сущности **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="8c64d-116">В связи с тем, как значения этих столбцов внешнего ключа поддерживаются в таблице, выбор значений может отрицательно повлиять на производительность запроса к виртуальной таблице.</span><span class="sxs-lookup"><span data-stu-id="8c64d-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="8c64d-117">Возможные симптомы</span><span class="sxs-lookup"><span data-stu-id="8c64d-117">Potential symptoms</span></span>

<span data-ttu-id="8c64d-118">Например, это воздействие может быть показано в запросах к сущности Работник (**mshr_hcmworkerentity**) или Базовый работник (**mshr_hcmworkerbaseentity**).</span><span class="sxs-lookup"><span data-stu-id="8c64d-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="8c64d-119">Проблема с производительностью будет проявляться несколькими различными способами:</span><span class="sxs-lookup"><span data-stu-id="8c64d-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="8c64d-120">**Медленное выполнение запроса**: запрос к виртуальной таблице возвращает ожидаемые результаты, но занимает больше времени, чем ожидалось, чтобы завершить выполнение запроса.</span><span class="sxs-lookup"><span data-stu-id="8c64d-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="8c64d-121">**Превышено время ожидания запроса**: возможно превышение времени ожидания запроса и возвращена следующая ошибка: "Получен маркер для вызова Finance and Operations, но Finance and Operations вернул ошибку типа InternalServerError".</span><span class="sxs-lookup"><span data-stu-id="8c64d-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="8c64d-122">**Непредвиденная ошибка**: запрос мог бы вернуть тип ошибки 400 со следующим сообщением: "произошла непредвиденная ошибка".</span><span class="sxs-lookup"><span data-stu-id="8c64d-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Ошибка типа 400 в HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="8c64d-124">**Регулирование количества запросов**: запрос может чрезмерно использовать ресурсы сервера и быть подвергнутым регулировке.</span><span class="sxs-lookup"><span data-stu-id="8c64d-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="8c64d-125">В этом случае запрос возвращает следующую ошибку: "Получен маркер для вызова Finance and Operations, но Finance and Operations вернул ошибку типа 429".</span><span class="sxs-lookup"><span data-stu-id="8c64d-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="8c64d-126">Дополнительные сведения о регулировании в Human Resources см. в [Регулирование количества вопросов и ответов. Вопросы и ответы](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="8c64d-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Ошибка типа 429 в HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="8c64d-128">Приказ</span><span class="sxs-lookup"><span data-stu-id="8c64d-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="8c64d-129">Ограничение числа столбцов, включенных в запрос данных</span><span class="sxs-lookup"><span data-stu-id="8c64d-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="8c64d-130">С помощью виртуальных таблиц одним из методов с наибольшим возможным повышением производительности запросов является ограничение числа столбцов, выбранных в запросе.</span><span class="sxs-lookup"><span data-stu-id="8c64d-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="8c64d-131">Общая рекомендация по оптимизации производительности запросов состоит в том, чтобы ограничить столбцы, возвращаемые в запросе, только нужными свойствами.</span><span class="sxs-lookup"><span data-stu-id="8c64d-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="8c64d-132">Это особенно актуально для столбцов внешнего ключа в виртуальных таблицах.</span><span class="sxs-lookup"><span data-stu-id="8c64d-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="8c64d-133">Если значения в столбцах внешнего ключа для интеграции или отчета не нужны, то необходимо структурировать запрос, чтобы выбрать только нужные столбцы, исключая столбцы внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="8c64d-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="8c64d-134">Выбор столбцов в запросе OData</span><span class="sxs-lookup"><span data-stu-id="8c64d-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="8c64d-135">При запросе виртуальной таблицы через веб-API Dataverse можно ограничить число столбцов, включаемых в запрос, используя параметр запроса системы **$select**, а также определить столбцы, для которых необходимо вернуть результаты.</span><span class="sxs-lookup"><span data-stu-id="8c64d-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="8c64d-136">Чтобы максимизировать производительность, исключите столбцы внешних ключей (с префиксом **_mshr_FK_**) из запроса.</span><span class="sxs-lookup"><span data-stu-id="8c64d-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="8c64d-137">Например, следующий запрос к сущности **mshr_hcmworkerbaseentity** будет включать только столбцы, включенные в предложение параметра запроса **$select**, исключая значения внешних ключей.</span><span class="sxs-lookup"><span data-stu-id="8c64d-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="8c64d-138">Это позволяет значительно повысить производительность запроса, включающего все столбцы таблицы.</span><span class="sxs-lookup"><span data-stu-id="8c64d-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="8c64d-139">Рекомендации по ограничению количества выбранных столбцов также применяются при использовании параметра запроса **$expand**, чтобы расширить запрос на соответствующие виртуальные таблицы с помощью свойств навигации.</span><span class="sxs-lookup"><span data-stu-id="8c64d-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="8c64d-140">Например, следующий запрос включает столбцы из сущности **mshr_hcmworkerbaseentity** с развернутыми столбцами из сущности **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="8c64d-141">Обратите внимание, что параметр запроса **$select** также включается в предложение параметра запроса **$expand**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="8c64d-142">При использовании этого метода получения данных с помощью параметра запроса **$select** в предложении параметра запроса **$expand** обычно улучшается производительность, если свойство навигации между сущностями является отношением "многие к одному".</span><span class="sxs-lookup"><span data-stu-id="8c64d-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="8c64d-143">Вы можете не увидеть такого же уменьшения времени выполнения запроса при развертывании отношения "один-ко-многим".</span><span class="sxs-lookup"><span data-stu-id="8c64d-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="8c64d-144">Дополнительные сведения об определении отношений для Dataverse виртуальных таблиц см. в [Связи между таблицами](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="8c64d-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="8c64d-145">Дополнительные сведения об использовании системных параметров запроса **$select** и **$expand** в веб-API Dataverse см. в [Получение записей связанных сущностей с помощью запроса](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="8c64d-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="8c64d-146">Выбор столбцов в Power BI</span><span class="sxs-lookup"><span data-stu-id="8c64d-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="8c64d-147">Если при создании отчета Power BI по виртуальной таблице Dataverse возникли какие-либо из вышеупомянутых проблем с низкой производительностью, можно повысить производительность, исключив столбцы внешних ключей из столбцов, выбранных из таблицы для отчета.</span><span class="sxs-lookup"><span data-stu-id="8c64d-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="8c64d-148">Например, если вы используете Power BI Desktop для создания отчета по сущности **mshr_hcmworkerbaseentity**, можно выполнить следующие действия, чтобы выбрать столбцы, которые необходимо включить в запрос отчета.</span><span class="sxs-lookup"><span data-stu-id="8c64d-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="8c64d-149">В Power BI Desktop выберите **Дополнительно...** в раскрывающемся списке **Получение данных** на ленте действий.</span><span class="sxs-lookup"><span data-stu-id="8c64d-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="8c64d-150">В окне **Получение данных** введите **Common Data Service** в поле поиска, выберите соединитель **Common Data Service** и нажмите кнопку **подключить**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="8c64d-151">В поле **URL-адрес сервера** в окне Common Data Service введите URI организации для вашей среды Dataverse и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Введите URI для вашей среды Dataverse](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="8c64d-153">В окне навигатора разверните узел **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="8c64d-154">В поле поиска введите **mshr_hcmworkerbaseentity** и выберите сущность.</span><span class="sxs-lookup"><span data-stu-id="8c64d-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="8c64d-155">Выберите **Преобразование данных**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="8c64d-156">В окне Редактор Power Query выберите **Расширенный редактор**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="8c64d-157">В окне **Расширенный редактор** обновите запрос так, чтобы он выглядел, как показано ниже, добавляя или удаляя любые столбцы массива по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8c64d-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Обновление запроса в расширенном редакторе для редактора Power Query](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="8c64d-159">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="8c64d-160">Если перед обновлением ранее была получена ошибка типа 429 из запроса, возможно, придется подождать период повтора перед обновлением запроса, чтобы он успешно завершился.</span><span class="sxs-lookup"><span data-stu-id="8c64d-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="8c64d-161">Нажмите кнопку **Закрыть и применить** на ленте действий редактора Power Query.</span><span class="sxs-lookup"><span data-stu-id="8c64d-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="8c64d-162">После этого можно приступить к созданию отчета Power BI по столбцам, выбранным из виртуальной таблицы.</span><span class="sxs-lookup"><span data-stu-id="8c64d-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="8c64d-163">Выбор столбцов в Power Apps</span><span class="sxs-lookup"><span data-stu-id="8c64d-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="8c64d-164">Аналогично запросам веб-API Dataverse и Power BI, можно повысить производительность запросов для Power Apps на основе виртуальных таблиц Dataverse, исключив из приложения столбцы из соответствующих таблиц.</span><span class="sxs-lookup"><span data-stu-id="8c64d-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="8c64d-165">Если какие-либо столбцы из соответствующей таблицы были включены на страницу, то при указании URL-адреса запроса, созданного для получения данных, будут включены свойства внешнего ключа соответствующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="8c64d-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="8c64d-166">Это, как и в примерах [Выбор столбцов в запросе OData](#selecting-columns-in-power-apps) выше, снижает производительность, вызывая дополнительные поиски данных.</span><span class="sxs-lookup"><span data-stu-id="8c64d-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="8c64d-167">Чтобы обойти это, можно убедиться, что ни одно поле данных из связанных таблиц не было включено в какую-либо форму данных Power App.</span><span class="sxs-lookup"><span data-stu-id="8c64d-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="8c64d-168">В панели древовидного представления выберите форму данных для экрана.</span><span class="sxs-lookup"><span data-stu-id="8c64d-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="8c64d-169">В области **Свойства** выберите **Изменить** в свойстве **Поля**.</span><span class="sxs-lookup"><span data-stu-id="8c64d-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="8c64d-170">В области **Данные** убедитесь, что ни одно из выбранных полей не является полем виртуальной таблицы источника данных.</span><span class="sxs-lookup"><span data-stu-id="8c64d-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="8c64d-171">Например, если одно из полей данных, включенных в страницу в приложении, ссылается на другую таблицу, например, **ThisItem.Worker.Name**, где **работник** — связанная таблица, возможны проблемы с понижением производительности при получении данных.</span><span class="sxs-lookup"><span data-stu-id="8c64d-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="8c64d-172">Можно использовать [монитор Power Apps](/powerapps/maker/monitor-overview), чтобы убедиться, что в запрос включаются только нужные столбцы для получения данных для Power App.</span><span class="sxs-lookup"><span data-stu-id="8c64d-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="8c64d-173">Можно просмотреть URL-адрес, созданный для операции GetRows, чтобы гарантировать, что выбранные для приложения столбцы будут оптимальными для получения данных.</span><span class="sxs-lookup"><span data-stu-id="8c64d-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Используйте монитор Power Apps для анализа операции GetData](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="8c64d-175">Фильтрация запроса данных</span><span class="sxs-lookup"><span data-stu-id="8c64d-175">Filtering the data query</span></span>

<span data-ttu-id="8c64d-176">Другим способом повышения производительности выполнения запроса является ограничение числа записей, возвращаемых в результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="8c64d-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="8c64d-177">Это можно сделать, отфильтровав результаты, чтобы гарантировать получение только необходимых записей.</span><span class="sxs-lookup"><span data-stu-id="8c64d-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="8c64d-178">См. [Фильтрация результатов](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) для получения дополнительных сведений о фильтрации данных запроса.</span><span class="sxs-lookup"><span data-stu-id="8c64d-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="8c64d-179">Ограничение размера страницы запроса</span><span class="sxs-lookup"><span data-stu-id="8c64d-179">Limiting the page size of the query</span></span>

<span data-ttu-id="8c64d-180">При работе с большими наборами данных можно разделить результаты запроса на несколько страниц, добавив заголовок предпочтения `odata.maxpagesize` в запросы данных.</span><span class="sxs-lookup"><span data-stu-id="8c64d-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="8c64d-181">Дополнительные сведения о разбиении на страницы см. в [Указание числа возвращаемых сущностей на странице](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="8c64d-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c64d-182">См. также</span><span class="sxs-lookup"><span data-stu-id="8c64d-182">See also</span></span>

- [<span data-ttu-id="8c64d-183">Настройка виртуальных таблиц Dataverse</span><span class="sxs-lookup"><span data-stu-id="8c64d-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="8c64d-184">Вопросы и ответы по виртуальным таблицам Human Resources</span><span class="sxs-lookup"><span data-stu-id="8c64d-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="8c64d-185">Вопросы и ответы по регулированию</span><span class="sxs-lookup"><span data-stu-id="8c64d-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]