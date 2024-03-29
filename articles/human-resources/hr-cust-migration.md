---
title: Миграция клиентов Dynamics 365 Human Resources в инфраструктуру для управления финансами и операциями
description: В этой статье описывается миграция клиентов Microsoft Dynamics 365 Human Resources в инфраструктуру приложений для управления финансами и операциями.
author: twheeloc
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9680c2d1caa08c15aed325f4153aac6eae63c3
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831729"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Миграция клиентов Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Миграция клиентов — это "миграция lift-and-shift" (перемещение) базы данных клиентов в инфраструктуру приложений для управления финансами и операциями. Для нее используется инструмент автоматического переноса. В результате получается новая среда приложений для управления финансами и операциями, в которой используется база данных Human Resources клиента.

## <a name="prerequisites"></a>Необходимые условия

### <a name="user-access-and-permissions"></a>Доступ и разрешения пользователей

- Пользователь служб Microsoft Dynamics Lifecycle Services должен иметь роль **Администратор организации**.
- Пользователь должен иметь возможность [создавать проекты Azure DevOps](/azure/devops/organizations/projects/create-project) или использовать существующие проекты Azure DevOps.
- Пользователь должен иметь доступ для [создания личного маркера безопасности доступа Azure DevOps](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) или маркер, доступный для использования.

### <a name="dataverse-environment-backup-sandbox"></a>Резервная среда Dataverse (песочница)

 - Необязательно, но рекомендуется: обновите существующую среду "песочницы" Human Resources, используя копию производственной среды Human Resources.
 - Создайте новую среду Dataverse с помощью центра администрирования Power Platform.
 - Скопируйте существующую среду Dataverse, связанную с автономным приложением Human Resources, в среду, созданную на предыдущем шаге.

