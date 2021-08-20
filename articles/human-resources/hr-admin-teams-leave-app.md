---
title: Приложение Human Resources в Teams
description: Эта тема знакомит с приложением Microsoft Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3b717cf2fb8663ed8e4981981d563672c9e645c4f9b592ee1896cfef4236396
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772725"
---
# <a name="human-resources-app-in-teams"></a>Приложение Human Resources в Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет сотрудникам быстро запросить отпуск и просмотреть сведения о балансе времени в Microsoft Teams. Сотрудники могут взаимодействовать с ботом для запроса информации. Вкладка **Отгул** содержит более детальная информация. Кроме того, они могут отправлять пользователям сведения о предстоящих отгулах в рабочих группа и чатах вне приложения Human Resources.

![Бот для приложения отпусков Human Resources Teams.](./media/hr-teams-leave-app-bot.png)

![Вкладка Отгул для приложения отпусков Human Resources Teams.](./media/hr-teams-leave-app-timeoff-tab.png)

![Карточка запроса отпуска в Human Resources.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Установка и настройка

Приложение Dynamics 365 Human Resources можно найти в магазине Teams. Сведения об установке приложения Teams см. в разделе [Управление запросами на отпуск в Teams](hr-teams-leave-app.md).

Сведения об управлении разрешениями приложений в Teams см. в разделе [Управление политиками разрешений приложений в Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

Если требуется, чтобы пользователи могли просматривать календарь отпусков и отсутствия в приложении, необходимо включить **Календарь отпусков и отсутствия в Teams** в управлении функциями. Дополнительные сведения о включении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Включение уведомлений для приложения Human Resources в Teams

Если требуется, чтобы пользователи получали уведомления о запросах на отпуск в приложении Teams, необходимо включить уведомления в Dynamics 365 Human Resources.

>[!NOTE]
>Уведомления будут получать только пользователи, вошедшие в Teams и использующие приложение Dynamics 365 Human Resources.

1. В модуле Human Resources выберите **Администрирование системы**.

2. Выберите **Ссылки**.

3. В разделе **Настройка** выберите **Системные параметры**.

4. На вкладке **Общие** установите для параметра **Включить уведомления для приложения Teams** значение **Да**.

   ![Включение уведомлений приложения Teams в системных параметрах.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Для включения уведомлений в Teams для всех пользователей выберите **Да** в ответ на запрос.

   ![Включение уведомлений Teams для всех пользователей.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Включение и выключение уведомлений Teams для отдельных пользователей

После включения уведомлений для приложения Dynamics 365 Human Resources Teams можно включать или отключать уведомления для отдельных пользователей.

1. В модуле Human Resources выберите **Администрирование системы**.

2. Выберите **Ссылки**.

3. В области **Пользователи** выберите **Параметры пользователей**.

4. Выберите вкладку **Рабочий процесс**.

5. Установите для параметра **Включить уведомления для приложения Teams** значение **Да**, чтобы включить уведомления для пользователя, или значение **Нет**, чтобы отключить уведомления для пользователя.

   ![Включение уведомлений приложения Teams в параметрах пользователя на вкладке рабочего процесса.](./media/hr-admin-teams-leave-app-notifications.png)

6. Нажмите **Сохранить**.

## <a name="supported-languages"></a>Поддерживаемые языки

Приложение Dynamics 365 Human Resources в Teams поддерживает следующие языки:

| Код языка | Язык |
| --- | --- |
| de-DE | Немецкий (Германия) |
| es-ES | Испанский (Испания) |
| es-MX | Испанский (Мексика) |
| fr-CA | Французский (Канада) |
| fr-FR | Французский (Франция) |
| it-IT | Итальянский (Италия) |
| nl-NL | Нидерландский (Нидерланды) |
| pt-BR | Португальский (Бразилия) |
| tr-TR | Турецкий (Турция) |
| zh-CN | Китайский (упрощенное письмо) |

## <a name="notes"></a>Основание

Следующие рабочие элементы включены в будущие выпуски:

| Рабочий элемент | Состояние |
| --- | --- |
| Неверное сальдо при подаче запроса на отпуск для будущей даты. | Прогнозирование пока недоступно. Сальдо отображается для текущей даты. |
| Не удается отменить запрос **На рассмотрении**. | Эта функциональная возможность в настоящее время не поддерживается и будет добавлена в будущем выпуске. |
| Сведения о сальдо рассчитываются на сегодняшний день. | В настоящее время в системе не отображается сальдо на период начисления, даже если оно настроено в параметрах отпусков и отсутствия. |

## <a name="troubleshooting"></a>Устранение неполадок

Если пользователь не может войти в систему или использовать приложение Human Resources Teams, попробуйте выполнить следующие инструкции по устранению неполадок. Если после устранения неполадок все еще возникают проблемы, обратитесь в службу поддержки. Для получения дополнительных см. [Получение поддержки](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Невозможно выполнить вход в приложение Human Resources в Teams

Если пользователь обращается к вам из-за того, что он не может войти в приложение, убедитесь, что у пользователя имеется соответствующая запись сотрудника в управлении персоналом.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Ошибка при утверждении запросов отпуска в приложении Human Resources в Teams

Если пользователь получает ошибку при попытке утверждения запросов на отпуск в приложении Teams выполните следующие действия по устранению неполадок:

1. Убедитесь, что их учетная запись Teams совпадает с той, которая используется для доступа к модулю Human Resources.

2. Проверьте, что они действительно являются утверждающим для этого запроса, проверив параметры рабочего процесса для утверждения отпуска. Дополнительные сведения о рабочих процессах запроса отпуска см. в разделе [Создание рабочего процесса запроса отпуска](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Утверждающие отпуска не получают сообщения чата Teams для утверждения запросов на отпуск

1. Убедитесь, что для среды и пользователя включены уведомления. Дополнительные сведения см. в [Включение уведомлений для приложения Human Resources в Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) и [Включение и выключение уведомлений Teams для отдельных пользователей](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Убедитесь, что пользователи вошли в систему на вкладке **Чаты** с теми же учетными данными, которые используются для утверждения запросов на отпуск. Используйте сообщения "выйти", а затем "войти", чтобы войти в систему, используя правильные учетные данные.

3. Если проблема сохраняется, проверьте статус пакетного задания системы бизнес-событий как системный администратор. Если он находится на ожидающем или выполняющемся этапе, проверьте через несколько минут. Если статус не меняется, отправьте запрос в службу поддержки, чтобы ее сотрудники могли помочь в устранении проблемы.

## <a name="privacy-notice"></a>Уведомление о конфиденциальности

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели. Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS). Узнайте подробнее о LUIS [здесь](https://www.luis.ai/). Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso). Затем эта информация передается в Microsoft  [Azure bot framework](https://azure.microsoft.com/services/bot-service/), которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.

Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем. Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources. Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework. 

Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания. Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, сетка событий Azure и Azure Cosmos DB

При использовании функции уведомлений для приложения Dynamics 365 Human Resources в Microsoft Teams некоторые клиентские данные могут выходить из географического региона, в котором развернута служба Human Resources вашего клиента.

Dynamics 365 Human Resources передает сведения о запросе отпуска сотрудника и задачах рабочего процесса в сетку событий Microsoft Azure и Microsoft Teams. Эти данные могут храниться в сетке событий Microsoft Azure в течение 24 часов и будут обрабатываться в США, шифруются при передаче и при хранении, и не используются корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания. Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

При взаимодействии с чат-ботом в приложении Human Resources содержимое беседы может храниться в Azure Cosmos DB и передаваться в Microsoft Teams. Эти данные могут храниться в Azure Cosmos DB течение 24 часов и могут быть обработаны вне географического региона, в котором развернута служба Human Resources для клиента, шифруются при передачи и хранении, и не используется корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания. Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Для ограничения доступа к приложению Human Resources в Microsoft Teams для вашей организации или пользователей в организации см. раздел [Управление политиками разрешений приложений в Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>См. также 

[Загрузка и установка Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Центр справки Microsoft Teams](https://support.office.com/teams)</br>
[Управление запросами на отпуск в Teams](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]