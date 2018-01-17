---
title: "Конфигурации запросов поставщика"
description: "В этом разделе описаны поля, которые необходимо заполнить в новом запросе поставщика."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: e45f8698e69a2a870c7c00f91622216deb4cb38a
ms.contentlocale: ru-ru
ms.lasthandoff: 12/14/2017

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="4cbae-103">Конфигурации запросов поставщика</span><span class="sxs-lookup"><span data-stu-id="4cbae-103">Vendor request configurations</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="4cbae-104">Для выполнения запроса поставщика контактное лицо поставщика должно заполнить мастер регистрации потенциального поставщика.</span><span class="sxs-lookup"><span data-stu-id="4cbae-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="4cbae-105">В форме **Конфигурации запросов поставщика** можно создать профили, которые определяют обязательные поля и видимые поля в мастере регистрации потенциального поставщика.</span><span class="sxs-lookup"><span data-stu-id="4cbae-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="4cbae-106">Мастер регистрации поставщика будет начинаться с запроса у пользователя потенциального поставщика страны или региона, в которых поставщик ведет свой бизнес.</span><span class="sxs-lookup"><span data-stu-id="4cbae-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="4cbae-107">Эта информация определяет используемую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="4cbae-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="4cbae-108">Если для страны/региона не определена конкретная конфигурация, будет использоваться конфигурация по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4cbae-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="4cbae-109">Настройка конфигурации запросов поставщиков</span><span class="sxs-lookup"><span data-stu-id="4cbae-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="4cbae-110">По умолчанию имеется доступная конфигурация поставщика в форме конфигураций запроса поставщика.</span><span class="sxs-lookup"><span data-stu-id="4cbae-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="4cbae-111">Невозможно выбрать страну или регион для конфигурации по умолчанию, поэтому раздел **Страна/регион** не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="4cbae-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1.  <span data-ttu-id="4cbae-112">Щелкните **Закупки и источники** > **Настройка** > **Поставщики**, затем щелкните **Конфигурации запросов поставщика**.</span><span class="sxs-lookup"><span data-stu-id="4cbae-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="4cbae-113">Щелкните вкладку **Поля**, чтобы задать статус перечисленных полей.</span><span class="sxs-lookup"><span data-stu-id="4cbae-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
-   <span data-ttu-id="4cbae-114">Скрыто (не отображается)</span><span class="sxs-lookup"><span data-stu-id="4cbae-114">Hidden (Not visible)</span></span>
-   <span data-ttu-id="4cbae-115">Отображается (видно, но не является обязательным)</span><span class="sxs-lookup"><span data-stu-id="4cbae-115">Displayed (Visible but not mandatory)</span></span>
-   <span data-ttu-id="4cbae-116">Обязательно (видно и обязательно)</span><span class="sxs-lookup"><span data-stu-id="4cbae-116">Required (Visible and mandatory)</span></span>
3.  <span data-ttu-id="4cbae-117">Щелкните вкладку **Содержимое**, чтобы указать, будет ли отображаться текст в мастере, и требуется ли подтверждение, что пользователь потенциального поставщика должен принять этот текст перед переходом к следующему шагу в мастере.</span><span class="sxs-lookup"><span data-stu-id="4cbae-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="4cbae-118">Подтверждение будет запрашиваться для любых положений и условий, которые пользователь должен принять для продолжения.</span><span class="sxs-lookup"><span data-stu-id="4cbae-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="4cbae-119">Можно также ввести подтверждающее сообщение, которое будет отображаться, когда мастер завершен, и можно добавить одну или несколько анкет.</span><span class="sxs-lookup"><span data-stu-id="4cbae-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="4cbae-120">Создание конфигурации поставщика для определенной страны или региона</span><span class="sxs-lookup"><span data-stu-id="4cbae-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="4cbae-121">Щелкните **Закупки и источники** > **Настройка** > **Поставщики**, затем щелкните **Конфигурации запросов поставщика**.</span><span class="sxs-lookup"><span data-stu-id="4cbae-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="4cbae-122">Щелкните **Создать**, чтобы создать новую конфигурацию, и введите имя для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4cbae-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="4cbae-123">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4cbae-123">Click **Save**.</span></span>
4.  <span data-ttu-id="4cbae-124">Откройте вкладку **Страна/регионы**, чтобы выбрать страну или регион, для которых должна использоваться конфигурация.</span><span class="sxs-lookup"><span data-stu-id="4cbae-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="4cbae-125">Завершите настройку конфигурации в соответствии с инструкциями для конфигурации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4cbae-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


