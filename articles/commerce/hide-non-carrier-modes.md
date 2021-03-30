---
title: Скрыть режимы доставки, не связанные с перевозчиком, из параметров отгрузки в POS
description: В этом разделе описывается параметр конфигурации, который позволяет предотвратить появление не связанных с перевозчиком режимов поставки для выбора, когда в приложении POS создаются заказы на отгрузку.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c06dfa697e3e0eab7a7f4183da9f178af818a6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206176"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="8ff58-103">Скрыть режимы доставки, не связанные с перевозчиком, из параметров отгрузки в POS</span><span class="sxs-lookup"><span data-stu-id="8ff58-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8ff58-104">В этом разделе описывается параметр конфигурации, который доступен для приложения POS.</span><span class="sxs-lookup"><span data-stu-id="8ff58-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="8ff58-105">Этот параметр конфигурации изменяет поведение для выбора режима доставки, когда заказы на отгрузку создаются в POS.</span><span class="sxs-lookup"><span data-stu-id="8ff58-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="8ff58-106">Когда пользователи создают заказ на отгрузку клиента в POS, они могут выбрать способ поставки для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="8ff58-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="8ff58-107">Эта функция доступна независимо от того, выполняется ли отгрузка всего заказа или только выбранных строк.</span><span class="sxs-lookup"><span data-stu-id="8ff58-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="8ff58-108">По умолчанию диалоговое окно, в котором выбран способ поставки, отображает все допустимые способы поставки для комбинации канала, номенклатуры и адреса поставки.</span><span class="sxs-lookup"><span data-stu-id="8ff58-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="8ff58-109">Эти способы поставки определяются на странице **Режимы поставки** в Headquarters (**Продажи и маркетинг \> Настройка \> Распределение \> Режимы поставки**).</span><span class="sxs-lookup"><span data-stu-id="8ff58-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="8ff58-110">Режимы поставки без перевозчика, такие как **На вынос** или **Отправка**, могут также отображаться для выбора в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="8ff58-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="8ff58-111">Однако была добавлена функция, позволяющая скрыть не относящиеся к перевозчикам режимы поставки в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="8ff58-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="8ff58-112">Чтобы включить эту функцию, на странице **Параметры Commerce** на вкладке **Заказы клиента** установите параметр **Показывать только параметры режима перевозчика для заказов на отгрузку** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="8ff58-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="8ff58-113">После включения этой функции и запуска соответствующих заданий распределения для синхронизации информации с базой данных канала не относящиеся к перевозчикам режимы поставки не отображаются для выбора в процессе создания заказов на отгрузку в POS.</span><span class="sxs-lookup"><span data-stu-id="8ff58-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]