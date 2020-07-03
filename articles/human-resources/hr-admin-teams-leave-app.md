---
title: Приложение Human Resources в Teams
description: Эта тема знакомит с приложением Microsoft Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431138"
---
# <a name="human-resources-app-in-teams"></a>Приложение Human Resources в Teams

[!include [banner](includes/preview-feature.md)]

Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет сотрудникам быстро запросить отпуск и просмотреть сведения о балансе времени в Microsoft Teams. Сотрудники могут взаимодействовать с ботом для запроса информации. Вкладка **Отгул** содержит более детальная информация.

![Бот для приложения отпусков Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Установка и настройка

Приложение "Human Resources" можно найти в магазине "Teams". Сведения об установке приложения Teams см. в разделе [Управление запросами на отпуск в Teams](hr-teams-leave-app.md).

Сведения об управлении разрешениями приложений в Teams см. в разделе [Управление политиками разрешений приложений в Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="known-issues"></a>Известные проблемы

| Расход | Состояние |
| --- | --- |
| Ошибка: обнаружена проблема при поиске среды для подключения. | Эта ошибка может появиться даже в том случае, если известно, что пользователь может получить доступ к одной или нескольким средам Human Resources. Кроме того, могут не отображаться все ожидаемые среды. До тех пор, пока проблема не исправлена, удалите пользователя и повторите импорт для решения проблемы. |
| Неверное сальдо при подаче запроса на отпуск для будущей даты. | Прогнозирование пока недоступно. Сальдо отображается для текущей даты. |
| При уменьшении количества часов, взятых в существующем запросе, **Остаток сальдо** уменьшается вместо увеличения. | Мы решим эту известную проблему в будущем. Отображение неверно, но правильные суммы корректируются при отправке. |
| Две карточки **предстоящих отпусков** отображаются для одних и тех же дат. | Карточки представляют собой отдельные отправки. Мы будем продолжать получать отзывы и корректировки. |
| Не удается отменить запрос **На рассмотрении**. | Эта функциональная возможность в настоящее время не поддерживается и будет добавлена в будущем выпуске. |
| Сведения о сальдо рассчитываются на сегодняшний день. | В настоящее время в системе не отображается сальдо на период начисления, даже если оно настроено в параметрах отпусков и отсутствия. |

## <a name="privacy-notice"></a>Уведомление о конфиденциальности

При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели. Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS). Узнайте подробнее о LUIS [здесь](https://www.luis.ai/). Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso). Затем эта информация передается в Microsoft [Azure bot framework](https://azure.microsoft.com/services/bot-service/) , которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя. 

Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем. Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources. Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework. 

Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания. Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>См. также 

[Загрузка и установка Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Центр справки Microsoft Teams](https://support.office.com/teams)</br>
[Управление запросами на отпуск в Teams](hr-teams-leave-app.md)

