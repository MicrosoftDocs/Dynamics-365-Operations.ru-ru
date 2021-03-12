---
title: Вопросы и ответы по клиенту
description: Эта статья дает ответы на часто задаваемые вопросы о клиенте Finance and Operations.
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fe6da2575b7de866de614ad399c8ad5c0110d9a
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798507"
---
# <a name="client-faq"></a><span data-ttu-id="7e351-103">Вопросы и ответы по клиенту</span><span class="sxs-lookup"><span data-stu-id="7e351-103">Client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e351-104">Эта статья дает ответы на часто задаваемые вопросы о клиенте Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7e351-104">This article provides answers to frequently asked questions about the Finance and Operations client.</span></span>

## <a name="why-arent-symbols-loaded"></a><span data-ttu-id="7e351-105">Почему не загружены символы?</span><span class="sxs-lookup"><span data-stu-id="7e351-105">Why aren't symbols loaded?</span></span>

<span data-ttu-id="7e351-106">Параметры безопасности в вашем браузере могут стать причиной неправильной загрузки символов.</span><span class="sxs-lookup"><span data-stu-id="7e351-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="7e351-107">Чтобы решить эту проблему, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e351-107">To resolve this issue, try the following steps:</span></span>

- <span data-ttu-id="7e351-108">При возникновении этой проблемы в обозревателе Internet Explorer щелкните **Сервис**, затем щелкните **Свойства браузера**.</span><span class="sxs-lookup"><span data-stu-id="7e351-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span> <span data-ttu-id="7e351-109">В диалоговом окне свойств обозревателя на вкладке **Безопасность** щелкните **Другой** и убедитесь, что выбран параметр **Скачивание шрифта**.</span><span class="sxs-lookup"><span data-stu-id="7e351-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
- <span data-ttu-id="7e351-110">В противном случае может потребоваться добавить сайт приложения в список доверенных сайтов.</span><span class="sxs-lookup"><span data-stu-id="7e351-110">Otherwise, you might have to add the app site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="7e351-111">Мне не хватает ленты из Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="7e351-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="7e351-112">Можно ли сделать так, чтобы вкладки панели действий всегда были открыты?</span><span class="sxs-lookup"><span data-stu-id="7e351-112">Can I keep Action Pane tabs open all the time?</span></span>

<span data-ttu-id="7e351-113">Мы планируем реализовать эту функцию в скором времени.</span><span class="sxs-lookup"><span data-stu-id="7e351-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="7e351-114">После этого пользователи смогут оставлять вкладки области действий открытыми все время.</span><span class="sxs-lookup"><span data-stu-id="7e351-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="7e351-115">В противном случае вкладки будут сворачиваться, когда не используются, чтобы предоставить больше пространства экрана для страницы.</span><span class="sxs-lookup"><span data-stu-id="7e351-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="7e351-116">Почему иногда отображаются различные меню при щелчке правой кнопкой мыши?</span><span class="sxs-lookup"><span data-stu-id="7e351-116">Why do I sometimes see different shortcut menus when I right click?</span></span>

<span data-ttu-id="7e351-117">При щелчке редактируемого поля правой кнопкой мыши (или при выборе текста) отображается контекстное меню браузера.</span><span class="sxs-lookup"><span data-stu-id="7e351-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="7e351-118">Это меню предоставляет доступ к командам **Вырезать**, **Копировать** и **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="7e351-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="7e351-119">Мы не можем встроить эти команды в контекстные меню, поскольку из соображений безопасности браузеры не позволяют получать доступ к буферу обмена системы программным способом.</span><span class="sxs-lookup"><span data-stu-id="7e351-119">We can't embed these commands into the shortcut menus because, for security reasons, browsers don't allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="7e351-120">Если щелкнуть правой кнопкой мыши ярлык поля или значение доступного только для чтения элемента управления, отобразится контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="7e351-120">If you right-click a field label or the value of a read-only control, you'll see the shortcut menu.</span></span>

<span data-ttu-id="7e351-121">Чтобы упростить доступ с клавиатуры, мы планируем реализовать сочетание клавиш в будущем, при нажатии которого будет открываться контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="7e351-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality"></a><span data-ttu-id="7e351-122">Где находится функция "Просмотр сведений"?</span><span class="sxs-lookup"><span data-stu-id="7e351-122">Where is the View details functionality?</span></span>

<span data-ttu-id="7e351-123">Параметр **Просмотр сведений** доступен в нескольких местах:</span><span class="sxs-lookup"><span data-stu-id="7e351-123">The **View details** option is available in a couple of ways:</span></span>

- <span data-ttu-id="7e351-124">Если элемент управления имеет возможности **Просмотр сведений** и если элемент управление имеет значение, то это значение отображается как гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="7e351-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="7e351-125">Можно перейти по гиперссылке, чтобы открыть страницу, которая содержит дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7e351-125">You can click the hyperlink to open a page that contains additional details.</span></span>
- <span data-ttu-id="7e351-126">**Просмотр сведений** также является параметром в контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="7e351-126">**View details** is also an option on shortcut menus.</span></span> <span data-ttu-id="7e351-127">Дополнительные сведения о том, когда отображаются контекстные меню при щелчке правой кнопкой мыши, см. в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="7e351-127">For more information about when shortcut menus are displayed when you right-click, see the previous section.</span></span>
