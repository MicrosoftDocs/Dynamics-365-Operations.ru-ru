---
title: Обновление бюджетов обслуживания
description: В этой статье объясняется, как обновить бюджет обслуживания в управлении активами.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a9333c9ad48c87159ed4071a8b4843fc0e55ceb5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860967"
---
# <a name="update-maintenance-budgets"></a>Обновление бюджетов обслуживания

[!include [banner](../../includes/banner.md)]

 

На странице **Строки бюджета обслуживания** отображаются все строки бюджета, которые были созданы для бюджета, выбранного на странице **Бюджеты обслуживания**. (Дополнительные сведения см. в разделе [Создание бюджетов обслуживания](create-maintenance-budget.md).) Строки бюджета обслуживания можно пересчитывать и корректировать до тех пор, пока бюджет обслуживания не утвержден. После прохождения бюджетного периода и разноски затрат в управлении активами можно также обновить строки бюджета фактическими затратами.

## <a name="recalculate-a-maintenance-budget"></a>Пересчет бюджета обслуживания

Пересчет бюджета обслуживания можно выполнить на странице **Строки бюджета обслуживания**. При пересчете бюджета обслуживания существующие строки бюджета удаляются, и выполняется новое вычисление.

1. На странице **Строки бюджета обслуживания** выберите **Пересчитать**.
2. В диалоговом окне **Пересчитать бюджет** выполните необходимые изменения для нового расчета, затем выберите **ОК**.

Новые строки бюджета создаются в соответствии с заданными значениями.

## <a name="adjust-budget-lines"></a>Корректировка строк бюджета

Вместо пересчета всего бюджета обслуживания можно скорректировать выбранные строки, которые относятся к бюджетным затратам.

1. На странице **Строки бюджета обслуживания** выберите строки, для которых необходимо обновить бюджетные затраты.
2. Выберите **Корректировка**.
3. Чтобы добавить сумму к выбранным строкам, установите флажок **Добавить затраты**, затем введите значение в поле **Добавить значение**.
4. Чтобы умножить бюджетные затраты в выбранных строках бюджета на коэффициент, установите флажок **Умножить затраты** и введите коэффициент в поле **Значение коэффициента**.

    Например, если ввести **1,2** в поле **Значение коэффициента**, бюджетные затраты в выбранных строках будут увеличены на 20 процентов. Если ввести **0,7**, бюджетные затраты по выбранным строкам будут уменьшены на 30 процентов.

5. Нажмите **ОК**.

Выбранные строки бюджета обновляются в соответствии со значениями, заданными на шаге 3 или 4.

## <a name="update-actual-costs"></a>Обновление фактических затрат

После прохождения дат строк бюджета разноски фактических затрат в управлении активами можно также обновить бюджет обслуживания с использованием фактических затрат.

1. На странице **Строки бюджета обслуживания** выберите **Обновить затраты**.
2. В диалоговом окне **Вычислить фактические затраты** выберите **ОК**.

Поля **Фактические затраты** в строках бюджета обновляются, если фактические затраты были разнесены. Новые строки бюджета могут быть созданы, если новые типы активов были созданы после создания бюджета, и если эти типы активов были использованы в активах, для которых были созданы заказы на работу и для которых были разнесены соответствующие затраты. В новых строках бюджета отображаются только фактические затраты, поскольку для них не были рассчитаны бюджетные затраты.

> [!NOTE]
> Чтобы просмотреть обзор фактических затрат, разделенных на профилактические, корректирующие и инвестиционные затраты, можно выполнить расчет для одного и того же периода на странице **Управление затратами по активам**. 

## <a name="manually-add-budget-lines"></a>Добавление строк бюджета вручную

На странице **Строки бюджета обслуживания** можно вручную добавить новую строку бюджета, выбрав **Создать**, затем сделав выбор в строке. Ниже приведены несколько примеров ситуаций, в которых такой подход может быть полезен:

- Известно, что ремонт некоторых активов в данный момент находится на этапе планирования, но в управлении активами еще не были созданы соответствующие задания. Однако требуется включить в бюджет обслуживания бюджетные затраты для этих заданий.
- Новые активы или типы активов были созданы после того, как был подготовлен бюджет обслуживания, но планы обслуживания еще не были настроены для этих активов или типов активов. Однако требуется включить в бюджет обслуживания бюджетные затраты для этих типов активов.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]