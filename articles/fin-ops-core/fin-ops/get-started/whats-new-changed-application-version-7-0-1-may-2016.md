---
title: Что нового и что изменилось в версии приложения Dynamics AX 7.0.1 (май 2016 г.)
description: В этой статье описываются новые и измененные компоненты в приложении Microsoft Dynamics AX версии 7.0.1. Эта версия была выпущена в мае 2016 г. и имеет номер сборки 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 1dd76150dd1519adf2c453db8e874d6db32b5906
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693150"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="b1877-104">Что нового и что изменилось в версии приложения Dynamics AX 7.0.1 (май 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="b1877-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1877-105">В этой статье описываются новые и измененные компоненты в приложении Microsoft Dynamics AX версии 7.0.1.</span><span class="sxs-lookup"><span data-stu-id="b1877-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="b1877-106">Эта версия была выпущена в мае 2016 г. и имеет номер сборки 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="b1877-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="b1877-107">Электронная отчетность (ER)</span><span class="sxs-lookup"><span data-stu-id="b1877-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="b1877-108">Что можно сделать?</span><span class="sxs-lookup"><span data-stu-id="b1877-108">What can you do?</span></span> | <span data-ttu-id="b1877-109">Почему это важно?</span><span class="sxs-lookup"><span data-stu-id="b1877-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="b1877-110">Настройте диалоговое окно времени выполнения для разработки отчетов электронной отчетности (ER), чтобы пользователи могли выбирать требуемые финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="b1877-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="b1877-111">Во время выполнения в диалоговом окне для выполнения отчета электронной отчетности пользователи могут выбрать несколько финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="b1877-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="b1877-112">Подробные сведения о выбранных финансовых аналитиках будут отображаться в создаваемом электронном документе.</span><span class="sxs-lookup"><span data-stu-id="b1877-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="b1877-113">Настройте доступ к нескольким финансовым аналитикам во время разработки отчета электронной отчетности с помощью одиночного сопоставления с необходимым источником данных.</span><span class="sxs-lookup"><span data-stu-id="b1877-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="b1877-114">Одну и ту же конфигурацию отчета электронной отчетности можно использовать для создания электронных документов, представляющих данные транзакций вместе со сведениями о финансовых аналитиках, независимо от количества финансовых аналитик, выбранных пользователем или настроенных для текущего юридического лица или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1877-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="b1877-115">Настройте отчет электронной отчетности для ввода данных в динамически создаваемых столбцах электронного документа, который создается в формате листа OPENXML.</span><span class="sxs-lookup"><span data-stu-id="b1877-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="b1877-116">Отчет электронной отчетности может ввести данные в создаваемый лист OPENXML посредством горизонтально реплицируемых столбцов.</span><span class="sxs-lookup"><span data-stu-id="b1877-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="b1877-117">Таким образом, одну и ту же конфигурацию отчетов электронной отчетности можно повторно использовать для создания электронных документов, которые содержат различное количество динамически создаваемых столбцов.</span><span class="sxs-lookup"><span data-stu-id="b1877-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="b1877-118">Настройки назначений аварийной отчетности таким образом, чтобы выходной результат формата направлялся в определенное назначение: файл, электронную почту или архив (папка Microsoft SharePoint или хранилище Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="b1877-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="b1877-119">Ранее при выполнении конфигурации электронной отчетности отображалось окно сообщения с запросом действия пользователя для сохранения или открытия файла.</span><span class="sxs-lookup"><span data-stu-id="b1877-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="b1877-120">Теперь можно отдельно предварительно настроить назначение для каждой конфигурации формата и каждого выходного компонента (папка или файл).</span><span class="sxs-lookup"><span data-stu-id="b1877-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="b1877-121">Пользователи, имеющие соответствующие права доступа, также могут изменять настройки назначения во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1877-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="b1877-122">POS – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="b1877-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="b1877-123">Что можно сделать?</span><span class="sxs-lookup"><span data-stu-id="b1877-123">What can you do?</span></span> | <span data-ttu-id="b1877-124">Почему это важно?</span><span class="sxs-lookup"><span data-stu-id="b1877-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="b1877-125">Использовать браузер Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="b1877-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="b1877-126">Предприятия розничной торговли теперь могут запустить Cloud POS из браузера Chrome и использовать все функциональные возможности, доступные в Microsoft Edge и версии Internet Explorer Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="b1877-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="b1877-127">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="b1877-127">Financial reporting</span></span>

| <span data-ttu-id="b1877-128">Что можно сделать?</span><span class="sxs-lookup"><span data-stu-id="b1877-128">What can you do?</span></span> | <span data-ttu-id="b1877-129">Почему это важно?</span><span class="sxs-lookup"><span data-stu-id="b1877-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="b1877-130">Перестроить магазин финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="b1877-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="b1877-131">При перемещении баз данных Dynamics AX между средами или внесении других существенных изменений в среду может потребоваться перестройка базы данных финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="b1877-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="b1877-132">Теперь сценарий Windows PowerShell может перестроить базу данных за вас.</span><span class="sxs-lookup"><span data-stu-id="b1877-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="b1877-133">Больше неневозможно выбрать параметры конструктора отчетов, которые не являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="b1877-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="b1877-134">Несколько параметров конструктора отчетов, которые использовались в находящихся на рынке версиях Management Reporter, не применяются к этой версии Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="b1877-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="b1877-135">Эти параметры были связаны с дизайном финансовых отчетов, выходными данными и привязкой.</span><span class="sxs-lookup"><span data-stu-id="b1877-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="b1877-136">Эти параметры были удалены из конструктора финансовых отчетов для предотвращения ошибок пользователя.</span><span class="sxs-lookup"><span data-stu-id="b1877-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="b1877-137">Управление финансами</span><span class="sxs-lookup"><span data-stu-id="b1877-137">Financial management</span></span>

| <span data-ttu-id="b1877-138">Что можно сделать?</span><span class="sxs-lookup"><span data-stu-id="b1877-138">What can you do?</span></span> | <span data-ttu-id="b1877-139">Почему это важно?</span><span class="sxs-lookup"><span data-stu-id="b1877-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="b1877-140">Создать файлы положительных платежей для платежей по расчетам с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="b1877-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="b1877-141">Можно создать файлы положительных платежей для предотвращения мошенничества с чеками.</span><span class="sxs-lookup"><span data-stu-id="b1877-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="b1877-142">Склад и производство</span><span class="sxs-lookup"><span data-stu-id="b1877-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b1877-143">Что можно сделать?</span><span class="sxs-lookup"><span data-stu-id="b1877-143">What can you do?</span></span></th>
<th><span data-ttu-id="b1877-144">Почему это важно?</span><span class="sxs-lookup"><span data-stu-id="b1877-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b1877-145">Определить политику работы склада, которая управляет созданием работы для набора продуктов в определенных местонахождениях.</span><span class="sxs-lookup"><span data-stu-id="b1877-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="b1877-146">Процессы склада не всегда включают работу.</span><span class="sxs-lookup"><span data-stu-id="b1877-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="b1877-147">С помощью новой политики работы склада можно предотвратить создание работы для комплектации сырья и размещения готовой продукции для набора продуктов в определенных местонахождениях.</span><span class="sxs-lookup"><span data-stu-id="b1877-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1877-148">Указать, что выходное местонахождение производства не находится под управлением номерного знака.</span><span class="sxs-lookup"><span data-stu-id="b1877-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="b1877-149">Теперь можно указать, что выходное местонахождение продукта не находится под управлением номерного знака.</span><span class="sxs-lookup"><span data-stu-id="b1877-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="b1877-150">Например, эта функция полезна, когда вышестоящий производственный заказ сообщает о готовых номенклатурах непосредственно в местонахождение, которое выступает в качестве входящего местонахождения производства для нижестоящего производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="b1877-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1877-151">Поддерживать спецификации, содержащие номенклатуры с различными аналитиками продукта одной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b1877-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="b1877-152">При использовании одной или нескольких аналитик продукта в производстве могут возникать ситуации, когда требуется произвести номенклатуру, основанную на другом варианте той же номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b1877-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="b1877-153">Дополнительные сведения см. в <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">этом блоге</a>.</span><span class="sxs-lookup"><span data-stu-id="b1877-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1877-154">Производственные заказы с циклическими структурами на первом уровне своих спецификаций исключаются из расчета уровня спецификации при планировании материальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1877-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="b1877-155">Невозможно назначить правильные уровни спецификации вариантам продукта для производственных заказов, которые вызывают цикличность в иерархии спецификаций.</span><span class="sxs-lookup"><span data-stu-id="b1877-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1877-156">Рассчитать отдельные уровни спецификации для планирования материальных ресурсов и расчета стоимости:</span><span class="sxs-lookup"><span data-stu-id="b1877-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="b1877-157">При планировании материальных ресурсов уровни спецификации рассчитываются в новой таблице <strong>ReqItemLevel</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1877-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="b1877-158">Завершенные производственные заказы игнорируются при расчете.</span><span class="sxs-lookup"><span data-stu-id="b1877-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="b1877-159">При расчете производственных затрат уровни спецификации рассчитываются в таблице <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1877-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="b1877-160">Завершенные производственные заказы включаются в расчет.</span><span class="sxs-lookup"><span data-stu-id="b1877-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="b1877-161">При выполнении планирования материальных ресурсов, например, составлении плана и развертывании сводного планирования, следует пересчитывать только уровни спецификации, используемые для планирования материальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1877-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="b1877-162">Другими словами, нет необходимости рассчитывать уровни спецификации, используемые для расчета учета затрат по производству.</span><span class="sxs-lookup"><span data-stu-id="b1877-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="b1877-163">При выполнении операций учета затрат, например закрытия склада, необходимо пересчитать только уровни спецификации, используемые для расчета учета затрат по производству.</span><span class="sxs-lookup"><span data-stu-id="b1877-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="b1877-164">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b1877-164">Additional resources</span></span>

[<span data-ttu-id="b1877-165">Что нового и что изменилось на домашней странице Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1877-165">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)

[<span data-ttu-id="b1877-166">Новые или обновленные руководства по задачам (май 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="b1877-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
