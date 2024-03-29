---
title: Определение и управление программой льгот
description: Человеческие ресурсы обеспечивают комплект инструментов, которые можно использовать для того, чтобы настроить и поддержать льготы, вычеты, и планы компенсации работников, которые организация предлагает или обрабатывает для своих работников. Эта статья обеспечивает информацию, как настроить преимущества и управлять ими.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 08b80f4f90ce6b4a286120cd6329a45a4ebd3f71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877811"
---
# <a name="define-and-manage-a-benefits-program"></a>Определение программ льгот и управление ими


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Human Resources обеспечивает комплект инструментов, которые можно использовать для того, чтобы настроить и поддержать льготы, вычеты, и планы компенсации работников, которые организация предлагает или обрабатывает для своих работников. Эта статья обеспечивает информацию, как настроить преимущества и управлять ими.

## <a name="benefit-setup"></a>Настройка льгот

Прежде чем работников можно зарегистрировать в льготах, вы должны создать элементы каждой льготы. Эти элементы совмещают сходные планы льгот и определяют параметры по умолчанию, такие как ставки вычетов и детали учета. Многие из этих установок можно отрегулировать, когда работники позже регистрируются на льготы. Для каждого плана льгот организация может предложить несколько вариантов регистрации, или работник может отказаться от участия в плане. 

[![Поток операций льгот.](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Элементы льготы

Прежде чем вы начинаете создавать льготы и регистрировать работников в них, вы должны определить элементы, которые составляют льготу: тип, план и варианты.

-   **Тип** — коллекция планов для конкретной льготы, например медицинской или парковочной.
-   **План** — конкретная льгота, на которую заключен контракт с поставщиком.
-   **Вариант** — уровень покрытия, например "только сотрудник" или "сотрудник и супруг/партнер".

Для каждого типа льготы, например окулист или стоматолог, организация может предложить одни или несколько планов своим работникам. Для каждого плана организация может предложить различные варианты. Например, работники могут купить дополнительное страховое покрытие жизни в размере одной, двух или трех годовых зарплат. Каждое сочетание из плана и вариантов становится льготой, на которую работники могут зарегистрироваться. 

[![Рис. Льготы.](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Применимость
Много факторов определяют приемлемость работника для различных типов льгот, которые работодатель предлагает. Когда вы создаете льготу в Dynamics 365 Human Resources, вы можете установить тип приемлемости, которая применяется к этой льготе. 

Вы можете сделать льготу доступной всем работникам. Например, некоторые компании предлагают парковочные пропуска всем работникам как дополнительную льготу. Когда вы создаете эту льготу, вы устанавливаете приемлемость как **Имеют право все работники**. 

Для других льгот, например удержание части зарплаты и налоговые сборы, приемлемость не применяется. Когда вы создаете эти типы льгот, вы ставите приемлемость как **Обход процесса допустимости**. 

Наконец, приемлемость льгот может быть основана на правилах. Например, компания предлагает два типа страхования жизни работникам. Руководители могут пользоваться одним планом страхования жизни, тогда как все другие работники на полном рабочем дне могут пользоваться другим планом страхования жизни. В Human Resources вы можете создать правило приемлемости льготы, чтобы найти всех руководителей, и другое правило для того, чтобы найти всех других работников на полном рабочем дне, и после этого применить эти правила к соответствующей льготе.

## <a name="enrollment"></a>Регистрация
После того как вы создавали льготы, которые ваша организация предлагает, и определили приемлемость, вы можете зачислить ваших работников на льготы. Вы можете зачислить одного работника на льготы, или вы можете зачислить много работников на одну или больше льгот за один процесс. 

Иногда, организация прекращает предлагать некоторые преимущества. В этом случае вы должны обновить льготу и работников, которые зарегистрированы. Массовое истечение срока действия льгот позволяет одновременно изменить дату истечения срока как льготы, так и регистраций работников на эту льготу. Можно также выбрать несколько сотрудников, включенных в льготу, и изменить дату окончания их покрытия. 

Подобным образом, массовое продление льготы позволяет вам продлить дату истечения срока как льготы, так и регистрации работника на эту льготу, если вы решаете предложить льготу дольше, чем вы первоначально запланировали.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
