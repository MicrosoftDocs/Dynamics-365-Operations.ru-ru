---
title: Поиск кандидатов с помощью LinkedIn Recruiter в Microsoft Dynamics 365 for Talent - Attract
description: Используйте интеграцию LinkedIn, предоставляемую Microsoft Dynamics 365 for Talent - Attract, для поиска кандидатов на вакансии с помощью LinkedIn Recruiter.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 14aba16fa81a8f25d0f88247319254407d428b2a
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739457"
---
# <a name="source-candidates-with-linkedin-recruiter"></a>Поиск кандидатов с помощью LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn — это крупнейшая в мире профессиональная сеть в Интернете, предоставляющая вам доступ к лучшим специалистам в мире. Microsoft Dynamics 365 for Talent: Attract позволяет искать кандидатов непосредственно из LinkedIn. Таким образом, легче будет найти кандидата, необходимого для заполнения открытых вакансий. После настройки подключения с LinkedIn через Attract можно просматривать потенциальных кандидатов из LinkedIn для должностей и экспортировать их в Attract всего одним щелчком мыши.

Если у вас нет такой возможности, обратитесь к администратору. Прежде чем вы сможете воспользоваться преимуществами LinkedIn Recruiter из Attract, администратор должен [настроить интеграцию с LinkedIn](./attract-admin-linkedin.md). Затем можно настроить подключение к LinkedIn Recruiter и начать поиск кандидатов.

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>Настройка подключения к LinkedIn Recruiter

Прежде чем начать работать с LinkedIn Recruiter через Attract, необходимо настроить подключение к LinkedIn Recruiter. Для этого шага требуются учетные данные пользователя LinkedIn Recruiter.

1. Выберите кнопку **Настройки** (значок шестеренки) в верхнем правом углу страницы.
2. Выберите **Параметры пользователя**.
3. На вкладке **Подключения** выберите **Подключить** рядом с **LinkedIn**. Следуйте указаниям, предоставленным LinkedIn.

    ![[Настройка подключения к LinkedIn Recruiter из Attract](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>Просмотр кандидатов LinkedIn в Attract

После подключения к LinkedIn Recruiter можно просматривать профили LinkedIn в Attract.

1. В Attract выберите **Должности** или **Кадровые пулы** слева, затем выберите соискателя.

    ![[Просмотр кандидатов из LinkedIn в Attract](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. В профиле кандидата выберите вкладку **LinkedIn**. Можно просмотреть профиль кандидата вместе с историей InMail и историей примечаний LinkedIn.

Отсюда можно сохранить кандидата в проекте LinkedIn Recruiter, отправить сообщение InMail или использовать функцию "держать меня в курсе", чтобы настроить оповещение в LinkedIn Recruiter.

> [!NOTE]
> Профиль LinkedIn для кандидата будет показан в Attract, когда информация в Attract о кандидате соответствует информации в LinkedIn. Используются следующие правила сопоставления:
> 
> 1. Если адрес электронной почты и кода участника LinkedIn совпадают в Attract и LinkedIn, будет показан профиль кандидата. Кандидаты по-прежнему имеют возможность установить или удалить связь профиля LinkedIn из Attract.
> 2. Если адрес электронной почты или код участника LinkedIn не совпадает, отображается список возможных кандидатов. Затем можно выбрать кандидата в списке и связать профиль.
> 3. Если нет удачных совпадений, появится сообщение о том, что совпадений не найдено.

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a>Экспорт кандидатов LinkedIn в Attract одним щелчком

При просмотре кандидатов в LinkedIn Recruiter можно экспортировать их в должности, которые в данный момент открыты в Attract. Для этого шага вам необходимо иметь в Attract разрешения нанимателя или специалиста по комплектации штата. Дополнительные сведения о ролях в Attract см. в разделе [Безопасность и управление ролями в Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).

Кроме того, необходимо убедиться, что должность находится на этапе соискателя. Подробнее см. в разделе [Действие подбора соискателей](./activities-attract.md#prospect-activity).

1. В Attract создайте должность, назначьте соответствующие роли и активируйте должность.
2. В LinkedIn Recruiter найдите подходящего кандидата на должность и перейдите к профилю кандидата.
3. В поле поиска должности в карточке контакта найдите должность по названию или коду должности, которая была активирована в Attract. Если не удается найти должность, выберите **Изменить ATS** для поиска соответствующего экземпляра Attract.
4. Выберите должность, затем выберите **Экспорт**.
5. В Attract откройте должность. Экспортированный кандидат появится на вкладке **Соискатель** должности.

## <a name="view-attract-information-in-linkedin-recruiter"></a>Просмотр информации Attract в LinkedIn Recruiter

В LinkedIn Recruiter можно отслеживать, подавал ли кандидат заявления на другие должности в вашей организации,посмотреть кандидатов на различных стадиях подачи заявления на должность, а также просмотреть отзывы и комментарии из Attract.

1. Откройте LinkedIn Recruiter и выберите профиль кандидата.
2. Наведите курсор на **В ATS**.
3. Выберите один из следующих параметров для просмотра сведений о кандидате, которые хранятся в Attract:

    - **Должности и статусы** — просмотр должностей, к которым относится кандидат, самый последний статус и прогресс кандидата по каждой должности.
    - **Отзыв о собеседовании** — просмотр отзыва, который проводившие собеседование сотрудники представили в Attract.
    - **Примечания** — просмотр всех примечаний, которые были введены для этого кандидата в Attract.

    ![[Просмотр сведений Attract из LinkedIn Recruiter](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> Данные о кандидате и заявлении о приеме на работу не будут синхронизированы с LinkedIn Recruiter, если кандидат не прошел далее стадии перспективного кандидата.

## <a name="view-linkedin-talent-pools"></a>Просмотр кадровых пулов LinkedIn

Если кандидаты соглашаются предоставить общий доступ к своим профилям LinkedIn любым пользователям вашей организации, новая запись создается в Attract. Эти кандидаты затем появятся в созданном системой кадровом пуле LinkedIn.

1. В Attract выберите **Кадровые пулы** в левой части.
2. Выберите кадровый пул LinkedIn. Будет отображен список кандидатов и их профили-заготовки из LinkedIn. Профили-заготовки содержат имя и фамилию кандидата и адрес электронной почты, если кандидат решил поделиться ими.

## <a name="see-also"></a>См. также

[Вопросы и ответы по LinkedIn](./attract-linkedin-faq.md)

[Настройка интеграции с LinkedIn](./attract-admin-linkedin.md)

[Создание вакансий](./creating-jobs-attract.md)

[Публикация вакансий в LinkedIn из Attract](./attract-post-jobs-to-linkedin.md)

[Устранение неполадок интеграции с LinkedIn](./attract-troubleshoot-linkedin.md)
