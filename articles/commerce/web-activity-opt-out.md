---
title: Отказ от сбора событий веб-активности
description: В этом разделе объясняется, как можно разрешить посетителям вашего сайта отказаться от сбора событий веб-активности в Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791565"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="3e29c-103">Отказ от сбора событий веб-активности</span><span class="sxs-lookup"><span data-stu-id="3e29c-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="3e29c-104">В этом разделе объясняется, как предоставить клиентам возможность отказаться от сбора событий веб-активности в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3e29c-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3e29c-105">Dynamics 365 Commerce позволяет администраторам сайтов анализировать веб-активность пользователей их сайтов электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="3e29c-105">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="3e29c-106">Таким образом, они могут лучше понять, как используются их сайты, и они могут оптимизировать сайты для обеспечения улучшенного взаимодействия с пользователями и выполнения бизнес-задач.</span><span class="sxs-lookup"><span data-stu-id="3e29c-106">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="3e29c-107">Способы для администраторов реализовать функции отказа</span><span class="sxs-lookup"><span data-stu-id="3e29c-107">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="3e29c-108">У администраторов есть три способа реализации функции отказа.</span><span class="sxs-lookup"><span data-stu-id="3e29c-108">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="3e29c-109">Отказ от имени пользователей</span><span class="sxs-lookup"><span data-stu-id="3e29c-109">Opt out on behalf of users</span></span>

<span data-ttu-id="3e29c-110">В управлении учетными записями в центральном офисе Commerce (HQ), администраторы могут выполнить отказ от имени пользователей.</span><span class="sxs-lookup"><span data-stu-id="3e29c-110">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="3e29c-111">В клиенте HQ на странице **все клиенты** выполните поиск и выберите клиента.</span><span class="sxs-lookup"><span data-stu-id="3e29c-111">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="3e29c-112">На странице сведения о клиенте на экспресс-вкладке **Retail** в разделе **Безопасность** установите для параметра **не отслеживать веб-активность** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3e29c-112">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Параметры конфиденциальности](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="3e29c-114">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3e29c-114">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="3e29c-115">Функция отказа на основе модуля</span><span class="sxs-lookup"><span data-stu-id="3e29c-115">Module-based opt-out experience</span></span>

<span data-ttu-id="3e29c-116">Администраторы могут позволить прошедшим аутентификацию пользователям отказаться от сбора событий веб-активности самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="3e29c-116">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="3e29c-117">Чтобы обеспечить такой отказ, добавьте на страницы профиля учетной записи клиента модуль отказа для пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e29c-117">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="3e29c-118">Настраиваемые расширения</span><span class="sxs-lookup"><span data-stu-id="3e29c-118">Custom extensions</span></span>

<span data-ttu-id="3e29c-119">Администраторы могут создавать свои собственные расширения для управления отказами пользователей.</span><span class="sxs-lookup"><span data-stu-id="3e29c-119">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="3e29c-120">Дополнительные сведения см. в разделе [API вызова Retail Server](e-commerce-extensibility/call-retail-server-apis.md) и [Расширяемость канала продаж через Интернет](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="3e29c-120">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
