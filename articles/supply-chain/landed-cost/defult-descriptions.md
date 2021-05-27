---
title: Описания по умолчанию для главной книги
description: Описания по умолчанию могут использоваться для обновления поля описания в разносках ваучера в главной книге.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021620"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="ec898-103">Описания по умолчанию для главной книги</span><span class="sxs-lookup"><span data-stu-id="ec898-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec898-104">Описания по умолчанию могут использоваться для обновления поля **Описание** в разносках ваучера в главной книге.</span><span class="sxs-lookup"><span data-stu-id="ec898-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="ec898-105">Эта функция была улучшена для работы со стоимостью на складе.</span><span class="sxs-lookup"><span data-stu-id="ec898-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="ec898-106">Чтобы настроить описания по умолчанию для разносок ГК, откройте **Управление организацией \> Настройка \> Описания по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="ec898-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="ec898-107">В следующей таблице перечислены новые значения, которые были добавлены в поле **Описание** на странице **Описания по умолчанию** для поддержки стоимости на складе.</span><span class="sxs-lookup"><span data-stu-id="ec898-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="ec898-108">Тип описания</span><span class="sxs-lookup"><span data-stu-id="ec898-108">Description type</span></span> | <span data-ttu-id="ec898-109">Основание</span><span class="sxs-lookup"><span data-stu-id="ec898-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="ec898-110">Импорт затрат — начисление затрат</span><span class="sxs-lookup"><span data-stu-id="ec898-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="ec898-111">При разноске накладной по заказу на покупку начисление затрат обрабатывается для оценки затрат на рейс.</span><span class="sxs-lookup"><span data-stu-id="ec898-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="ec898-112">Описания по умолчанию могут быть указаны для добавления номера рейса в описание.</span><span class="sxs-lookup"><span data-stu-id="ec898-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="ec898-113">Используйте *%4* для номера отгрузки.</span><span class="sxs-lookup"><span data-stu-id="ec898-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="ec898-114">Учет затрат на импорт — заказ товаров в пути</span><span class="sxs-lookup"><span data-stu-id="ec898-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="ec898-115">При использовании обработки в пути накладная заказа на покупку разносится, и товары разносятся на счет товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="ec898-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="ec898-116">Описания по умолчанию могут быть указаны для добавления номера заказа в пути в описание.</span><span class="sxs-lookup"><span data-stu-id="ec898-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="ec898-117">Используйте *%4* для номера заказа в пути.</span><span class="sxs-lookup"><span data-stu-id="ec898-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="ec898-118">Запасы — закрытие — коррекция</span><span class="sxs-lookup"><span data-stu-id="ec898-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="ec898-119">Когда накладная для расчетов с поставщиками (AP) обрабатывается для затрат на рейс, корректировка запасов обрабатывается для оценки затрат на рейс.</span><span class="sxs-lookup"><span data-stu-id="ec898-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="ec898-120">Описания по умолчанию могут быть указаны для добавления номера рейса в описание.</span><span class="sxs-lookup"><span data-stu-id="ec898-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="ec898-121">Используйте *%4* для номера отгрузки.</span><span class="sxs-lookup"><span data-stu-id="ec898-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="ec898-122">Дополнительные сведения о работе со страницей **Описания по умолчанию** см. в разделе [Настройка описаний по умолчанию для автоматической разноски](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="ec898-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
