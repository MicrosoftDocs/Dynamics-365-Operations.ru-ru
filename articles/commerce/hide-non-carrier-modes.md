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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 75e7e8f183982f7829db78eb75b8c29c9ab95e89
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023876"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="cd8b0-103">Скрыть режимы доставки, не связанные с перевозчиком, из параметров отгрузки в POS</span><span class="sxs-lookup"><span data-stu-id="cd8b0-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cd8b0-104">В этом разделе описывается параметр конфигурации, который доступен для приложения POS.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="cd8b0-105">Этот параметр конфигурации изменяет поведение для выбора режима доставки, когда заказы на отгрузку создаются в POS.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="cd8b0-106">Когда пользователи создают заказ на отгрузку клиента в POS, они могут выбрать способ поставки для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="cd8b0-107">Эта функция доступна независимо от того, выполняется ли отгрузка всего заказа или только выбранных строк.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="cd8b0-108">По умолчанию диалоговое окно, в котором выбран способ поставки, отображает все допустимые способы поставки для комбинации канала, номенклатуры и адреса поставки.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="cd8b0-109">Эти способы поставки определяются на странице **Режимы поставки** в Headquarters (**Продажи и маркетинг \> Настройка \> Распределение \> Режимы поставки**).</span><span class="sxs-lookup"><span data-stu-id="cd8b0-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="cd8b0-110">Режимы поставки без перевозчика, такие как **На вынос** или **Отправка**, могут также отображаться для выбора в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="cd8b0-111">Однако была добавлена функция, позволяющая скрыть не относящиеся к перевозчикам режимы поставки в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="cd8b0-112">Чтобы включить эту функцию, на странице **Параметры Commerce** на вкладке **Заказы клиента** установите параметр **Показывать только параметры режима перевозчика для заказов на отгрузку** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="cd8b0-113">После включения этой функции и запуска соответствующих заданий распределения для синхронизации информации с базой данных канала не относящиеся к перевозчикам режимы поставки не отображаются для выбора в процессе создания заказов на отгрузку в POS.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
