---
title: Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent - Attract
description: В этой теме объясняется, как настроить интеграцию с LinkedIn для Microsoft Dynamics 365 Talent - Attract, чтобы можно было легко публиковать объявления о вакансиях в LinkedIn из Attract, а также для того, чтобы ваши специалисты по найму на работу могли синхронизировать свои сведения о наборе сотрудников с профилем LinkedIn кандидата.
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
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6b86cafdf364f2de051f3d8ceab7413c2c13c3a5
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009978"
---
# <a name="set-up-linkedin-integration"></a>Настройка интеграции с LinkedIn

[!include[banner](../includes/banner.md)]

Помогите специалистам по найму персонала и менеджерам по найму привлекать лучшие кадры, настроив интеграцию LinkedIn с Microsoft Dynamics 365 Talent: Attract. С помощью Attract можно размещать объявления о вакансиях непосредственно в LinkedIn, в самой крупной профессиональной сети в Интернете.

Вакансии, которые размещаются в LinkedIn с помощью Attract, размещаются в ограниченных списках и не требуют дополнительных затрат от вашей компании. Эти списки доступны только через партнеров программного обеспечения LinkedIn, таких как Attract. Они не отображаются в панели **Вакансии** на странице LinkedIn вашей компании, поскольку там отображаются только оплаченные списки. Однако они отображаются, когда потенциальные кандидаты просматривают все доступные вакансии. Ограниченные списки также отображаются в результатах поиска вакансий в LinkedIn.

Attract предоставляет два способа интеграции с LinkedIn, помогая искать кандидатов на этом популярном сайте карьеры:

- Публикация вакансий из Attract в LinkedIn.
- Перенос кандидатов из LinkedIn в Attract.

