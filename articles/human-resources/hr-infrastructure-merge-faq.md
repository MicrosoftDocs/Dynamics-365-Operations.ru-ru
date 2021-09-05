---
title: Вопросы и ответы по объединению инфраструктуры Dynamics 365 Human Resources
description: В этой теме содержатся ответы на часто задаваемые вопросы о слиянии инфраструктуры для приложений Microsoft Dynamics 365 Human Resources и Finance and Operations.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ae2896eda98a8f9545d465e941d5b50065ae94b
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386547"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Вопросы и ответы по объединению инфраструктуры Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме содержатся ответы на часто задаваемые вопросы о слиянии инфраструктуры для приложений Microsoft Dynamics 365 Human Resources и Finance and Operations.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Что такое объединение инфраструктуры Dynamics 365 Human Resources?

Dynamics 365 Human Resources — это отдельное приложение, использующее инфраструктуру, отличную от других приложений Finance and Operations, таких как Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce и Dynamics 365 Project Operations. Слияние инфраструктуры перенесет Dynamics 365 Human Resources в ту же инфраструктуру, что и другие приложения Finance and Operations.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Ценность и преимущества объединения инфраструктуры

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Моя организация использует Dynamics 365 Human Resources для управления операциями с персоналом. Какие преимущества мы получим от этих изменений?

- Эти изменения устраняют путаницу, вызванную несколькими наборами возможностей управления персоналом (HR) в Dynamics 365.
- Они обеспечивают расширяемость Microsoft Power Platform и способ расширения бизнес-логики и параметров функций.
- Они обеспечивают согласованность между Dynamics 365 Human Resources и другими приложениями Finance and Operations в плане управления жизненным циклом приложений (ALM), Microsoft Dynamics Lifecycle Services (LCS), географической доступности, расширяемости и т. д.
- Они позволяют использовать преимущества общих служб и инструментов и помогают сократить затраты.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Моя организация использует модуль Human Resources в Dynamics 365 Finance, Supply Chain Management, Commerce или Project Operations. Какие преимущества мы получим от этих изменений?

Возможности и инвестиции, которые были сделаны в Dynamics 365 Human Resources, становятся доступными для клиентов, использующих модуль HR в Dynamics 365 Finance. Некоторые из этих возможностей включают управление отпусками и отсутствием, управление льготами и управление задачами.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Будут ли утрачены какие-либо функции и возможности, которые в настоящее время используются?

