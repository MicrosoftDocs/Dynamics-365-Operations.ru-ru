---
title: Копирование экземпляра
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010288"
---
# <a name="copy-an-instance"></a>Копирование экземпляра

Можно использовать Microsoft Dynamics Lifecycle Services (LCS) для копирования базы данных Microsoft Dynamics 365 Human Resources в среду в песочнице. При наличии другой среды-песочницы можно также скопировать базу данных из этой среды в целевую среду-песочницу.

Чтобы скопировать экземпляр, необходимо обеспечить следующее:

- Экземпляр Human Resources, который требуется перезаписывать, должен быть средой песочницы.

- Среды, которых копируются, должны быть в одном регионе. Нельзя копировать по регионам.

- Вы должны быть администратором в целевой среде, чтобы можно было войти в систему после копирования экземпляра.

- При копировании базы данных Human Resources не копируются элементы (приложения или данные), содержащиеся в среде Microsoft PowerApps. Сведения о способе копирования элементов в среде PowerApps см. в разделе [Копирование среды](https://docs.microsoft.com/power-platform/admin/copy-environment). Среда PowerApps, которую требуется перезаписывать, должна быть средой песочницы. Чтобы изменить производственную среду PowerApps на среду песочницы, необходимо быть глобальным администратором клиента. Дополнительные сведения об изменении среды PowerApps см. в разделе [Переключение экземпляра](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>Результаты копирования базы данных Human Resources

При копировании базы данных Human Resources происходят следующие события:

- Процесс копирования стирает существующую базу данных в целевой среде. После завершения процесса копирования восстановить существующую базу данных невозможно.

- Целевая среда будет недоступна до завершения процесса копирования.

- Документы в хранилище BLOB-объектов Microsoft Azure не копируются из одной среды в другую. Таким образом, все документы и шаблоны, которые прикрепляются, не будут скопированы и останутся в исходной среде.

- Все пользователи, кроме администратора и других учетных записей пользователей внутренних служб, будут недоступны. Таким образом, пользователь с правами администратора может удалять или заменять данные до того, как другие пользователи смогут вернуться в систему.

- Пользователь-администратор должен выполнить необходимые изменения конфигурации, такие как повторное подключение конечных точек интеграции к отдельным службам или URL-адресам.

## <a name="copy-the-human-resources-database"></a>Копирование базы данных Human Resources

Чтобы выполнить эту задачу, необходимо сначала скопировать экземпляр, а затем войти в центр администрирования Microsoft Power Platform, чтобы скопировать среду PowerApps.

> [!WARNING]
> При копировании экземпляра база данных удаляется из целевого экземпляра. Целевой экземпляр недоступен в ходе этого процесса.

1. Выполните вход LCS и выберите проект LCS, содержащий экземпляр, который необходимо скопировать.

2. В проекте LCS выберите плитку **Управление приложением Human Resources**.

3. Выберите экземпляр для копирования, а затем выберите **Копировать**.

4. В области задач **Копирование экземпляра** выберите экземпляр, который требуется перезаписать, и нажмите кнопку **Копировать**. Дождитесь обновления значения поля **Статус копирования** до **Завершено**.

   ![[Выберите экземпляр для перезаписи](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Выберите **Power Platform** и выполните вход в центр администрирования Microsoft Power Platform.

   ![[Выберите Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Выберите среду PowerApps для копирования, а затем выберите **Копировать**.

7. После завершения процесса копирования выполните вход в целевой экземпляр и включите интеграцию Common Data Service. Для получения дополнительных сведений и инструкций см. раздел [Настройка интеграции Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

## <a name="data-elements-and-statuses"></a>Элементы данных и статусы

Следующие элементы данных не копируются при копировании экземпляра Human Resources:

- Адреса электронной почты в таблице **LogisticsElectronicAddress**

- Журнал пакетных заданий в **BatchJobHistory**, **BatchHistory** и **BatchConstraintHistory**

- Пароль SMTP в таблице **SysEmailSMTPPassword**

- Сервер ретрансляции SMTP в таблице **SysEmailParameters**

- Параметры управления печатью в таблицах **PrintMgmtSettings** и **PrintMgmtDocInstance**

- Записи, специфические для данной среды в таблицах **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** и **BatchServerGroup**

- Вложения документов в таблице DocuValue. К этим вложениям относятся все шаблоны Microsoft Office, которые были перезаписаны в исходной среде

- Строка доступа в таблице **PersonnelIntegrationConfiguration**

Некоторые из этих элементов не копируются, поскольку они связаны с определенной средой. Примерами являются записи **BatchServerConfig** и **SysCorpNetPrinters**. Другие элементы не копируются из-за объема запросов технической поддержки. Например, повторяющиеся сообщения электронной почты могут быть отправлены, поскольку протокол SMTP все еще включен в среде приемочного тестирования пользователя (песочнице), могут быть отправлены недопустимые сообщения интеграции, так как пакетные задания по-прежнему включены, и пользователи могут быть включены до того, как администраторы смогут выполнить действия по очистке после обновления.

Кроме того, при копировании экземпляра изменяются следующие статусы:

- Все пользователи, кроме администраторов задаются как **Отключено**.

- Все пакетные задания, за исключением некоторых системных заданий, устанавливаются в значение **Удержание**.

## <a name="environment-admin"></a>Администратор среды

Все пользователи в целевой среде песочницы, включая администраторов, заменяются пользователями исходной среды. Перед копированием экземпляра убедитесь, что вы являетесь администратором в целевой среде. Если это не так, после завершения копирования вы не сможете войти в целевую среду песочницы.

Все пользователи, не являющиеся администраторами в целевой среде песочницы, отключены для защиты от нежелательного входа в среду песочницы. Администраторы могут повторно включить пользователей, если это необходимо.