Можно настроить оба варианта на вкладке **Интеграция с LinkedIn** в центре администрирования. Чтобы открыть центр администрирования, выберите <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> Чтобы использовать интеграцию LinkedIn Recruiter с Attract, требуются [надстройка Comprehensive Hiring](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) и [лицензии LinkedIn Recruiter](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Для получения дополнительных сведений см. раздел [Какая версия Attract?](./attract-comprehensive-hiring.md).

Если вы не можете опубликовать объявления о вакансиях в LinkedIn, см. раздел [Устранение неполадок интеграции с LinkedIn](./attract-troubleshoot-linkedin.md).

Сведения о других способах публикации вакансий в LinkedIn см. в разделе [Вопросы и ответы по LinkedIn](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Настройка публикации объявлений о вакансиях в LinkedIn

Прежде чем можно будет размещать объявления о вакансиях из Attract в LinkedIn, необходим [код компании LinkedIn](https://aka.ms/findID). Ваш код компании LinkedIn — это строка чисел, которая уникально идентифицирует вашу компанию в LinkedIn. Дополнительные сведения см. в разделе [Назначение кода компании LinkedIn с доской вакансий LinkedIn — часто задаваемые вопросы](https://aka.ms/findID).

Attract посылает канал объявлений о вакансиях в LinkedIn, и LinkedIn выполняет проверку канала примерно один раз в день. Размещение объявлений о вакансиях на сайте может занять до 48 часов

Вакансии, опубликованные в LinkedIn, отображаются на действующем сайте LinkedIn. В LinkedIn отсутствует тестовая среда для публикации вакансий. Таким образом, следите, чтобы случайно не опубликовать тестовые объявления о вакансиях. 

1. В меню **Настройка** (символ шестеренки) в правом верхнем углу выберите **Центр администрирования**. В качестве альтернативы перейдите к <https://attract.talent.dynamics.com/adminsettings>.
2. Перейдите на вкладку **Интеграция LinkedIn**.
3. В поле **Название компании** введите название компании, затем в поле **Код компании** введите свой код компании LinkedIn. Убедитесь, что название компании соответствует имени, которое отображается на странице LinkedIn компании. Дополнительные сведения о кодах компании LinkedIn см. в разделе [Назначение кода компании LinkedIn с доской вакансий LinkedIn — часто задаваемые вопросы](https://www.linkedin.com/help/linkedin/answer/98972).

    Если требуется изменить какие-либо сведения для организации, см. раздел [Изменение адреса организации, технического контакта и т. д.](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Если неполадки остались, обратитесь [в службу поддержки LinkedIn](https://www.linkedin.com/help/linkedin).

4. Нажмите **Сохранить**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Настройка LinkedIn Recruiter с Attract 

Чтобы разрешить специалистам по найму получать вакансии через LinkedIn Recruiter, необходимо настроить интеграцию LinkedIn Recruiter в Attract. Чтобы завершить процесс настройки, необходимо работать с пользователем, который является администратором контракта LinkedIn Recruiter вашей организации.

1. В меню **Настройка** (символ шестеренки) в правом верхнем углу выберите **Центр администрирования**. В качестве альтернативы перейдите к <https://attract.talent.dynamics.com/adminsettings>.
2. Перейдите на вкладку **Интеграция LinkedIn**.

    [![Представление администратора Attract для запуска интеграции LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Выберите **Подключить** для запуска настройки. Вы получите пошаговые инструкции по процессу входа в LinkedIn.
4. При наличии мест в нескольких контрактах LinkedIn выберите контракт, который вы хотите подключить к системе Attract. Если имеется место в единственном контракте LinkedIn, этот шаг можно пропустить.
5. В разделе **Recruiter System Connect (RSC)** выберите **Запросить**.

    [![Представление администратора Attract для запроса интеграции LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. Теперь параметр **Recruiter System Connect (RSC)** будет отображаться как **Партнер готов**. Если на этой странице отображается сообщение **Уведомить партнера**, подождите несколько секунд, выберите **Уведомить партнера**, затем обновите эту страницу. Теперь настройка должна отображаться как **Партнер готов**.

    [![Представление администратора Attract для индикации, что запросы со стороны Attract выполнены](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Для выполнения следующих шагов необходимо иметь права администратора контракта LinkedIn Recruiter.

    1. Выполните вход в LinkedIn с учетной записью администратора, затем выберите **LinkedIn Recruiter** в правом верхнем углу. 
    2. В меню **Дополнительно** в верхней части страницы выберите **Параметры администратора**, затем выберите вкладку **ATS**.
    3. Чтобы разрешить экспорт одним щелчком только для одного контракта, следует включить **Доступ на уровне контракта (для каждого рабочего места в этом контракте)**. Чтобы включить его для всей компании, включите **Доступ на уровне компании (для каждого контракта в компании)**.

    [![Включение интеграции Attract из представления администратора LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

8. В центре администрирования выберите вкладку **Интеграция LinkedIn**. Параметр **Recruiter System Connect (RSC)** теперь должен отображаться как **Включено**.

    [![Интеграция LinkedIn Recruiter завершена](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Настройка "Подать заявление с помощью LinkedIn" в Attract

Можно разрешить кандидатам подавать заявление на должности, используя профили LinkedIn. Дополнительные сведения о подаче заявлений с помощью LinkedIn см. в разделе [Безграничные возможности LinkedIn: подача заявления с помощью LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Эта функция в данный момент находится в режиме предварительного просмотра. Перед выполнением этих действий убедитесь, что подача заявления с помощью LinkedIn включена. Дополнительные сведения о порядке включении предварительных версий функций см. в разделе [Доступ к функциям предварительного просмотра в Talent](./access-preview-feature.md).

1. В меню **Настройка** (символ шестеренки) в правом верхнем углу выберите **Центр администрирования**. В качестве альтернативы перейдите к <https://attract.talent.dynamics.com/adminsettings>.
2. Перейдите на вкладку **Интеграция LinkedIn**.

    [![Представление администратора Attract для запуска интеграции LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Рядом с пунктом **Подача заявлений с помощью LinkedIn** выберите **Подключить** для запуска настройки. Вы получите пошаговые инструкции по остальной части процесса в LinkedIn.

## <a name="see-also"></a>См. также

[Вопросы и ответы по LinkedIn](./attract-linkedin-faq.md)

[Публикация вакансий на внешних сайтах из Attract](./posting-jobs-external.md)

[Поиск кандидатов с помощью LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[Создание вакансий](./creating-jobs-attract.md)

[Устранение неполадок интеграции с LinkedIn](./attract-troubleshoot-linkedin.md)
