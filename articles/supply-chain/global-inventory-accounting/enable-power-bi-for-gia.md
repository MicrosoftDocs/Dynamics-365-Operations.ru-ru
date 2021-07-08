---
title: Включение Power BI для глобального учета запасов
description: В этой теме описывается, как включить Microsoft Power BI для глобального складского учета.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273215"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="a52ab-103">Включение Power BI для глобального учета запасов</span><span class="sxs-lookup"><span data-stu-id="a52ab-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="a52ab-104">Можно закреплять плитки, панели мониторинга и отчеты из учетной записи [PowerBI.com](https://powerbi.com/) в вашей рабочей области приложения Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a52ab-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a52ab-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="a52ab-105">Prerequisites</span></span>

<span data-ttu-id="a52ab-106">Прежде чем можно будет включить отчетность Power BI, должны быть выполнены следующие условия:</span><span class="sxs-lookup"><span data-stu-id="a52ab-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="a52ab-107">Вы должны быть системным администратором в приложении Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a52ab-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="a52ab-108">Необходимо иметь учетную запись [PowerBI.com](https://powerbi.com/).</span><span class="sxs-lookup"><span data-stu-id="a52ab-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="a52ab-109">В учетной записи Power BI должна быть хотя бы одна панель мониторинга и один отчет.</span><span class="sxs-lookup"><span data-stu-id="a52ab-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="a52ab-110">Вы должны быть администратором вашей учетной записи Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="a52ab-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="a52ab-111">Домен Azure AD должен быть тем же доменом, который использовался для учетной записи [PowerBI.com](https://powerbi.com/).</span><span class="sxs-lookup"><span data-stu-id="a52ab-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="a52ab-112">Настройка</span><span class="sxs-lookup"><span data-stu-id="a52ab-112">Setup</span></span>

<span data-ttu-id="a52ab-113">Чтобы настроить интеграцию Power BI, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a52ab-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="a52ab-114">Выполните вход в [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="a52ab-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="a52ab-115">Перейдите к **библиотеке общих ресурсов**, выберите **модель отчета Power BI** в качестве типа актива и загрузите пакет **Глобальный складской учет**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="a52ab-116">Выполните вход в [PowerBI.com](https://app.powerbi.com/) и отправьте файл **Глобальный учет запасов** Power BI, выполнив следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="a52ab-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="a52ab-117">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-117">Select **New**.</span></span>
    1. <span data-ttu-id="a52ab-118">Выберите **Отправить файл**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="a52ab-119">Выберите файл отчета **Глобальный учет запасов** Power BI.</span><span class="sxs-lookup"><span data-stu-id="a52ab-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="a52ab-120">Настройте отчет **Глобальный учет запасов** Power BI, выполнив следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="a52ab-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="a52ab-121">Перейдите **Моя рабочая область**, найдите набор данных для глобального складского учета и затем в меню **Параметры** выберите **Настройки**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="a52ab-122">В **Настройки глобального учета запасов** разверните **Параметры** и обновите все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="a52ab-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="a52ab-123">Зарегистрируйте приложение, как описано в [Настройка интеграции PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="a52ab-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="a52ab-124">Интегрируйте файл отчета **Глобальный учет запасов** Power BI в Dynamics 365 Supply Chain Management, выполнив следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="a52ab-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="a52ab-125">Перейдите в раздел **Администрирование системы \> Настройка \> Конфигурация PowerBI.com**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="a52ab-126">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="a52ab-127">Выберите **Включить интеграцию PowerBI.Com**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="a52ab-128">В поле **Код приложения** введите код приложения.</span><span class="sxs-lookup"><span data-stu-id="a52ab-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="a52ab-129">В поле **Ключ приложения** введите ключ приложения.</span><span class="sxs-lookup"><span data-stu-id="a52ab-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="a52ab-130">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-130">Select **Save**.</span></span>

1. <span data-ttu-id="a52ab-131">Обновите страницу, чтобы отображалось диалоговое окно входа Power BI.</span><span class="sxs-lookup"><span data-stu-id="a52ab-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="a52ab-132">На вкладке **Параметры** выберите **Открыть каталог отчетов**, а затем выберите файл отчета **Глобальный учет запасов** Power BI, который был отправлен ранее.</span><span class="sxs-lookup"><span data-stu-id="a52ab-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="a52ab-133">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="a52ab-133">Refresh the page.</span></span> <span data-ttu-id="a52ab-134">Вы увидите, что отчет добавлен.</span><span class="sxs-lookup"><span data-stu-id="a52ab-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="a52ab-135">В **Отчеты Power BI** выберите ссылку **Глобальный учет запасов**.</span><span class="sxs-lookup"><span data-stu-id="a52ab-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="a52ab-136">Дополнительные сведения см. в разделе [Настройка интеграции PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="a52ab-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