> [!NOTE]
> При добавлении базы данных убедитесь, что для параметра **Включить приложения Dynamics 365** установлено значение **Да**. Подробные сведения см. в разделе [Подготовка среды Power Platform](hr-cust-migration.md#prepare-a-power-platform-environment).

### <a name="dataverse-capacity"></a>Емкость Dataverse

1. Используйте страницу **Сводка** в центре администрирования Power Platform для проверки того, что в [хранилище Dataverse](/power-platform/admin/finance-operations-storage-capacity) имеется достаточно свободного места для копирования среды.
2. Если нет достаточной емкости, воспользуйтесь [руководством по высвобождению места в хранилище](/power-platform/admin/free-storage-space) для уменьшения общего потребления. Клиенты также могут [добавить дополнительную емкость хранилища](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Процесс миграции клиентов

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Создание проекта Lifecycle Services для переноса Human Resources

Первым шагом является создание нового проекта внедрения финансов и операций в службе Lifecycle Services. У клиента будет существующий проект Human Resources Lifecycle Services. Существующие среды Human Resources будут перенесены в новый проект внедрения приложений для управления финансами и операциями.

Чтобы создать новый проект, выполните следующие действия.

1. Выполните вход в службы Lifecycle Services в качестве глобального администратора или назначенного пользователя учетной записи службы.
2. На главной странице Lifecycle Services выберите **Создать/новый (+)**.
3. Выберите приложения для управления финансами и операциями в качестве продукта.
4. В поле **Цель проекта** выберите **Реализация**.
5. Ввести наименование и описание проекта.
6. В поле **Пользовательский тип проекта** выберите **Миграция Microsoft Dynamics 365 Human Resources**.
7. Выберите флажок, чтобы принять условия.
8. Выберите **Создать**.

После создания нового проекта Lifecycle Services выполните следующие действия, чтобы настроить и сконфигурировать проект.

1. Выберите **Адаптация проекта**, чтобы завершить адаптацию проекта. Дополнительные сведения см. в разделе [Адаптация проекта](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Выберите тот же регион, что и для текущих сред. Этот выбор не повлияет на миграцию.
    - Для устаревших систем выберите **Другое**.

2. Завершите настройку параметров проекта. Как часть этого шага, следует настроить библиотеку SharePoint Online, Azure DevOps и подключения Azure, если это необходимо. Дополнительные сведения см. в разделе [Руководство пользователя служб Lifecycle Services (LCS)](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Клиенты могут использовать существующий проекта Azure DevOps и связанный с ним личного маркера безопасности доступа. Если используется существующий проект, конфигурации, которые относятся к проекту, автоматически доступны и могут быть проверены на точность.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Миграция среды песочницы Human Resources

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Подготовка к миграции среды песочницы

После создания нового проекта Lifecycle Services и выполнения процесса адаптации проекта все готово к миграции первой среды. Перед началом процесса рекомендуется обновить среду песочницы, которую необходимо перенести из производственной среды в автономную инфраструктуру.

#### <a name="prepare-a-power-platform-environment"></a>Подготовка среды Power Platform

> [!NOTE]
> Этот шаг применяется только к миграции среды "песочницы". При миграции производственной среды существующая среда центра администрирования Power Platform, прикрепленная к производственной среде, будет перенесена первой. При добавлении базы данных убедитесь, что для кнопки **Включить приложения Dynamics 365** установлено значение **Да**. 

- В центре администрирования Power Platform [создайте среду с базой данных](/power-platform/admin/create-environment#create-an-environment-with-a-database), которая будет использоваться для миграции "песочницы", или выберите существующую среду.
- [Скопируйте среду](/power-platform/admin/copy-environment) для обновления среды Power Platform, используемой для сопоставления.

#### <a name="migrate-the-sandbox-environment"></a>Миграция среды песочницы

1. Выполните вход в службы Lifecycle Services в качестве глобального администратора или назначенного пользователя учетной записи службы.

    > [!NOTE]
    > Рекомендуется использовать именную учетную запись пользователя. У вошедшего пользователя должна быть роль безопасности **Владелец проекта** или **Менеджер среды** в автономном проекте Lifecycle Services Human Resources.

2. Откройте только что созданный проект миграции Human Resources.
3. Просмотрите и выполните соответствующие этапы методологии миграции и адаптации проекта.
4. На панели мониторинга проекта в области **По умолчанию. Приемочное тестирование версии Standard** выберите **Миграция HR**.
5. В области **Выберите среду для миграции** выберите соответствующий проект Lifecycle Services и исходную среду Human Resources (из исходного автономного приложения Human Resources).
6. Включите **Сопоставить с новой средой Power Platform** и выберите соответствующую среду Power Platform. Затем выберите **Далее**.
7. Выполните мастер **Параметры развертывания (финансы и операции – песочница)** для подтверждения сведений и приемки клиентом, затем выберите **Развернуть**.

Состояние среды будет показывать ход выполнения. Состояние будет изменено с **Загрузка** **Развертывание**, затем на **Развернуто**.

> [!NOTE]
> Производственная область будет недоступна до тех пор, пока не будет выполнен контрольный список готовности проекта к вводу в эксплуатацию. Дополнительные сведения см. в разделе [Подготовка к вводу в эксплуатацию](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Соображения и допущения

Среда "песочницы" Human Resources существует в проекте Lifecycle Services в клиенте, который обладает следующими характеристиками:

- Среда "песочницы" Human Resources не связана с существующей объединенной средой. Для конкретной среды Human Resources только одна миграция может выполняться одновременно.
- Количество сред песочницы, которые разрешены в каждый момент времени, основано на лицензировании Human Resources. Если для клиента было приобретено достаточное количество лицензий, в области **Среды** проекта будут отображаться дополнительные среды песочницы.
- Миграции должны выполняться для сред одного типа. Другими словами, можно выполнять только миграции "песочница-песочница" или "производство-производство".

    > [!NOTE]
    > Когда определяется статус производственной среды или песочницы, рассматриваются только типы среды Human Resources. Если среды неправильно классифицируются (то есть, производственная среда помечается как среда "песочницы", либо среда "песочницы" помечена как производственная среда), обратитесь в службу поддержки.

- Если миграция не была успешно выполнена, будет выведено сообщение об ошибке и станет доступна кнопка **Удалить**. Используйте эту кнопку, чтобы удалить неудачно выполненную миграцию. После этого можно повторно выполнить миграцию среды.

#### <a name="validate-the-sandbox-migration"></a>Проверка миграции песочницы

После успешного завершения процесса миграции "песочницы" создайте подробный план испытаний для проверки и приемки для всех бизнес-процессов.

Перед началом тестирования проверьте следующие сведения:

- Убедитесь, что перенесенная среда доступна по созданному URL-адресу.
- Убедитесь, что пользователи имеют доступ к мигрированной песочнице.
- Убедитесь, что среда Dataverse, связанная с перенесенной средой "песочницы", доступна.
- Точечно проверьте различные данные, чтобы убедиться, что доступны самые последние данные.
- Выполните важные бизнес-процессы для проверки.
- Убедитесь, что политики безопасности применимы.
- Убедитесь, что пакетные задания запускаются ожидаемым образом.

У вас не будет доступа удаленного рабочего стола к перенесенной изолированной среде. Можно использовать возможности и средства самообслуживания для выполнения следующих действий в среде "песочницы" уровня 2+:

- Доступ к [базе данных Azure SQL](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Доступ к [файлам журналов](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Использование [средств мониторинга производительности](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- [Включение и отключение режима обслуживания](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Перезапуск [служб](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Настройка [Regression Suite Automation Tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Дополнительные сведения см. в разделе [Вопросы и ответы для дистанционного развертывания](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Миграция производственной среды Human Resources

После завершения миграции и проверки среды "песочницы" выполните следующие шаги для миграции производственной среды.

#### <a name="prerequisites"></a>Необходимые условия

- Должно быть выполнено средство оценки подписки.
- Оценка [готовности к вводу в эксплуатацию](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) должна быть завершена.
- Пользователь, инициирующий производственную миграцию в Lifecycle Services, должен иметь роль системного администратора на Power Platform. 

#### <a name="migrate-the-production-environment"></a>Миграция производственной среды

1. Выполните вход в службы Lifecycle Services в качестве глобального администратора или назначенного пользователя учетной записи службы.

    > [!NOTE]
    > Рекомендуется использовать именную учетную запись пользователя. У вошедшего пользователя должна быть роль безопасности **Владелец проекта** или **Менеджер среды** в проекте Lifecycle Services.

2. Откройте новый проект миграции Human Resources.
3. Просмотрите и выполните соответствующие этапы методологии миграции и адаптации проекта.
4. На панели мониторинга проекта в области **Рабочий** выберите **Миграция HR**.
5. В области **Выберите среду для миграции** выберите соответствующий проект Lifecycle Services и исходную среду Human Resources (из исходного автономного приложения Human Resources). Затем выберите **Далее**.
6. Выполните мастер **Параметры развертывания (финансы и операции – песочница)** для подтверждения сведений и приемки клиентом, затем выберите **Развернуть**.

Состояние среды будет показывать ход выполнения развертывания. Состояние будет изменено с **Загрузка** **Развертывание**, затем на **Развернуто**.

#### <a name="post-migration-considerations"></a>Соображения после миграции

- Примените последние [обновления качества](/fin-ops-core/fin-ops/get-started/quality-updates) к вашим средам.
- Если используются [виртуальные таблицы](hr-admin-integration-common-data-service-virtual-entities.md), перенастройте конечные точки.
- Перенастройте интеграцию двойной записи. Оцените, какие сущности должны быть включены.
- Рекомендуется использовать виртуальные таблицы для замены двойной записи для интеграции.

#### <a name="dual-write-integration"></a>Интеграция двойной записи

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Настройка интеграции двойной записи Microsoft Power Platform

1. Перейдите в центр администрирования Power Platform и выберите **Среды** в левой области навигации.
2. Выберите ранее скопированную или обновленную среду и убедитесь, что она находится в состоянии **Готов**.
3. Перейдите в Lifecycle Services и убедитесь, что проект миграции находится в состоянии **Развернут**.
4. В перемещенной среде выберите **Полные сведения** для просмотра дополнительных сведений и [настройки приложения двойной записи](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. В области **Конфигурирование приложения для двойной записи** установите флажок, чтобы согласиться на сопоставление и синхронизацию данных между базами данных, затем выберите **Настроить**.
6. Когда в окне сообщения выводится уведомление об успешной конфигурации двойной записи, выберите **ОК**.
7. Можно отслеживать ход выполнения настройки в сведениях.
8. После завершения настройки выберите команду **связь со средой Power Platform**, чтобы синхронизировать доступные сущности данных.
9. Когда статус указывает на то, что среды были успешно связаны, перейдите в центр администрирования Power Platform, чтобы просмотреть и выбрать соответствующие сущности данных.
10. В левой области выберите **Приложения Dynamics 365 \> Ресурсы**.
11. Убедитесь, что статус двойной записи приложения Human Resources **Включен**.
12. Выберите приложение двойной записи Human Resources, затем выберите **Установить**.
13. В области **Установка приложения двойной записи Dynamics 365 Human Resources** выберите подходящую среду для установки в нее пакета.
14. Установите флажок, чтобы согласиться с условиями обслуживания, затем выберите **Установить**.
15. В среде приложений Dynamics 365 состояние будет **Устанавливается** в ходе установки. Оно будет обновлено до **Установлено** после завершения установки.

##### <a name="review-and-apply-a-dual-write-solution"></a>Проверка и применение решения двойной записи

1. В новой среде приложений для управления финансами и операциями перейдите в раздел **Управление данными \> Двойная запись**.
2. Выберите **Применить решение**.
3. В этой области выберите **Установленные решения Dynamics**, **Сопоставления основных сущностей приложений двойной записи** и **Сопоставления Dynamics 365 Human Resources**. Затем выберите **Применить**. Сообщение подтверждает применение решения. После успешного применения решения все доступные сопоставления таблиц будут показаны.
4. Просмотрите доступные сопоставления таблиц, чтобы выбрать и выполнить интеграцию, используя двойную запись.
5. При первом запуске интеграции двойной записи для сопоставлений таблиц установите флажок **Начальная синхронизация**. При наличии существующей интеграции из исходной среды Human Resources не нужно выбирать флажок **Начальная синхронизация** при выполнении интеграции для сопоставлений таблиц.

#### <a name="recommended-practices"></a>Рекомендуемые методы

В этом разделе описываются рекомендации по миграции из автономной инфраструктуры в инфраструктуру приложений для управления финансами и операциями.

- Мы настоятельно рекомендует вам работать с партнером Microsoft Dynamics для получения помощи по переносу среды Human Resources.
- Планируйте время, необходимое для полного приемочного тестирования пользователем (UAT) в "песочнице" перенесенной среды.
- Планируйте и документируйте подробное описание шагов по миграции интеграций в перенесенную среду.
- Создайте подробный контрольный список для структурирования процесса переключения для миграции.
- Планируйте подходящее время простоя для компании во время миграции.
- Настоятельно рекомендуется, чтобы клиенты, имеющие право на FastTrack, взаимодействовали с их архитектором решений FastTrack, чтобы получить помощь в контроле процесса миграции.
- Перед первой миграцией настоятельно рекомендуется обновить среду "песочницы" в изолированной инфраструктуре. Это обновление должно включать среду Dataverse, подключенную к среде "песочницы", в которую планируется выполнить миграцию.
- Настоятельно рекомендуется использовать учетную запись службы при развертывании, миграции и создании проекта Lifecycle Services.
- Планируйте обновление среды "песочницы" для проверки UAT в новейшем общедоступном выпуске (GA). Дополнительные сведения см. в разделе [соображений](hr-infrastructure-merge.md#considerations).
