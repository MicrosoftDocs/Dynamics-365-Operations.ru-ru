---
title: Работа с датой и временем в Microsoft Dynamics 365 Talent
description: Узнайте, что следует ожидать при использовании полей даты и времени в Microsoft Dynamics 365 Talent. Узнайте, что следует ожидать при взаимодействии с данными даты и времени в форме в Talent, во внешнем источнике или в Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: abd215243cbda68ba3f57b5fa41054a10745d11f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551034"
---
# <a name="work-with-date-and-time-in-microsoft-dynamics-365-talent"></a>Работа с датой и временем в Microsoft Dynamics 365 Talent

[!include [banner](includes/banner.md)]

Поля **Дата и время** являются фундаментальным понятием в Dynamics 365 Talent. Важно понимать, как работать с данными **Дата и время** в форме Dynamics 365, Common Data Service и во внешних источниках.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Общее представление о разнице между типами данных полей "Дата" и "Дата и время"

Поля **Дата и время** содержатся сведения о часовом поясе, а поля **Дата** — не содержат. В полях **Дата** отображается одна и та же информация в любом местонахождении. При вводе даты в поле **Дата** Talent записывают эту же дату в базу данных.

При отображении данных в поле **Дата и время** Talent корректирует дату и время на основе часового пояса, заданного в форме **Параметры пользователя** (**Общие > Настройка > Параметры пользователя**). Сведения о дате и времени, вводимые в поле, могут не совпадать со сведениями, записанными в базу данных.

[![Форма "Параметры пользователя"](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Общие сведения о полях даты и времени в формах 

При вводе данных в поле **Дата и время** отображаемые на экране данные не будут совпадать с данными, хранящимися в базе данных, если часовой пояс пользователя не установлен в значение времени в формате UTC. Данные в полях **Дата и время** всегда хранятся в формате UTC.

[![Форма работника](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Общие сведения о полях даты и времени в базе данных 

Когда Talent записывает значение **Дата и время** в базу данных, он сохраняет данные в формате UTC. Это позволяет пользователям просматривать любые данные **Дата и время** относительно часового пояса, определенного в параметрах пользователя.
 
В приведенном выше примере время начала — это момент времени, а не конкретная дата. При изменении часового пояса зарегистрированного пользователя с GMT +12:00 на GMT UTC та же самая созданная запись отображает 30.04.2019 12:00:00 вместо 01.05.2019 12:00:00.
  
В приведенном ниже примере занятость сотрудника 000724 становится активной в то же время, независимо от часового пояса. Сотрудник будет активным 30.04.2019 в часовом поясе GMT, что совпадает с 01.05.2019 в часовом поясе GMT+12:00. Они ссылаются на один и тот же момент времени, а не на конкретную дату. 

[![Форма работника](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Данные даты и времени в платформе управления данными, Excel, Common Data Service и Power BI 

Отчеты платформы управления данными, надстройки Excel, Common Data Service и Power BI все предназначены для непосредственного взаимодействия с данными на уровне базы данных. Так как нет клиента для корректировки данных **Дата и время** в соответствии с часовым поясом пользователя, все значения **Дата и время** заданы в формате UTC, что может привести к некоторым неправильным допущениям при вводе или просмотре данных.  
 
База данных предполагают, что данные **Дата и время**, которые передаются через DMF, Excel или Common Data Service, введены в формате UTC. Это может привести к путанице, когда введенное значение **Дата и время** не отображается ожидаемым образом, поскольку у пользователя, просматривающего данные, не задан часовой пояс UTC. 
 
То же самое происходит в обратную сторону при экспорте данных. Данные **Дата и время** в экспортированном объекте DMF могут отличаться при отображении в клиенте Dynamics. 
 
При использовании внешних источников, таких как DMF, для просмотра или разработки данных, важно помнить, что значения **Дата и время** по умолчанию учитываются в формате UTC, независимо от часового пояса компьютера пользователя или настроек часового пояса текущего пользователя. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Примеры одной и той же записи, отображаемой в разных областях продукта 

**Talent, когда установлен часовой пояс пользователя UTC**

[![Форма работника](./media/worker-form3.png)](./media/worker-form3.png)

**Talent, когда установлен часовой пояс пользователя GMT +12:00** 

[![Форма работника](./media/worker-form4.png)](./media/worker-form4.png)

**Excel через OData**

[![Excel через OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**Промежуточное хранение DMF**

[![Промежуточное хранение DMF](./media/DMFStaging.png)](./media/DMFStaging.png)

**Экспорт DMF**

[![Промежуточное хранение DMF](./media/DMFexport.png)](./media/DMFexport.png)

**Excel через Common Data Service**

[![Excel через Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)

### <a name="see-also"></a>См. также

[Данные "Дата и время"](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Предпочтительные часовые пояса пользователя](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
