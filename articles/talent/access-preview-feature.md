---
title: Управление функциями
description: В этом разделе описывается, как администратор может включить функции предварительного просмотра в Microsoft Dynamics 365 Talent, и перечисляются функции, которые в настоящее время включены для предварительного просмотра.
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
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462403"
---
# <a name="manage-features"></a><span data-ttu-id="95c24-103">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="95c24-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95c24-104">В рамках нашего непрерывного процесса развертывания возможностей управление человеческим капиталом (HCM) для Microsoft Dynamics 365 Human Resources мы хотим предоставить клиентам возможность испытать новые функции.</span><span class="sxs-lookup"><span data-stu-id="95c24-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="95c24-105">Администраторы могут видеть и использовать функции предварительного просмотра в средах.</span><span class="sxs-lookup"><span data-stu-id="95c24-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="95c24-106">Общедоступная версия этих функций почти готова, и они прошли множество тестов.</span><span class="sxs-lookup"><span data-stu-id="95c24-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="95c24-107">Мы хотели бы получить окончательные отзывы клиентов и выполнить проверку до выпуска общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="95c24-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="95c24-108">В этом разделе описывается, как можно включить функции предварительного просмотра, и перечисляются функции, которые в настоящее время доступны для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="95c24-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="95c24-109">Этот список будет обновляться по мере выпуска общедоступной версии функций и выпуска новых функций для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="95c24-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="95c24-110">Уведомление не отправляется при выпуске новых функций для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="95c24-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="95c24-111">Функции просто отобразятся для пользователей.</span><span class="sxs-lookup"><span data-stu-id="95c24-111">Users will just start to see the features.</span></span> <span data-ttu-id="95c24-112">Дополнительные сведения о новых возможностях в Talent см. в разделах [Что нового и что изменилось в Dynamics 365 Talent](./whats-new.md) и [Заметки о выпуске Dynamics 365 и Power Platform](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="95c24-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="95c24-113">Включение и отключение функций предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="95c24-113">Enable or disable preview features</span></span>

<span data-ttu-id="95c24-114">Чтобы получить доступ к предварительным версиям функций, необходимо сначала включить их в своей среде.</span><span class="sxs-lookup"><span data-stu-id="95c24-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="95c24-115">Включение или отключение функций предварительного просмотра зависят от среды.</span><span class="sxs-lookup"><span data-stu-id="95c24-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95c24-116">При включении параметра **Функции предварительного просмотра** вы включаете функции предварительного просмотра для всех пользователей в организации, имеющихся в данной среде.</span><span class="sxs-lookup"><span data-stu-id="95c24-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="95c24-117">При отключении параметра вы отключаете функции предварительного просмотра и делаете их недоступными для пользователей.</span><span class="sxs-lookup"><span data-stu-id="95c24-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="95c24-118">Функции предварительного просмотра имеют ограниченную поддержку в Talent.</span><span class="sxs-lookup"><span data-stu-id="95c24-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="95c24-119">К ним могут применяться меньше требований к соблюдению конфиденциальности и безопасности, и они не включаются в соглашение об уровне обслуживания (SLA) Talent.</span><span class="sxs-lookup"><span data-stu-id="95c24-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="95c24-120">Не следует использовать функции предварительного просмотра для обработки личных данных (то есть любой информации, которая может идентифицировать пользователя) или для обработки других данных, на которые действуют юридические или нормативные требования.</span><span class="sxs-lookup"><span data-stu-id="95c24-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="95c24-121">Attract</span><span class="sxs-lookup"><span data-stu-id="95c24-121">Attract</span></span>

1. <span data-ttu-id="95c24-122">Войдите в Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="95c24-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="95c24-123">В меню **Настройка** (символ шестеренки) в правом верхнем углу выберите **Центр администрирования**.</span><span class="sxs-lookup"><span data-stu-id="95c24-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="95c24-124">На вкладке **Управление функциями** выберите вариант рядом с параметром **Функции предварительного просмотра**, чтобы он стал синим и содержат текст **Вкл.**.</span><span class="sxs-lookup"><span data-stu-id="95c24-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Включение предварительных версий функций в Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="95c24-126">Выберите или отмените выбор отдельных функций предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="95c24-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="95c24-127">Если ничего не сделать, включаются все доступные функции предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="95c24-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="95c24-128">Обновите браузер, чтобы отобразить новые функции.</span><span class="sxs-lookup"><span data-stu-id="95c24-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="95c24-129">Все пользователи, которые уже выполнили вход в систему, увидят функции при следующем входе. Также они могут обновить браузер, чтобы отобразить функции немедленно.</span><span class="sxs-lookup"><span data-stu-id="95c24-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="95c24-130">Некоторые функции предварительного просмотра могут потребовать дополнительной настройки.</span><span class="sxs-lookup"><span data-stu-id="95c24-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="95c24-131">Для завершения настройки щелкните ссылки рядом с функцией для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="95c24-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="95c24-132">Отзывы</span><span class="sxs-lookup"><span data-stu-id="95c24-132">Feedback</span></span>

<span data-ttu-id="95c24-133">Мы хотим узнать ваше мнение о вашем опыте использования любой из этих предварительных версий функций.</span><span class="sxs-lookup"><span data-stu-id="95c24-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="95c24-134">Мы рекомендуем вам регулярно публиковать отзывы об использовании этих или любых других функциях на следующих сайтах:</span><span class="sxs-lookup"><span data-stu-id="95c24-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="95c24-135">[Сообщество](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) — этот сайт является отличным ресурсом, на котором пользователи могут обсудить сценарии, задать вопросы и получить помощь сообщества.</span><span class="sxs-lookup"><span data-stu-id="95c24-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="95c24-136">Расскажите нам, какие функции вам бы хотелось увидеть в продукте, или расскажите о любых изменениях, которые, по вашему мнению, мы должны сделать в существующих функциях.</span><span class="sxs-lookup"><span data-stu-id="95c24-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="95c24-137">Предложить идеи по продуктам можно на следующих сайтах:</span><span class="sxs-lookup"><span data-stu-id="95c24-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="95c24-138">Идеи Attract</span><span class="sxs-lookup"><span data-stu-id="95c24-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="95c24-139">Идеи Onboard</span><span class="sxs-lookup"><span data-stu-id="95c24-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="95c24-140">Убедитесь, что вы не указываете личные данные (любую информацию, которая может идентифицировать пользователя) в отзыв или оценку продукта.</span><span class="sxs-lookup"><span data-stu-id="95c24-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="95c24-141">Собираемые сведения могут быть проанализированы в дальнейшем, и они не будут использоваться для ответа на запросы согласно применимым законам о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="95c24-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="95c24-142">На личные данные, собранные отдельно в рамках этих программ, распространяется [заявление о конфиденциальности Майкрософт](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="95c24-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="95c24-143">Создайте закладку для этого раздела и часто проверяйте его, чтобы оставаться в курсе новых функций предварительного просмотра по мере их выпуска.</span><span class="sxs-lookup"><span data-stu-id="95c24-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="95c24-144">См. также</span><span class="sxs-lookup"><span data-stu-id="95c24-144">See also</span></span>

- [<span data-ttu-id="95c24-145">Попробуйте или купите приложения Talent</span><span class="sxs-lookup"><span data-stu-id="95c24-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="95c24-146">Что нового и что изменилось в Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="95c24-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="95c24-147">Планы выпуска</span><span class="sxs-lookup"><span data-stu-id="95c24-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="95c24-148">Получение поддержки по Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="95c24-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
