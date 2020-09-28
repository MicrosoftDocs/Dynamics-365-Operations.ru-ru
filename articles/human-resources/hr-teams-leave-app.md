---
title: Управление запросами на отпуск в Teams
description: В этом разделе показано, как запросить отпуск в приложении Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766768"
---
# <a name="manage-leave-requests-in-teams"></a>Управление запросами на отпуск в Teams

[!include [banner](includes/preview-feature.md)]

Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет быстро запросить отпуск и просмотреть сведения о балансе времени прямо в Microsoft Teams. Можно взаимодействовать с ботом для запроса информации. Вкладка **Отгул** содержит более детальная информация.

## <a name="install-the-app"></a>Установка приложения

Приложение "Human Resources" можно найти в магазине "Teams".

1. В Microsoft Teams выберите многоточие.

   ![Многоточие приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. Выполните поиск Dynamics 365 Human Resources, а затем выберите плитку **Human Resources**.

   ![Плитка HR приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. Для установки приложения нажмите кнопку **Добавить**.

   ![Установка приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

Если приложение не выполняет автоматический вход, выберите вкладку **Параметры**, чтобы выполнить вход.

![Вкладка Параметры приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна. 

Если имеется доступ к нескольким экземплярам "Human Resources", можно выбрать среду, к которой необходимо подключиться, на вкладке **Параметры**.

> [!WARNING]
> Приложение в настоящее время не поддерживает роль "системный администратор" и выводит сообщение об ошибке, если вход осуществляется с учетной записью системного администратора. Чтобы войти с использованием других учетных записей, на вкладке **Параметры** нажмите кнопку **переключателя счетов**, а затем выполните вход с учетной записью пользователя, не обладающей правами администратора системы.
 
## <a name="use-the-bot"></a>Использование бота

После установки приложения появится приветственное сообщение, позволяющее знать типы действий, которые может выполнять бот от вашего имени.

![Приветственное сообщение бота для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> При первом взаимодействии с ботом может потребоваться выполнить вход. Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.

Можно спросить бота о следующем:

- Отображение сведений о балансе времени для каждого типа отпусков, которые вам назначены.

   ![Показать балансы приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- Отображение дополнительных сведений о конкретном типе отпуска.

   ![Показать сведения приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- Запустите запрос на отпуск для вас.

   ![Запрос на отпуск приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
После того как вы запустите запрос на отпуск, вы можете скорректировать дни непосредственно в карточке.

![Изменить запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
По завершении ввода данных выберите **Отправить**, чтобы отправить его на утверждение. Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.

![Отправка запросов для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Управление отпуском в Teams

Вкладка **Отгул** служит для просмотра следующих элементов:

- Сведения о балансе времени для каждого типа отпусков, которые вам назначены

- Предстоящие запросы на отпуск

- Запросы на отгулы

- Черновые запросы на отпуск

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Создание нового запроса

1. Выберите **Новый запрос** для создания нового запроса на отпуск.

   ![Новый запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Введите день или дни, которые требуется взять отпуск, а затем нажмите кнопку **Добавить**.

   ![Добавить отпуск для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Если применимо, введите код причины. Кроме того, необходимо ввести комментарии и добавить вложения.

4. По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение. Можно также ввести **Сохранить как черновик**, чтобы вернуться к нему позже.

### <a name="manage-draft-requests"></a>Управление черновыми запросами

1. Выберите вкладку **Черновики**.

   ![Вкладка Черновики для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. Выберите карандаш для редактирования запроса или выберите корзину, чтобы удалить запрос.

3. Внесите любые необходимые изменения. По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение. Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.

   ![Изменить черновик для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a>Уведомления Teams

Если вы или сотрудник, для которого вы являетесь утверждающим, отправляете запрос на отпуск, вы получите уведомление в приложении Human Resources в Teams. Можно выбрать уведомление для его просмотра. Уведомления также появляются в области **Чат**.

Если вы являетесь утверждающим, вы можете выбрать **Утвердить** или **Отклонить** в уведомлении. Кроме того, можно указать необязательное сообщение.

![Уведомление о запросе отпуска в приложении Human Resources в Teams](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a>Просмотр календаря отпусков рабочей группы

Если вы являетесь руководителем с непосредственными подчиненными, вы можете просмотреть утвержденные и ожидающие утверждения запросы отгулов для вашей рабочей группы.

1. В приложении Human Resources app в Teams выберите **Отгул**.

2. Выберите **Календарь рабочей группы**.

   ![Просмотр календаря в приложении Human Resources в Teams](./media/hr-teams-leave-app-view-calendar.png)

В календаре отображаются утвержденные и ожидающие утверждения отгулы ваших непосредственных подчиненных.

![Календарь отгулов в приложении Human Resources в Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a>Уведомление о конфиденциальности

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели. Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS). Узнайте подробнее о LUIS [здесь](https://www.luis.ai/). Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso). Затем эта информация передается в Microsoft  [Azure bot framework](https://azure.microsoft.com/services/bot-service/), которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя. 

Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем. Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources. Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework. 

Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания. Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>Сетка событий Microsoft Azure и Microsoft Teams

При использовании функции уведомлений для приложения Dynamics 365 Human Resources в Teams некоторые клиентские данные будут выходить из географического региона, в котором развернута служба Human Resources вашего клиента. Dynamics 365 Human Resources передает сведения о запросе отпуска сотрудника и задачах рабочего процесса в сетку событий Microsoft Azure и Microsoft Teams. Эти данные могут храниться в течение 24 часов и обрабатываться в США, шифруются при передаче и при хранении, и не используются корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.

## <a name="see-also"></a>См. также

[Загрузка и установка Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Центр справки Microsoft Teams](https://support.office.com/teams)</br>
[Приложение Human Resources в Teams](hr-admin-teams-leave-app.md)
