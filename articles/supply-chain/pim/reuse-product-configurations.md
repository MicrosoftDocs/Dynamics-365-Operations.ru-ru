---
title: "Повторное использование конфигураций продуктов"
description: "Можно указать, что требуется автоматически повторно использовать существующую конфигурацию продукта. Затем, когда пользователь завершает сеанс настройки, система проверяет, не существует ли имеющейся конфигурации, которая соответствует выбору пользователя. Если такая конфигурация найдена, используются ИД конфигурации, соответствующая спецификация и маршрут."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: b4d61c869577a3e18d1ac951f32dae286937a51c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2017

---

# <a name="reuse-product-configurations"></a><span data-ttu-id="3c707-105">Повторное использование конфигураций продуктов</span><span class="sxs-lookup"><span data-stu-id="3c707-105">Reuse product configurations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3c707-106">Можно указать, что требуется автоматически повторно использовать существующую конфигурацию продукта.</span><span class="sxs-lookup"><span data-stu-id="3c707-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="3c707-107">Затем, когда пользователь завершает сеанс настройки, система проверяет, не существует ли имеющейся конфигурации, которая соответствует выбору пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c707-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="3c707-108">Если такая конфигурация найдена, используются ИД конфигурации, соответствующая спецификация и маршрут.</span><span class="sxs-lookup"><span data-stu-id="3c707-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="3c707-109">Требования к повторному использованию конфигураций</span><span class="sxs-lookup"><span data-stu-id="3c707-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="3c707-110">Чтобы разрешить повторное использовании конфигураций, необходимо задать следующую информацию для компонентов и атрибутов на странице **Сведения о модели конфигурации продукта**:</span><span class="sxs-lookup"><span data-stu-id="3c707-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="3c707-111">**Компоненты и подкомпоненты** — на экспресс-вкладке **Общие** в поле **Повторно использовать конфигурации** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="3c707-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="3c707-112">**Атрибуты** — на экспресс-вкладке **Атрибуты** выберите параметр **Включить в повторное использование**.</span><span class="sxs-lookup"><span data-stu-id="3c707-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="3c707-113">Этот параметр отображается только в том случае, если для соответствующего компонента включено повторное использование.</span><span class="sxs-lookup"><span data-stu-id="3c707-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="3c707-114">Если не выбран ни один атрибут для повторного использования, конфигурация всегда повторно используется, независимо от параметров, выбранных в ходе сеанса конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3c707-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="3c707-115">Значения атрибутов в существующей конфигурации должны соответствовать значениям, выбранным пользователем.</span><span class="sxs-lookup"><span data-stu-id="3c707-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="3c707-116">Например, если пользователь выбирает цвет **Голубой** в качестве цвета во время сеанса конфигурации, система проверяет, есть ли в имеющейся конфигурация компонента голубой цвет.</span><span class="sxs-lookup"><span data-stu-id="3c707-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="3c707-117">Сброс повторного использования конфигураций</span><span class="sxs-lookup"><span data-stu-id="3c707-117">Resetting configuration reuse</span></span>
<span data-ttu-id="3c707-118">При сброс повторного использования конфигураций ранее созданные конфигурации больше не учитываются.</span><span class="sxs-lookup"><span data-stu-id="3c707-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="3c707-119">Сброс повторного использования конфигураций может потребоваться, если спецификация или маршрут были изменены, но никакие соответствующие атрибуты не были изменены.</span><span class="sxs-lookup"><span data-stu-id="3c707-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="3c707-120">Сброс повторного использования конфигураций производится на экспресс-вкладке **Общие** для компонента.</span><span class="sxs-lookup"><span data-stu-id="3c707-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>




