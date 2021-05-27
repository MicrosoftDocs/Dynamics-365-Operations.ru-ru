---
title: Невозможно применение шаблона к выпущенному продукту
description: Невозможно применить шаблон к выпущенному продукту.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026840"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="ca877-103">Невозможно применить шаблон, чтобы создать выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="ca877-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="ca877-104">Номер статьи базы знаний: 4612097</span><span class="sxs-lookup"><span data-stu-id="ca877-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="ca877-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="ca877-105">Symptoms</span></span>

<span data-ttu-id="ca877-106">При создании нового запущенного продукта с помощью диалогового окна **Новый выпущенный продукт** можно выбрать шаблон.</span><span class="sxs-lookup"><span data-stu-id="ca877-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="ca877-107">Шаблон должен предоставлять настройки по умолчанию для многих полей нового выпущенного продукта.</span><span class="sxs-lookup"><span data-stu-id="ca877-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="ca877-108">Однако некоторые или все поля не настраиваются после выбора шаблона.</span><span class="sxs-lookup"><span data-stu-id="ca877-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="ca877-109">Причина</span><span class="sxs-lookup"><span data-stu-id="ca877-109">Cause</span></span>

<span data-ttu-id="ca877-110">Многие страницы в Microsoft Dynamics 365 Supply Chain Management позволяют создать шаблон, который устанавливает исходные настройки для записей, отображаемых на этих страницах.</span><span class="sxs-lookup"><span data-stu-id="ca877-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="ca877-111">Можно создать один из этих шаблонов, выбрав **Сведения о записи** на вкладке **Параметры** панели операций.</span><span class="sxs-lookup"><span data-stu-id="ca877-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="ca877-112">Однако выпущенные продукты значительно сложнее большинства других типов записей.</span><span class="sxs-lookup"><span data-stu-id="ca877-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="ca877-113">Хотя можно выбрать **Сведения о записи** на странице **Выпущенные продукты** для создания шаблона и хотя этот шаблон можно выбрать при создании выпущенного продукта, шаблон не будет предоставлять ожидаемые значения полей для нового выпущенного продукта.</span><span class="sxs-lookup"><span data-stu-id="ca877-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="ca877-114">Таким образом, нельзя использовать шаблоны "сведения о записи" для выпущенных продуктов.</span><span class="sxs-lookup"><span data-stu-id="ca877-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="ca877-115">Вместо этого необходимо создать специальные шаблоны продуктов.</span><span class="sxs-lookup"><span data-stu-id="ca877-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="ca877-116">Приказ</span><span class="sxs-lookup"><span data-stu-id="ca877-116">Resolution</span></span>

<span data-ttu-id="ca877-117">Чтобы создать шаблон продукта, воспользуйтесь меню **Шаблон** на вкладке **Продукт** панели операций, а не кнопкой **Сведения о записи** на вкладке **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="ca877-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="ca877-118">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="ca877-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ca877-119">На панели операций на вкладке **Продукт** в группе **Создать** выберите **Шаблон**, а затем выберите вариант **Создать личный шаблон** или **Создать общий шаблон**, как необходимо.</span><span class="sxs-lookup"><span data-stu-id="ca877-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
