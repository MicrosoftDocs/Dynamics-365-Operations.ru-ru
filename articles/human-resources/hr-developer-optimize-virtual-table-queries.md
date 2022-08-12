---
title: Оптимизация запросов виртуальных таблиц Dataverse
description: Оптимизация и устранение неполадок с производительностью запросов к виртуальной таблице Dataverse
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f379cd7783cc984666582d2c680a1db013627ce
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070183"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Оптимизация запросов виртуальных таблиц Dataverse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Расход

### <a name="overview"></a>Обзор

При использовании виртуальных таблиц Dataverse для разработки интеграций и других подключений к данным с помощью Dynamics 365 Human Resources могут возникнуть проблемы с производительностью запросов к виртуальным таблицам. Медленное выполнение запроса может происходить на различных клиентах или интерфейсах. Например, эта проблема могла возникнуть в следующих обстоятельствах:

- При запросе виртуальной таблицы через веб-API Dataverse
- При создании приложения Power App для виртуальной таблицы
- При создании отчета Power BI по виртуальной таблице

Все эти интерфейсы могут решить проблему производительности.

Одной из причин низкой производительности виртуальных таблиц Dataverse для Human Resources являются столбцы внешнего ключа виртуальной таблицы, связанные с [свойствами навигации](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) таблицы. Когда для виртуальной таблицы создаются свойства навигации, столбец внешнего ключа автоматически добавляется в таблицу для представления значения ключа для соответствующего столбца ключа виртуальной таблицы. Например, столбец **_mshr_fk_person_id_value** добавляется в сущность **mshr_hcmworkerbaseentity** с помощью свойства внешнего ключа из сущности **mshr_dirpersonentity**. В связи с тем, как значения этих столбцов внешнего ключа поддерживаются в таблице, выбор значений может отрицательно повлиять на производительность запроса к виртуальной таблице.

### <a name="potential-symptoms"></a>Возможные симптомы

Например, это воздействие может быть показано в запросах к сущности Работник (**mshr_hcmworkerentity**) или Базовый работник (**mshr_hcmworkerbaseentity**). Проблема с производительностью будет проявляться несколькими различными способами:

