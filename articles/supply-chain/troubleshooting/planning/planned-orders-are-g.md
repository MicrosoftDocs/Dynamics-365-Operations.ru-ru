---
title: Сводное планирование создает спланированные заказы для виртуальных продуктов
description: Спланированные заказы для виртуальных продуктов создаются после выполнения сводного планирования.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026854"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="b0dd8-103">Сводное планирование создает спланированные заказы для виртуальных продуктов</span><span class="sxs-lookup"><span data-stu-id="b0dd8-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="b0dd8-104">Номер статьи базы знаний: 4614729</span><span class="sxs-lookup"><span data-stu-id="b0dd8-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="b0dd8-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="b0dd8-105">Symptoms</span></span>

<span data-ttu-id="b0dd8-106">Спланированные заказы для виртуальных продуктов создаются после выполнения сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="b0dd8-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="b0dd8-107">Resolution</span></span>

<span data-ttu-id="b0dd8-108">Настройка параметра **Виртуальный** для выпущенных продуктов определяет тип строки по умолчанию для спецификации.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="b0dd8-109">Если для параметра **Виртуальный** установлено значение *Да*, система все равно создаст спланированные заказы для номенклатуры, но для каждого спланированного заказа параметр **Непосредственно производное требование** будет установлено значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="b0dd8-110">Поэтому спланированный производственный заказ не может быть утвержден самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="b0dd8-111">Вместо этого он всегда будет автоматически включено при утверждении родительского производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="b0dd8-112">Кроме того, строки спецификации спланированного виртуального заказа будут включены в спецификацию родительского производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
