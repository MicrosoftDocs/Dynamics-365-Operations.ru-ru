---
title: "Безопасность пользователя портала поставщика"
description: "В этой статье описывается порядок настройки безопасности для внешних поставщиков, которые используют портал поставщиков. Эта информация относится только к версиям Dynamics AX от февраля 2016 г. и мая 2016 г."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f79f686720d615da6996f854a9e4cc18f840337f
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="ca4f8-104">Безопасность пользователя портала поставщика</span><span class="sxs-lookup"><span data-stu-id="ca4f8-104">Vendor portal user security</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ca4f8-105">В этой статье описывается порядок настройки безопасности для внешних поставщиков, которые используют портал поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="ca4f8-106">Эта информация относится только к версиям Dynamics AX от февраля 2016 г. и мая 2016 г.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="ca4f8-107">Функция портала поставщика была заменена расширенной функцией сотрудничества с поставщиками в Dynamics 365 for Operations версии 1611.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="ca4f8-108">Дополнительные сведения о настройке безопасности для совместной работы с поставщиками см. в разделе [Настройка и ведение сотрудничества с поставщиками](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="ca4f8-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="ca4f8-109">На портале поставщика ограниченное подмножество информации о заказах на покупку становится доступно внешним поставщикам.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="ca4f8-110">Необходимо правильно настроить разрешения пользователей в отношении портала поставщика в Microsoft Dynamics AX, чтобы поставщики случайно не получили доступ к какой-либо другой информации в вашем экземпляре Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="ca4f8-111">**Важно:** в отличие от других пользователей, внешние поставщики не должны иметь роль **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="ca4f8-112">Роль **SystemUser** обеспечивает доступ к набору привилегий, которые не подходят для внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="ca4f8-113">Настройка пользователя портала поставщика</span><span class="sxs-lookup"><span data-stu-id="ca4f8-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="ca4f8-114">Прежде чем создавать учетную запись пользователя для кого-либо, кто будет пользоваться порталом поставщика, вы должны настроить поставщика так, чтобы разрешить ему сотрудничать с вашей организацией через портал поставщика.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="ca4f8-115">Для этого используется поле **Совместная работа с заказами на покупку** на вкладке **Общее** страницы **Поставщики**.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="ca4f8-116">Внешние поставщики, которые пользуются порталом поставщика, должны быть настроены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ca4f8-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="ca4f8-117">Для поставщика должна быть зарегистрирована учетная запись пользователя Microsoft Azure Active Directory (AAD) на странице **Пользователи** в Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="ca4f8-118">Поставщик должен иметь роль безопасности **Поставщик (внешний)**, а не роль **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="ca4f8-119">**Примечание.** Роль **SystemUser** устанавливается автоматически при создании новой учетной записи пользователя в Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="ca4f8-120">Следовательно, вы должны удалить эту роль; при этом будет выведено предупреждение, с которым вам нужно будет согласиться.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="ca4f8-121">Пользователь-поставщик не следует давать разрешение на добавление дополнительных полей из таблиц заказов на покупку в то представление заказа, которое он видит.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="ca4f8-122">На вкладке **Персонализация** на вкладке **Пользователи** установите параметр **Явная персонализация разрешена** для пользователя в значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="ca4f8-123">Учетная запись пользователя должна быть связана с зарегистрированным контактным лицом.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="ca4f8-124">На странице **Пользователи** выберите контактное лицо в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="ca4f8-125">Выбранное лицо должно иметь роль **Контактное лицо** для соответствующего поставщика.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="ca4f8-126">Если одному и тому же человеку требуется доступ к порталу поставщика для нескольких учетных записей поставщиков (для разных юридических лиц, например), каждая из учетных записей пользователей этого человека должна быть связана с одним и тем же зарегистрированным контактным лицом.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="ca4f8-127">Роль **Поставщик (внешний)** включает все основные возможности, которые необходимы для использования функциональности, доступной на портале поставщика.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="ca4f8-128">Такая настройка позволяет гарантировать, что пользовательский интерфейс, который будет видеть внешний пользователь, будет ориентирован исключительно на предполагаемый сценарий его использования.</span><span class="sxs-lookup"><span data-stu-id="ca4f8-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="ca4f8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ca4f8-129">See also</span></span>
--------

[<span data-ttu-id="ca4f8-130">Совместная работа с поставщиками</span><span class="sxs-lookup"><span data-stu-id="ca4f8-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