- **Медленное выполнение запроса**: запрос к виртуальной таблице возвращает ожидаемые результаты, но занимает больше времени, чем ожидалось, чтобы завершить выполнение запроса.
- **Превышено время ожидания запроса**: возможно превышение времени ожидания запроса и возвращена следующая ошибка: "Получен маркер для вызова финансов и операций, но финансы и операции вернул ошибку типа InternalServerError".
- **Непредвиденная ошибка**: запрос мог бы вернуть тип ошибки 400 со следующим сообщением: "произошла непредвиденная ошибка".

  ![Ошибка типа 400 в HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **Регулирование количества запросов**: запрос может чрезмерно использовать ресурсы сервера и быть подвергнутым регулировке. В этом случае запрос возвращает следующую ошибку: "Получен маркер для вызова финансов и операций, но Финансы и операции вернул ошибку типа 429". Дополнительные сведения о регулировании в Human Resources см. в [Регулирование количества вопросов и ответов. Вопросы и ответы](./hr-admin-integration-throttling-faq.md).

  ![Ошибка типа 429 в HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Решение

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Ограничение числа столбцов, включенных в запрос данных

С помощью виртуальных таблиц одним из методов с наибольшим возможным повышением производительности запросов является ограничение числа столбцов, выбранных в запросе. Общая рекомендация по оптимизации производительности запросов состоит в том, чтобы ограничить столбцы, возвращаемые в запросе, только нужными свойствами. Это особенно актуально для столбцов внешнего ключа в виртуальных таблицах. Если значения в столбцах внешнего ключа для интеграции или отчета не нужны, то необходимо структурировать запрос, чтобы выбрать только нужные столбцы, исключая столбцы внешнего ключа.

#### <a name="selecting-columns-in-an-odata-query"></a>Выбор столбцов в запросе OData

При запросе виртуальной таблицы через веб-API Dataverse можно ограничить число столбцов, включаемых в запрос, используя параметр запроса системы **$select**, а также определить столбцы, для которых необходимо вернуть результаты. Чтобы максимизировать производительность, исключите столбцы внешних ключей (с префиксом **_mshr_FK_**) из запроса.

Например, следующий запрос к сущности **mshr_hcmworkerbaseentity** будет включать только столбцы, включенные в предложение параметра запроса **$select**, исключая значения внешних ключей. Это позволяет значительно повысить производительность запроса, включающего все столбцы таблицы.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Рекомендации по ограничению количества выбранных столбцов также применяются при использовании параметра запроса **$expand**, чтобы расширить запрос на соответствующие виртуальные таблицы с помощью свойств навигации. Например, следующий запрос включает столбцы из сущности **mshr_hcmworkerbaseentity** с развернутыми столбцами из сущности **mshr_dirpersonentity**. Обратите внимание, что параметр запроса **$select** также включается в предложение параметра запроса **$expand**.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

При использовании этого метода получения данных с помощью параметра запроса **$select** в предложении параметра запроса **$expand** обычно улучшается производительность, если свойство навигации между сущностями является отношением "многие к одному". Вы можете не увидеть такого же уменьшения времени выполнения запроса при развертывании отношения "один-ко-многим". Дополнительные сведения об определении отношений для Dataverse виртуальных таблиц см. в [Связи между таблицами](/powerapps/maker/data-platform/create-edit-entity-relationships).

Дополнительные сведения об использовании системных параметров запроса **$select** и **$expand** в веб-API Dataverse см. в [Получение записей связанных сущностей с помощью запроса](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Выбор столбцов в Power BI

Если при создании отчета Power BI по виртуальной таблице Dataverse возникли какие-либо из вышеупомянутых проблем с низкой производительностью, можно повысить производительность, исключив столбцы внешних ключей из столбцов, выбранных из таблицы для отчета. Например, если вы используете Power BI Desktop для создания отчета по сущности **mshr_hcmworkerbaseentity**, можно выполнить следующие действия, чтобы выбрать столбцы, которые необходимо включить в запрос отчета.

1. В Power BI Desktop выберите **Дополнительно...** в раскрывающемся списке **Получение данных** на ленте действий.
2. В окне **Получение данных** введите **Common Data Service** в поле поиска, выберите соединитель **Common Data Service** и нажмите кнопку **подключить**.
3. В поле **URL-адрес сервера** в окне Common Data Service введите URI организации для вашей среды Dataverse и нажмите кнопку **ОК**.
  
   ![Введите URI для вашей среды Dataverse.](./media/PowerBIDataverseURLSetup.png)
  
4. В окне навигатора разверните узел **Сущности**.
5. В поле поиска введите **mshr_hcmworkerbaseentity** и выберите сущность.
6. Выберите **Преобразование данных**.
7. В окне редактора Power Query выберите **Расширенный редактор**.
8. В окне **Расширенный редактор** обновите запрос так, чтобы он выглядел, как показано ниже, добавляя или удаляя любые столбцы массива по мере необходимости.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Обновление запроса в расширенном редакторе для редактора Power Query.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Выберите **Готово**.

   > [!NOTE]
   > Если перед обновлением ранее была получена ошибка типа 429 из запроса, возможно, придется подождать период повтора перед обновлением запроса, чтобы он успешно завершился.

10. Нажмите кнопку **Закрыть и применить** на ленте действий редактора Power Query.

После этого можно приступить к созданию отчета Power BI по столбцам, выбранным из виртуальной таблицы.

#### <a name="selecting-columns-in-power-apps"></a>Выбор столбцов в Power Apps

Аналогично запросам веб-API Dataverse и Power BI, можно повысить производительность запросов для Power Apps на основе виртуальных таблиц Dataverse, исключив из приложения столбцы из соответствующих таблиц. Если какие-либо столбцы из соответствующей таблицы были включены на страницу, то при указании URL-адреса запроса, созданного для получения данных, будут включены свойства внешнего ключа соответствующей таблицы. Это, как и в примерах [Выбор столбцов в запросе OData](#selecting-columns-in-power-apps) выше, снижает производительность, вызывая дополнительные поиски данных.

Чтобы обойти это, можно убедиться, что ни одно поле данных из связанных таблиц не было включено в какую-либо форму данных Power App.

1. В панели древовидного представления выберите форму данных для экрана.
2. В области **Свойства** выберите **Изменить** в свойстве **Поля**.
3. В области **Данные** убедитесь, что ни одно из выбранных полей не является полем виртуальной таблицы источника данных.

Например, если одно из полей данных, включенных в страницу в приложении, ссылается на другую таблицу, например, **ThisItem.Worker.Name**, где **работник** — связанная таблица, возможны проблемы с понижением производительности при получении данных.

Можно использовать [монитор Power Apps](/powerapps/maker/monitor-overview), чтобы убедиться, что в запрос включаются только нужные столбцы для получения данных для Power App. Можно просмотреть URL-адрес, созданный для операции GetRows, чтобы гарантировать, что выбранные для приложения столбцы будут оптимальными для получения данных.

![Используйте монитор Power Apps для анализа операции GetData.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Фильтрация запроса данных

Другим способом повышения производительности выполнения запроса является ограничение числа записей, возвращаемых в результатах запроса. Это можно сделать, отфильтровав результаты, чтобы гарантировать получение только необходимых записей.

См. [Фильтрация результатов](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) для получения дополнительных сведений о фильтрации данных запроса.

### <a name="limiting-the-page-size-of-the-query"></a>Ограничение размера страницы запроса

При работе с большими наборами данных можно разделить результаты запроса на несколько страниц, добавив заголовок предпочтения `odata.maxpagesize` в запросы данных.

Дополнительные сведения о разбиении на страницы см. в [Указание числа возвращаемых сущностей на странице](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>См. также

- [Настройка виртуальных таблиц Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)
- [Вопросы и ответы по виртуальным таблицам Human Resources](hr-admin-virtual-entity-faq.md)
- [Вопросы и ответы по регулированию](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

