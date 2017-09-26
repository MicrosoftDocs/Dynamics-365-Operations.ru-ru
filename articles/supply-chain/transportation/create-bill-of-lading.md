---
title: "Создание транспортной накладной"
description: "В этом разделе описывается создание транспортной накладной при использовании процессов управления складом."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f3010daa41f54cf026d46b1b7648a277651173da
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017

---

# <a name="create-a-bill-of-lading"></a>Создание транспортной накладной

[!include[banner](../includes/banner.md)]


В этом разделе описывается создание транспортной накладной при использовании процессов управления складом.  

Транспортная накладная — юридический документ между компанией, которая отгружает номенклатуры, и перевозчиком. Документ сопровождает отгруженные номенклатуры и служит как подтверждение получения отгрузки, когда номенклатуры доставляются по месту назначения. Если вы используете управление складом, существует два способа создания транспортной накладной:

  -   Создайте отчет вручную, используя страницу **Транспортная накладная**.
  -   Создайте отчет в разделе **Рабочее место планирования загрузки**.

При создании транспортной накладной в разделе **Рабочее место планирования загрузки** статус загрузки должен быть **Отгружено.** Если имеется более одной отгрузки в загрузке, транспортная накладная создается для каждой отгрузки. После создания транспортной накладной можно вносить в нее изменения на странице **Транспортная накладная**.

## <a name="master-bill-of-lading"></a>Сводная транспортная накладная
При наличии нескольких отгрузок в загрузке можно создать сводную транспортную накладную. Она имеет тот же макет и сведения как и транспортная накладная, но содержит сводное содержимое по всем отгрузкам. Если для параметра **Создание сводной транспортной накладной при наличии нескольких отгрузок для загрузки** задано значение **Да** на странице **Параметры управления транспортировкой**, сводная транспортная накладная создается автоматически при создании транспортной накладной в разделе **Рабочее место планирования загрузки** и имеется несколько отгрузок. Можно также получить список транспортных накладных, щелкнув **Связанные сведения** &gt; **Транспортная накладная**. При создании транспортной накладной вручную можно создать сводную транспортную накладную на странице **Транспортная накладная**.



