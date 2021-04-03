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
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477908"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="094ba-103">Создание клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="094ba-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="094ba-104">В этом разделе описывается, как создать клиента по умолчанию для использования при создании канала в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="094ba-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="094ba-105">При создании канала необходимо предоставить клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="094ba-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="094ba-106">После создания группы клиентов и адресной книги клиентов можно легко создать клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="094ba-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="094ba-107">Создание группы клиентов</span><span class="sxs-lookup"><span data-stu-id="094ba-107">Create a customer group</span></span>

<span data-ttu-id="094ba-108">Если ни одна группа клиентов еще не существует, ее можно создать.</span><span class="sxs-lookup"><span data-stu-id="094ba-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="094ba-109">Примерами могут служить группы, представляющие разные группы клиентов, такие как оптовая торговля, розница, Интернет, сотрудники и т. д.</span><span class="sxs-lookup"><span data-stu-id="094ba-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="094ba-110">Чтобы создать группу клиентов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="094ba-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="094ba-111">В области переходов выберите **Модули \> Retail и Commerce \> Клиенты \> Группы клиентов**.</span><span class="sxs-lookup"><span data-stu-id="094ba-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="094ba-112">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="094ba-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="094ba-113">В поле **Группа клиентов** введите код группы клиентов.</span><span class="sxs-lookup"><span data-stu-id="094ba-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="094ba-114">В поле **Описание** введите соответствующее описание.</span><span class="sxs-lookup"><span data-stu-id="094ba-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="094ba-115">В поле **Условия оплаты** введите соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="094ba-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="094ba-116">В поле **Время между сроком накладной и датой платежа** введите соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="094ba-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="094ba-117">В поле **Налоговая группа по умолчанию** введите налоговую группу, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="094ba-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="094ba-118">При необходимости установите флажок **Цены включают налог**.</span><span class="sxs-lookup"><span data-stu-id="094ba-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="094ba-119">В поле **Причина списания по умолчанию** введите соответствующее значение, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="094ba-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="094ba-120">На следующем рисунке показано несколько настроенных групп клиентов.</span><span class="sxs-lookup"><span data-stu-id="094ba-120">The following image shows several configured customer groups.</span></span>

![Группы клиентов](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="094ba-122">Создание адресной книги клиентов</span><span class="sxs-lookup"><span data-stu-id="094ba-122">Create a customer address book</span></span>

<span data-ttu-id="094ba-123">Клиент должен быть связан с адресной книгой.</span><span class="sxs-lookup"><span data-stu-id="094ba-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="094ba-124">Если это еще не было создано, необходимо создать его.</span><span class="sxs-lookup"><span data-stu-id="094ba-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="094ba-125">Чтобы создать адресную книгу клиентов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="094ba-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="094ba-126">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Адресные книги**.</span><span class="sxs-lookup"><span data-stu-id="094ba-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="094ba-127">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="094ba-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="094ba-128">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="094ba-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="094ba-129">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="094ba-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="094ba-130">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="094ba-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="094ba-131">На следующем рисунке показан пример адресной книги.</span><span class="sxs-lookup"><span data-stu-id="094ba-131">The following image shows an example address book.</span></span>

![Адресная книга](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="094ba-133">Создание клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="094ba-133">Create a default customer</span></span>

<span data-ttu-id="094ba-134">Чтобы клиента по умолчанию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="094ba-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="094ba-135">В области переходов выберите **Модули \> Retail и Commerce \> Клиенты \> Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="094ba-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="094ba-136">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="094ba-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="094ba-137">В раскрывающемся списке **Тип** выберите "Человек".</span><span class="sxs-lookup"><span data-stu-id="094ba-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="094ba-138">В раскрывающемся списке **Счет клиента** выберите или введите номер счета (например, "100001").</span><span class="sxs-lookup"><span data-stu-id="094ba-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="094ba-139">В раскрывающемся списке **Имя** выберите или введите имя (например, "по умолчанию").</span><span class="sxs-lookup"><span data-stu-id="094ba-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="094ba-140">В раскрывающемся списке **Отчество** выберите или введите имя (например, "розница").</span><span class="sxs-lookup"><span data-stu-id="094ba-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="094ba-141">В раскрывающемся списке **Фамилия** выберите или введите имя (например, "клиент").</span><span class="sxs-lookup"><span data-stu-id="094ba-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="094ba-142">В раскрывающемся списке **Валюта** выберите или введите валюту (например, "USD").</span><span class="sxs-lookup"><span data-stu-id="094ba-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="094ba-143">В раскрывающемся списке **Валюта** выберите группу клиентов, которая была создана ранее.</span><span class="sxs-lookup"><span data-stu-id="094ba-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="094ba-144">В раскрывающемся списке **Адресные книги** выберите существующую адресную книгу клиентов.</span><span class="sxs-lookup"><span data-stu-id="094ba-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="094ba-145">Выберите **Сохранить**, чтобы сохранить и вернуться на экран сведения о клиенте для нового клиента.</span><span class="sxs-lookup"><span data-stu-id="094ba-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="094ba-146">Нет необходимости добавлять адрес для клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="094ba-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="094ba-147">На следующем рисунке показан пример создания клиента.</span><span class="sxs-lookup"><span data-stu-id="094ba-147">The following image shows an example of customer creation.</span></span>

![Создание клиента по умолчанию](media/default-customer-creation.png)

<span data-ttu-id="094ba-149">На следующем рисунке показана конфигурация клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="094ba-149">The following image shows a default customer configuration.</span></span>

![Пример конфигурации клиента](media/default-customer-configuration1.png)

<span data-ttu-id="094ba-151">Большая часть значений по умолчанию на экране сведений клиента может остаться, но следует изменить два значения.</span><span class="sxs-lookup"><span data-stu-id="094ba-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="094ba-152">На экране сведений о клиенте разверните **Значения заказов на продажу по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="094ba-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="094ba-153">В раскрывающемся списке **Сайт** выберите или введите предварительно настроенный сайт.</span><span class="sxs-lookup"><span data-stu-id="094ba-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="094ba-154">В раскрывающемся списке **Склад** выберите предварительно настроенный склад.</span><span class="sxs-lookup"><span data-stu-id="094ba-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="094ba-155">На следующем рисунке показан пример конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="094ba-155">The following image shows an example customer configuration.</span></span>

![Пример конфигурации клиента](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="094ba-157">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="094ba-157">Additional resources</span></span>

[<span data-ttu-id="094ba-158">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="094ba-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="094ba-159">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="094ba-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
