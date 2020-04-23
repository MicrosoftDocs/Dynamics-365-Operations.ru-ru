---
title: Шаблоны обслуживания
description: Можно определить соглашение на обслуживание в качестве шаблона, и в дальнейшем копировать строки шаблона в другое соглашение на обслуживание или в заказ на обслуживание.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9d8ebcb2e59fae58f0701b529674cf1f9876c6b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206849"
---
# <a name="service-templates"></a><span data-ttu-id="0c00b-103">Шаблоны обслуживания</span><span class="sxs-lookup"><span data-stu-id="0c00b-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c00b-104">Можно определить соглашение на обслуживание в качестве шаблона, и в дальнейшем копировать строки шаблона в другое соглашение на обслуживание или в заказ на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0c00b-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="0c00b-105">пример</span><span class="sxs-lookup"><span data-stu-id="0c00b-105">Example</span></span>

<span data-ttu-id="0c00b-106">У обслуживаемого вами клиента существует несколько служебных лифтов в пяти различных местоположениях.</span><span class="sxs-lookup"><span data-stu-id="0c00b-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="0c00b-107">Вам необходимо настроить для данного клиента пять соглашений на обслуживание - по одному на каждое местоположение.</span><span class="sxs-lookup"><span data-stu-id="0c00b-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="0c00b-108">Чтобы сократить повторяющиеся этапы работы по настройке и обеспечить идентичность настроек соглашений на обслуживание, создается одно соглашение на обслуживание в качестве шаблона для работ по обслуживанию лифтов.</span><span class="sxs-lookup"><span data-stu-id="0c00b-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="0c00b-109">Теперь можно копировать строки шаблона в 5 новых соглашений на обслуживание таким образом, чтобы каждое соглашение на обслуживание будет заполнено строками из шаблона.</span><span class="sxs-lookup"><span data-stu-id="0c00b-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="0c00b-110">Создать шаблон</span><span class="sxs-lookup"><span data-stu-id="0c00b-110">Create a template</span></span>

<span data-ttu-id="0c00b-111">При создании шаблона обслуживания создается соглашение на обслуживание, созданные в нем требуемые строки, и присоединяется соглашение на обслуживание к группе шаблона.</span><span class="sxs-lookup"><span data-stu-id="0c00b-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="0c00b-112">Соглашение на обслуживание можно определить в качестве шаблона, только если оно не имеет приложенных заказов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0c00b-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="0c00b-113">Кроме того, ни один заказ на обслуживание не создаются из соглашения на обслуживание, которое определено в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="0c00b-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="0c00b-114">Копировать строки шаблона</span><span class="sxs-lookup"><span data-stu-id="0c00b-114">Copy template lines</span></span>

<span data-ttu-id="0c00b-115">Строки шаблона можно копировать из шаблона обслуживания в другое соглашение на обслуживание или в заказ на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0c00b-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="0c00b-116">При копировании строк шаблона в заказы на обслуживание или соглашения на обслуживание группы шаблонов отображаются в виде дерева, в котором каждая группа может быть раскрыта.</span><span class="sxs-lookup"><span data-stu-id="0c00b-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="0c00b-117">Такое представление позволяет видеть все шаблоны и строки шаблонов.</span><span class="sxs-lookup"><span data-stu-id="0c00b-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="0c00b-118">Проще определить строки шаблона, которые необходимо скопировать если вы группировали шаблоны по именам, которые отражают использование шаблонов.</span><span class="sxs-lookup"><span data-stu-id="0c00b-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c00b-119">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="0c00b-119">Related topics</span></span>

[<span data-ttu-id="0c00b-120">Копирование строк шаблонов обслуживания</span><span class="sxs-lookup"><span data-stu-id="0c00b-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