Между Dynamics 365 Human Resources и модулем HR в приложениях Finance and Operations существует функциональное равенство. Dynamics 365 Human Resources будет имеет приоритет для аналогичных функций. Дополнительные сведения см. в разделе [Обзор управления функциями](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Изменится ли опыт для моих пользователей?

Новые возможности работы с персоналом будут управляться с помощью управления функциями. Клиенты будут решать, хотят ли они их получать. В некоторых случаях возможности могут быть изменены. В этих случаях будет представлена документация.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Каким образом это изменение повлияет на меня, если я существующий клиент, и я использую как модуль HR в инфраструктуре Finance and Operations, и Dynamics 365 Human Resources при помощи пользовательской интеграции?

Пользовательские интеграции между Dynamics 365 Human Resources и модулем HR в Dynamics 365 Finance больше не потребуются. Все данные о персонале будут находиться в той же базе данных, что и другие приложения Finance and Operations.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Миграция из Dynamics 365 Human Resources в приложения Finance and Operations

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Моя организация использует Dynamics 365 Human Resources для управления операциями с персоналом. Что необходимо запланировать для миграции на новый опыт?

Если ваша организация использует Dynamics 365 Human Resources, но не использует никакие другие приложения Finance and Operations, ваша среда Human Resources будет перенесена в новую инфраструктуру. Большая часть процесса миграции будет автоматизирована. Процессы будут использоваться для переноса вашей базы данных и синхронизации их с новой инфраструктурой.

Кроме того, будет использовано средство, позволяющее тестировать процесс миграции и проверять данные и опыт перед миграцией производственной среды.

Если в организации используются как Dynamics 365 Human Resources, так и приложения Finance and Operations, следует спланировать дополнительное время для проверки правильности переноса данных в новую среду. Миграция в новую инфраструктуру приведет к объединению данных из вашей среды Human Resources с вашей средой Finance and Operations. Конфликтующие данные требуют ввода данных пользователем, чтобы определить, как конфликт следует разрешить. Пользователям и администраторам придется управлять сопоставлениями данных там, где имеются конфликты, и тестировать миграцию в изолированных средах перед миграцией рабочих сред.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Моя организация использует модуль Human Resources в Dynamics 365 Finance, Supply Chain Management, Commerce или Project Operations. Что необходимо запланировать для миграции на новый опыт?

Для организаций, использующих модуль HR в приложениях Finance and Operations, новая функциональность функций из Dynamics 365 Human Resources будет применена к среде посредством стандартного процесса обновления одной версии. Можно ожидать, что в среде будут отображаться новые функции, которые становятся доступными в каждом обновлении. Можно использовать управление функциями для включения новых функций, однако следует предусмотреть их проверку. Выполните предусмотренные процессы для проверки других обновлений среды. Дополнительные сведения о том, как обновления применяются к приложениям Finance and Operations, см. в [обзоре одной версии](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Когда будет выполнена миграция моей организации?

Миграция для каждой организации будет зависеть от текущей конфигурации и готовности к миграции в новую инфраструктуру. Эти даты могут быть изменены.

- Организации, которые используют модуль HR в приложениях Finance and Operations, получат функциональность управления персоналом для Dynamics 365 Human Resources в составе регулярного обновления одной версии. Новые возможности планируются для общей доступности начиная с января 2022 года.
- Организации, которые используют только Dynamics 365 Human Resources, будут иметь доступ к средствам миграции, чтобы они могли начать тестирование и начать миграцию начиная с середины 2022 года. Дата, на которую миграция в новую инфраструктуру должна быть завершена, еще не была определена. Однако это будет по крайней мере на один год позже даты, когда станет доступно средство миграции.
- Организации, которые используют и Dynamics 365 Human Resources, и другие приложения Finance and Operations, будут иметь доступ к средствам миграции, чтобы они могли начать тестирование и начать миграцию начиная с конца 2022 года. Дата, на которую миграция в новую инфраструктуру должна быть завершена, еще не была определена. Однако это будет по крайней мере на один год позже даты, когда станет доступно средство миграции.

Дополнительные сведения о новых возможностях для Dynamics 365 Human Resources см. в разделе [Что нового и что изменилось в Human Resources](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Моя организация еще не использовала Dynamics 365 Human Resources. Следует ли нам перейти на модуль Human Resources в приложениях Finance and Operations или приложение Dynamics 365 Human Resources в устаревшей инфраструктуре?

Важно учесть, для чего требуются функции HR и когда эти функции появятся в новой инфраструктуре. Если организация нуждается в основных функциях управления персоналом, которые в настоящее время доступны в модуле HR в приложениях Finance and Operations в новой инфраструктуре. Равенство функций между модулем HR приложений Finance and Operations и приложения Dynamics 365 Human Resources ожидается в выпуске 10.0.25, который запланирован на март 2022. Функции интеграции, такие как приложения Teams и интеграции сущностей Dataverse, будут доступны в последующих выпусках.

Если потребности организации в функциях HR будут доступны в новой инфраструктуре в течение времени, когда организация приступит к работе, может быть проще перейти на модуль Human Resources в приложениях Finance and Operations. Это приведет к более удобной миграции, поскольку это стандартное обновление приложения для приложения Dynamics 365 Human Resources, и клиент будет уже в новой инфраструктуре. Если организация решила приступить к работе с приложением Dynamics 365 Human Resources в существующей инфраструктуре, то для перехода к новой инфраструктуре потребуется выполнить миграцию среды. Этого можно избежать, если перейти на новую инфраструктуру.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Я использую новые возможности, доступные только в Dynamics 365 Human Resources (такие как **Отпуска и отсутствие** и **Управление льготами**). Будут ли эти возможности немедленно доступны в модуле Human Resources в инфраструктуре Finance and Operations также?

Да, все модули Dynamics 365 Human Resources будут работать как есть в приложениях Finance and Operations, и будет 100% равенство функций. В рамках общей стратегии миграции для клиентов, которые в настоящее время используют эти возможности в HR, данные клиентов будут перенесены таким образом, чтобы они продолжали работать в инфраструктуре Finance and Operations.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Я использую новые возможности управления льготами Dynamics 365 Human Resources. Я создал настраиваемые интеграции с модулем HR в инфраструктуре Finance and Operations, чтобы можно было использовать преимущества возможностей модуля зарплаты, используя данные по льготам. Будут ли эти пользовательские интеграции необходимы для продолжения работы?

В ходе объединения инфраструктуры данные HR переводятся в ту же базу данных, что и другие приложения Finance and Operations. Интеграция между модулями в приложениях Finance and Operations больше не потребуется.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Моя организация использует одно или несколько решений независимых поставщиков программного обеспечения с Dynamics 365 Human Resources. Будут ли автоматически перенесены наши решения независимых поставщиков программного обеспечения?

Процесс миграции для каждого решения независимых поставщиков программного обеспечения (ISV) может различаться в зависимости от способа интеграции решения. Для обеспечения плавного перехода к новой инфраструктуре корпорация Майкрософт тесно взаимодействует с независимыми поставщиками программного обеспечения.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Моя организация использует интеграцию LinkedIn Talent Hub с Dynamics 365 Human Resources. Будет ли эта интеграция продолжать работать после изменения инфраструктуры?

Нет, интеграция LinkedIn Talent Hub не будет работать после миграции в новую инфраструктуру. Служба для интеграции с LinkedIn Talent Hub будет отменена для устаревшей инфраструктуры Dynamics 365 Human Resources.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Моя организация использует приложение Human Resources для Teams. Будет ли это приложение продолжать работать после изменения инфраструктуры?

Да, приложение Human Resources для Teams будет продолжать работать после миграции в новую инфраструктуру.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>В организации настроена пользовательская безопасность в Dynamics 365 Human Resources. Будет ли пользовательская безопасность применяться после завершения изменения инфраструктуры?

Да, пользовательские конфигурации безопасности будут включены в миграцию данных в новую инфраструктуру.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Мы используем интегратор данных для перемещения данных между приложениями Dynamics 365 Human Resources и Finance and Operations. Как будут затронуты данные, интеграция которых в данный момент выполняется?

Данные HR, которые в данный момент в Dynamics 365 Human Resources, синхронизируются с Dataverse. Затем интегратор данных может использоваться для односторонней синхронизации с приложениями Finance and Operations. После миграции в новую инфраструктуру данные HR будут собственными для приложений Finance and Operations. Интегратору данных больше не потребуется синхронизировать данные между приложениями Finance and Operations и Human Resources.

Текущие собственные таблицы данных Dataverse для модуля Human Resources продолжат синхронизировать данные из среды в новой инфраструктуре. Объекты будут преобразованы для поддержки двойной записи. Любые другие интеграции данных, настроенные через интегратор данных по этим таблицам для других приложений Dynamics 365, продолжат работать в том виде, в котором они настроены.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Для перемещения данных HR между Dataverse и другими приложениями Finance and Operations используется двойная запись. Как повлияет перенос в новую инфраструктуру на данные, которые в настоящее время интегрируются?

Данные HR будут собственными для приложений Finance and Operations в среде в новой инфраструктуре. Будет использоваться двойная запись для перемещения данных HR между новой средой и средой Dataverse.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Мы создали настраиваемую интеграцию из Dynamics 365 Human Resources в одну или несколько внешних систем. Придется ли разрабатывать новые интеграции после завершения изменения инфраструктуры?

Это зависит от конечной точки интеграции. Дополнительные сведения о технологиях интеграции, доступных в приложениях Finance and Operations, и о выборе наилучшей технологии интеграции см. в разделе [Обзор интеграции](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Мы расширили Dataverse для Dynamics 365 Human Resources. Будут ли эти расширения автоматически перенесены?

Если среды Dynamics 365 Human Resources и Finance and Operations, которые будут объединены в среде новой инфраструктуры, подключены к одной и той же среде Dataverse, два приложения будут по-прежнему подключены к одной среде Dataverse после миграции. Для любых расширений Dataverse миграция не требуется.

Однако если среды Dynamics 365 Human Resources и Finance and Operations в настоящее время подключена к отдельным средам Dataverse, то эти две среды Dataverse необходимо будет объединить, чтобы они были подключены к одной среде в новой инфраструктуре. Для этой миграции Dataverse таблицы Dataverse, которые являются стандартными для решений Human Resources, могут быть подключены к и повторно синхронизированы с новой средой Dataverse. Любые расширения среды Dataverse не будут перенесены автоматически, но должны быть заново развернуты в новой среде. Для управления расширениями Dataverse рекомендуется использовать управляемые решения. Дополнительные сведения см. в разделе [Введение в решения](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Мы настроили потоки Microsoft Power Automate и/или Microsoft Power Apps для работы с Dynamics 365 Human Resources. Будут ли эти компоненты Microsoft Power Platform перенесены и начнут работать автоматически после завершения изменения инфраструктуры?

Потоки Power Apps, Power Automate и другие настройки Microsoft Power Platform похожи на расширения Dataverse. Будут ли они автоматически работать после миграции в новую инфраструктуру, зависит от того, были ли приложение Human Resources и приложения Finance and Operations подключены к одной и той же среде Power Apps до миграции.

Если приложения в настоящее время подключены к одной и той же среде Power Apps, они будут по-прежнему подключены к этой среде Power Apps после миграции в новую инфраструктуру. В этом случае Power Apps, потоки Power Automate и другие настройки Microsoft Power Platform будут продолжать работать без дополнительной настройки. Для управления расширениями приложений в Dataverse рекомендуется использовать управляемые решения. Дополнительные сведения см. в разделе [Введение в решения](/powerapps/developer/data-platform/introduction-solutions).

Однако если приложение Human Resources и приложения Finance and Operations подключены к разным средам Power Apps, они должны быть объединены в рамках миграции. Для этой задачи потребуется повторно развернуть все Power Apps и другие настройки в новой среде.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Мы включили виртуальные таблицы Dataverse для Dynamics 365 Human Resources. Что произойдет с этими таблицами во время миграции?

После миграции, если среда новой инфраструктуры остается подключенной к среде Dataverse, которая в данный момент подключена к Dynamics 365 Human Resources, виртуальные таблицы Dataverse, созданные в этой среде, будут продолжать работать без дополнительной настройки.

Однако, если среда новой инфраструктуры подключена к другой среде Dataverse после миграции, виртуальные таблицы должны быть повторно созданы в новой среде Dataverse.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Мы разработали интеграцию с помощью интерфейса API системы отслеживания кандидатов (АТС), API зарплаты, виртуальных таблиц Dataverse для Dynamics 365 Human Resources или других объектов в веб-API Dataverse. Будут ли эти интеграции продолжать работать после изменения инфраструктуры?

После миграции, если среда в новой инфраструктуре остается подключенной к среде Dataverse, которая в данный момент подключена к Dynamics 365 Human Resources, любые интеграции, разработанные для веб-API Dataverse, будут продолжать работать после завершения миграции.

Однако если среда в новой инфраструктуре подключена к другой среде Dataverse после миграции, любые интеграции, разработанные для веб-API Dataverse, будет необходимо заново настроить, чтобы они подключались к новой среде Dataverse.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Если ли влияние на область Azure при миграции среды?

Предполагается, что ваша среда Human Resources обычно остается в той же области Azure во время миграции. Единственное исключение происходит, если среда Human Resources будет объединена со средой Finance and Operations, которая находится в другом регионе. В этом случае среда Human Resources будет перенесена в область Azure среды Finance and Operations.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Моя организация зависит от рабочих процессов в Dynamics 365 Human Resources для одного или нескольких бизнес-процессов. Будут ли эти рабочие потоки автоматически перенесены?

Да, конфигурации рабочих потоков, журнал рабочих процессов и текущие внутрипроцессные рабочие процессы будут перенесены.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Какое обучение и ресурсы будут доступны для помощи в процессе миграции?

Для подробного описания каждого шага процесса миграции будет предоставлена полная документация. В зависимости от потребностей могут также быть доступны дополнительные ресурсы, такие как видео и семинары.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Моя организация создала сохраненные представления в Dynamics 365 Human Resources, чтобы улучшить удобство использования интерфейса. Будут ли эти сохраненные представления автоматически перенесены?

Да, сохраненные представления будут перенесены в новую инфраструктуру.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Мы используем Ceridian с Dynamics 365 Human Resources. Будут ли интеграция Ceridian доступна после завершения изменения инфраструктуры? 

Интеграция с Ceridian будет перенесена в интеграцию на основе API зарплаты. Интеграция на основе файлов, которая в настоящее время существует в Dynamics 365 Human Resources, не будет перенесена в инфраструктуру Finance and Operations. Дополнительные сведения см. в разделе [Введение в API зарплаты](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Каким образом миграция влияет на процесс обновления служб?

После миграции клиенты будут иметь намного большую гибкость в плане ALM и обновлений служб. Обновления служб больше не будут применяться автоматически в средах Human Resources. Вместо этого служба будет следовать процессами и функциональным возможностям обновления службы одной версии. Таким образом, параметры конфигурации для обновлений будут доступны через LCS. Дополнительные сведения см. в разделе [Обзор одной версии](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Как повлияет миграция на мой проект LCS для Dynamics 365 Human Resources?

Миграция в новую инфраструктуру переместит управление средами Dynamics 365 Human Resources в проект реализации Finance and Operations в LCS. Если миграция выполняет слияние Dynamics 365 Human Resources с существующей средой Finance and Operations, проект LCS для Human Resources будет объединен в проект реализации LCS для приложения Finance and Operations. Если в настоящее время используется только Dynamics 365 Human Resources, будет создан новый проект внедрения LCS, а существующий проект LCS Human Resources будет перенесен в этот новый проект.

Новый проект будет иметь тот же тип проекта, который используется приложениями Finance and Operations. Он будет иметь те же функции и функциональные возможности для управления средами. Дополнительные сведения см. в разделе [Ресурсы Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Мы связали наши записи задач со средством моделирования бизнес-процессов в Human Resources. Как будет выполняться миграция и слияние средства моделирования бизнес-процессов в LCS?

Библиотеки бизнес-процессов для проекта LCS будут перенесены в новый проект LCS для Human Resources.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Моя организация в настоящее время использует только Dynamics 365 Human Resources. Какие ресурсы доступны для получения дополнительных сведений о возможностях разработки после завершения изменения инфраструктуры?

Параметры расширяемости Microsoft Power Platform и параметры расширяемости Finance and Operations будут доступны и могут использоваться для разработки. Дополнительные сведения см. в разделе [Домашняя страница модуля разработки и настройки](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Мы включили функции в Dynamics 365 Human Resources. Будут ли эти функции автоматически включены в ходе миграции?

Будет ли функция автоматически включаться в новой инфраструктуре, будет определяться отдельно для каждой функции. Эта информация будет включена в документацию по функции.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Что происходит с моей базой данных BYOD во время миграции?

Импорт и экспорт конфигураций для вашей собственной базы данных (BYOD) будут перенесены в новую инфраструктуру.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Что происходит с моим Azure Data Lake во время миграции?

Все экспорты, в настоящее время настроенные для Azure Data Lake Storage в приложениях Finance and Operations, будут сохранять ту же конфигурацию после миграции.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>В настоящее время мы используем Dynamics AX 2012. Будут ли доступные в данный момент инструменты обновления использоваться для обновления модуля HR в AX 2012 до Dynamics 365 Human Resources?

Да. Dynamics 365 Human Resources будет включено в объединенную базу кода и инфраструктуру для приложений Finance and Operations. Обновление с Dynamics AX 2012 до Dynamics 365 Human Resources будет использовать тот же самый путь обновления и инструментарий, которые используются для обновления до последней версии приложений Finance and Operations.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Мы используем обработку документов с Dynamics 365 Human Resources. Что произойдет с этими документами во время миграции?

Эти документы останутся в существующем хранилище документов. Они будут повторно сопоставлены новой среде в новой инфраструктуре.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Что происходит с пакетными заданиями, которые были настроены в Dynamics 365 Human Resources, после миграции?

Применимые пакетные задания будут автоматически перенесены в новую инфраструктуру.

## <a name="licensing-impact"></a>Влияние на лицензирование

Эта документация не заменяет и не замещает любую юридическую документацию, которая охватывает права использования.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Моя организация использует Dynamics 365 Human Resources для управления операциями с персоналом. Изменится ли наше лицензирование или расходы?

Клиенты, которые приобрели лицензии Dynamics 365 Human Resources, не будут затронуты. Для этих клиентов отсутствует миграция лицензирования. Дополнительный единица складского учета (SKU) песочницы, специфичная для Human Resources, больше не будет применяться. Вместо этого клиенты могут выбирать, покупать ли песочницу уровня 2 для приложений Finance and Operations по немного более низкой цене. Существующие клиенты, которые приобрели песочницу Human Resources, будут перенесены в песочницу уровня 2 приложений Finance and Operations без дополнительных затрат.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Моя организация использует модуль Human Resources в Dynamics 365 Finance, Supply Chain Management, Commerce или Project Operations. Изменится ли мое лицензирование или расходы?

Существующие пользователи приложений Dynamics 365 и пользователи отдельных приложений Dynamics 365 Finance, Supply Chain Management, Commerce и Project Operations могут получить доступ к Human Resources как часть этих лицензий до февраля 2025 года или до окончания текущего лицензионного соглашения, в зависимости от того, что наступит раньше. Можно выбрать переход на лицензии Human Resources раньше, если это поможет снизить затраты. Начиная с февраля 2025 года все существующие клиенты CSP и EA должны перестать использовать модуль HR и приобрести лицензии Human Resources, чтобы воспользоваться преимуществами новых возможностей, которые появляются в приложениях Finance and Operations.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Моя организация активно использует Dynamics 365 Finance, Supply Chain Management, Commerce или Project Operations. Потребуется ли приобретение дополнительной среды для поддержки объединения инфраструктуры?

Дополнительные среды не требуются для поддержки изменения инфраструктуры.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Куда можно обратиться, если у меня есть дополнительные вопросы о лицензировании продуктов?

При наличии вопросов о лицензировании можно найти дополнительную информацию в [Центре бизнес-приложений — цены и лицензирование D365](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Если эта информация не помогает вам с вашей проблемой, откройте запрос на LicenseQ.
