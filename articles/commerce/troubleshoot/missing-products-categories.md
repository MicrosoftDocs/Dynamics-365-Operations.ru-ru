---
title: Продукты и категории отсутствуют после копирования среды
description: В этом разделе приведены инструкции по устранению неполадок, которые могут помочь при отсутствии продуктов и категорий после копирования сайта между средами или в рамках одной и той же среды.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585509"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="0b589-103">Продукты и категории отсутствуют после копирования среды</span><span class="sxs-lookup"><span data-stu-id="0b589-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b589-104">В этом разделе приведены инструкции по устранению неполадок, которые могут помочь при отсутствии продуктов и категорий после копирования сайта между средами или в рамках одной и той же среды.</span><span class="sxs-lookup"><span data-stu-id="0b589-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="0b589-105">описание</span><span class="sxs-lookup"><span data-stu-id="0b589-105">Description</span></span>

<span data-ttu-id="0b589-106">После копирования сайта из одной среды в другую или в рамках той же среды продукты и категории на сайте отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0b589-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="0b589-107">Продукты и категории будут отсутствовать в витрине электронной коммерции и на вкладке **продукты** в конструкторе сайтов Commerce.</span><span class="sxs-lookup"><span data-stu-id="0b589-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="0b589-108">Приказ</span><span class="sxs-lookup"><span data-stu-id="0b589-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="0b589-109">Сопоставьте номер операционной единицы канала с новым скопированным сайтом в конструкторе сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="0b589-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="0b589-110">Чтобы сопоставить номер операционной единицы канала (OUN) с новым скопированным сайтом в конструкторе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b589-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0b589-111">Выберите недавно скопированный сайт.</span><span class="sxs-lookup"><span data-stu-id="0b589-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="0b589-112">В **Параметры сайта** выберите **Каналы**.</span><span class="sxs-lookup"><span data-stu-id="0b589-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="0b589-113">Рядом с названием канала выберите многоточие (**...**), а затем выберите **Изменить канал интернет-магазина**.</span><span class="sxs-lookup"><span data-stu-id="0b589-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="0b589-114">В диалоговом окне **Изменить канал интернет-магазина** выберите канал, который необходимо сопоставить с новым скопированным сайтом, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0b589-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="0b589-115">Выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="0b589-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b589-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0b589-116">Additional resources</span></span>

[<span data-ttu-id="0b589-117">Связывание сайта Dynamics 365 Commerce с интернет-каналом</span><span class="sxs-lookup"><span data-stu-id="0b589-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)