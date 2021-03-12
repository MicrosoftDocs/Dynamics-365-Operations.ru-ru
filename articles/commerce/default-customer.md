---
title: Создание клиента по умолчанию
description: В этом разделе описывается, как создать клиента по умолчанию для использования при создании канала в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1dd4dfc5b8ca7af66941d081b4c20be0f5d6001d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993408"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="56390-103">Создание клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="56390-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="56390-104">В этом разделе описывается, как создать клиента по умолчанию для использования при создании канала в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="56390-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="56390-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="56390-105">Overview</span></span>

<span data-ttu-id="56390-106">При создании канала необходимо предоставить клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56390-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="56390-107">После создания группы клиентов и адресной книги клиентов можно легко создать клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56390-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="56390-108">Создание группы клиентов</span><span class="sxs-lookup"><span data-stu-id="56390-108">Create a customer group</span></span>

<span data-ttu-id="56390-109">Если ни одна группа клиентов еще не существует, ее можно создать.</span><span class="sxs-lookup"><span data-stu-id="56390-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="56390-110">Примерами могут служить группы, представляющие разные группы клиентов, такие как оптовая торговля, розница, Интернет, сотрудники и т. д.</span><span class="sxs-lookup"><span data-stu-id="56390-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="56390-111">Чтобы создать группу клиентов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="56390-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="56390-112">В области переходов выберите **Модули \> Retail и Commerce \> Клиенты \> Группы клиентов**.</span><span class="sxs-lookup"><span data-stu-id="56390-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="56390-113">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="56390-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="56390-114">В поле **Группа клиентов** введите код группы клиентов.</span><span class="sxs-lookup"><span data-stu-id="56390-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="56390-115">В поле **Описание** введите соответствующее описание.</span><span class="sxs-lookup"><span data-stu-id="56390-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="56390-116">В поле **Условия оплаты** введите соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="56390-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="56390-117">В поле **Время между сроком накладной и датой платежа** введите соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="56390-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="56390-118">В поле **Налоговая группа по умолчанию** введите налоговую группу, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="56390-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="56390-119">При необходимости установите флажок **Цены включают налог**.</span><span class="sxs-lookup"><span data-stu-id="56390-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="56390-120">В поле **Причина списания по умолчанию** введите соответствующее значение, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="56390-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="56390-121">На следующем рисунке показано несколько настроенных групп клиентов.</span><span class="sxs-lookup"><span data-stu-id="56390-121">The following image shows several configured customer groups.</span></span>

![Группы клиентов](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="56390-123">Создание адресной книги клиентов</span><span class="sxs-lookup"><span data-stu-id="56390-123">Create a customer address book</span></span>

<span data-ttu-id="56390-124">Клиент должен быть связан с адресной книгой.</span><span class="sxs-lookup"><span data-stu-id="56390-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="56390-125">Если это еще не было создано, необходимо создать его.</span><span class="sxs-lookup"><span data-stu-id="56390-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="56390-126">Чтобы создать адресную книгу клиентов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="56390-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="56390-127">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Адресные книги**.</span><span class="sxs-lookup"><span data-stu-id="56390-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="56390-128">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="56390-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="56390-129">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="56390-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="56390-130">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="56390-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="56390-131">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="56390-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="56390-132">На следующем рисунке показан пример адресной книги.</span><span class="sxs-lookup"><span data-stu-id="56390-132">The following image shows an example address book.</span></span>

![Адресная книга](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="56390-134">Создание клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="56390-134">Create a default customer</span></span>

<span data-ttu-id="56390-135">Чтобы клиента по умолчанию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="56390-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="56390-136">В области переходов выберите **Модули \> Retail и Commerce \> Клиенты \> Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="56390-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="56390-137">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="56390-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="56390-138">В раскрывающемся списке **Тип** выберите "Человек".</span><span class="sxs-lookup"><span data-stu-id="56390-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="56390-139">В раскрывающемся списке **Счет клиента** выберите или введите номер счета (например, "100001").</span><span class="sxs-lookup"><span data-stu-id="56390-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="56390-140">В раскрывающемся списке **Имя** выберите или введите имя (например, "по умолчанию").</span><span class="sxs-lookup"><span data-stu-id="56390-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="56390-141">В раскрывающемся списке **Отчество** выберите или введите имя (например, "розница").</span><span class="sxs-lookup"><span data-stu-id="56390-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="56390-142">В раскрывающемся списке **Фамилия** выберите или введите имя (например, "клиент").</span><span class="sxs-lookup"><span data-stu-id="56390-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="56390-143">В раскрывающемся списке **Валюта** выберите или введите валюту (например, "USD").</span><span class="sxs-lookup"><span data-stu-id="56390-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="56390-144">В раскрывающемся списке **Валюта** выберите группу клиентов, которая была создана ранее.</span><span class="sxs-lookup"><span data-stu-id="56390-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="56390-145">В раскрывающемся списке **Адресные книги** выберите существующую адресную книгу клиентов.</span><span class="sxs-lookup"><span data-stu-id="56390-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="56390-146">Выберите **Сохранить**, чтобы сохранить и вернуться на экран сведения о клиенте для нового клиента.</span><span class="sxs-lookup"><span data-stu-id="56390-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="56390-147">Нет необходимости добавлять адрес для клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56390-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="56390-148">На следующем рисунке показан пример создания клиента.</span><span class="sxs-lookup"><span data-stu-id="56390-148">The following image shows an example of customer creation.</span></span>

![Создание клиента по умолчанию](media/default-customer-creation.png)

<span data-ttu-id="56390-150">На следующем рисунке показана конфигурация клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56390-150">The following image shows a default customer configuration.</span></span>

![Пример конфигурации клиента](media/default-customer-configuration1.png)

<span data-ttu-id="56390-152">Большая часть значений по умолчанию на экране сведений клиента может остаться, но следует изменить два значения.</span><span class="sxs-lookup"><span data-stu-id="56390-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="56390-153">На экране сведений о клиенте разверните **Значения заказов на продажу по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="56390-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="56390-154">В раскрывающемся списке **Сайт** выберите или введите предварительно настроенный сайт.</span><span class="sxs-lookup"><span data-stu-id="56390-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="56390-155">В раскрывающемся списке **Склад** выберите предварительно настроенный склад.</span><span class="sxs-lookup"><span data-stu-id="56390-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="56390-156">На следующем рисунке показан пример конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="56390-156">The following image shows an example customer configuration.</span></span>

![Пример конфигурации клиента](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="56390-158">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="56390-158">Additional resources</span></span>

[<span data-ttu-id="56390-159">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="56390-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="56390-160">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="56390-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
