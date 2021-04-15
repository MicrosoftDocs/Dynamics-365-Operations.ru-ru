---
title: Создание клиента по умолчанию
description: В этом разделе описывается, как создать клиента по умолчанию для использования при создании канала в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799187"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="20d8c-103">Создание клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="20d8c-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="20d8c-104">В этом разделе описывается, как создать клиента по умолчанию для использования при создании канала в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="20d8c-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="20d8c-105">При создании канала необходимо предоставить клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20d8c-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="20d8c-106">После создания группы клиентов и адресной книги клиентов можно легко создать клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20d8c-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="20d8c-107">Создание группы клиентов</span><span class="sxs-lookup"><span data-stu-id="20d8c-107">Create a customer group</span></span>

<span data-ttu-id="20d8c-108">Если ни одна группа клиентов еще не существует, ее можно создать.</span><span class="sxs-lookup"><span data-stu-id="20d8c-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="20d8c-109">Примерами могут служить группы, представляющие разные группы клиентов, такие как оптовая торговля, розница, Интернет, сотрудники и т. д.</span><span class="sxs-lookup"><span data-stu-id="20d8c-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="20d8c-110">Чтобы создать группу клиентов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="20d8c-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="20d8c-111">В области переходов выберите **Модули \> Retail и Commerce \> Клиенты \> Группы клиентов**.</span><span class="sxs-lookup"><span data-stu-id="20d8c-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="20d8c-112">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="20d8c-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="20d8c-113">В поле **Группа клиентов** введите код группы клиентов.</span><span class="sxs-lookup"><span data-stu-id="20d8c-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="20d8c-114">В поле **Описание** введите соответствующее описание.</span><span class="sxs-lookup"><span data-stu-id="20d8c-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="20d8c-115">В поле **Условия оплаты** введите соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="20d8c-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="20d8c-116">В поле **Время между сроком накладной и датой платежа** введите соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="20d8c-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="20d8c-117">В поле **Налоговая группа по умолчанию** введите налоговую группу, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="20d8c-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="20d8c-118">При необходимости установите флажок **Цены включают налог**.</span><span class="sxs-lookup"><span data-stu-id="20d8c-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="20d8c-119">В поле **Причина списания по умолчанию** введите соответствующее значение, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="20d8c-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="20d8c-120">На следующем рисунке показано несколько настроенных групп клиентов.</span><span class="sxs-lookup"><span data-stu-id="20d8c-120">The following image shows several configured customer groups.</span></span>

![Группы клиентов](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="20d8c-122">Создание адресной книги клиентов</span><span class="sxs-lookup"><span data-stu-id="20d8c-122">Create a customer address book</span></span>

<span data-ttu-id="20d8c-123">Клиент должен быть связан с адресной книгой.</span><span class="sxs-lookup"><span data-stu-id="20d8c-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="20d8c-124">Если это еще не было создано, необходимо создать его.</span><span class="sxs-lookup"><span data-stu-id="20d8c-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="20d8c-125">Чтобы создать адресную книгу клиентов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="20d8c-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="20d8c-126">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Адресные книги**.</span><span class="sxs-lookup"><span data-stu-id="20d8c-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="20d8c-127">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="20d8c-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="20d8c-128">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="20d8c-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="20d8c-129">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="20d8c-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="20d8c-130">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="20d8c-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="20d8c-131">На следующем рисунке показан пример адресной книги.</span><span class="sxs-lookup"><span data-stu-id="20d8c-131">The following image shows an example address book.</span></span>

![Адресная книга](media/address-book.png)

## <a name="create-a-default-customer&quot;></a><span data-ttu-id=&quot;20d8c-133&quot;>Создание клиента по умолчанию</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;20d8c-133&quot;>Create a default customer</span></span>

<span data-ttu-id=&quot;20d8c-134&quot;>Чтобы клиента по умолчанию, выполните следующие действия.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;20d8c-134&quot;>To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id=&quot;20d8c-135&quot;>В области переходов выберите **Модули \> Retail и Commerce \> Клиенты \> Все клиенты**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;20d8c-135&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id=&quot;20d8c-136&quot;>В области действий выберите **Создать**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;20d8c-136&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;20d8c-137&quot;>В раскрывающемся списке **Тип** выберите &quot;Человек&quot;.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;20d8c-137&quot;>In the **Type** drop-down list, select &quot;Person&quot;.</span></span>
1. <span data-ttu-id=&quot;20d8c-138&quot;>В раскрывающемся списке **Счет клиента** выберите или введите номер счета (например, &quot;100001").</span><span class="sxs-lookup"><span data-stu-id="20d8c-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="20d8c-139">В раскрывающемся списке **Имя** выберите или введите имя (например, "по умолчанию").</span><span class="sxs-lookup"><span data-stu-id="20d8c-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="20d8c-140">В раскрывающемся списке **Отчество** выберите или введите имя (например, "розница").</span><span class="sxs-lookup"><span data-stu-id="20d8c-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="20d8c-141">В раскрывающемся списке **Фамилия** выберите или введите имя (например, "клиент").</span><span class="sxs-lookup"><span data-stu-id="20d8c-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="20d8c-142">В раскрывающемся списке **Валюта** выберите или введите валюту (например, "USD").</span><span class="sxs-lookup"><span data-stu-id="20d8c-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="20d8c-143">В раскрывающемся списке **Валюта** выберите группу клиентов, которая была создана ранее.</span><span class="sxs-lookup"><span data-stu-id="20d8c-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="20d8c-144">В раскрывающемся списке **Адресные книги** выберите существующую адресную книгу клиентов.</span><span class="sxs-lookup"><span data-stu-id="20d8c-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="20d8c-145">Выберите **Сохранить**, чтобы сохранить и вернуться на экран сведения о клиенте для нового клиента.</span><span class="sxs-lookup"><span data-stu-id="20d8c-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="20d8c-146">Нет необходимости добавлять адрес для клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20d8c-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="20d8c-147">На следующем рисунке показан пример создания клиента.</span><span class="sxs-lookup"><span data-stu-id="20d8c-147">The following image shows an example of customer creation.</span></span>

![Создание клиента по умолчанию](media/default-customer-creation.png)

<span data-ttu-id="20d8c-149">На следующем рисунке показана конфигурация клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20d8c-149">The following image shows a default customer configuration.</span></span>

![Пример конфигурации клиента](media/default-customer-configuration1.png)

<span data-ttu-id="20d8c-151">Большая часть значений по умолчанию на экране сведений клиента может остаться, но следует изменить два значения.</span><span class="sxs-lookup"><span data-stu-id="20d8c-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="20d8c-152">На экране сведений о клиенте разверните **Значения заказов на продажу по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="20d8c-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="20d8c-153">В раскрывающемся списке **Сайт** выберите или введите предварительно настроенный сайт.</span><span class="sxs-lookup"><span data-stu-id="20d8c-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="20d8c-154">В раскрывающемся списке **Склад** выберите предварительно настроенный склад.</span><span class="sxs-lookup"><span data-stu-id="20d8c-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="20d8c-155">На следующем рисунке показан пример конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="20d8c-155">The following image shows an example customer configuration.</span></span>

![Пример конфигурации клиента](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="20d8c-157">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="20d8c-157">Additional resources</span></span>

[<span data-ttu-id="20d8c-158">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="20d8c-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="20d8c-159">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="20d8c-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
