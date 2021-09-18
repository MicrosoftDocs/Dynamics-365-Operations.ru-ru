---
title: Функциональные разрывы между отчетами стоимости запасов/устаревания и их версиями хранилищ
description: Функциональные разрывы между отчетами стоимости запасов/устаревания и их версиями хранилищ
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a72e2d32e755e137cebbc0bf7afb0bed08fb93f2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477440"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Функциональные разрывы между отчетами стоимости запасов/устаревания и их версиями хранилищ

Функции [Хранилище отчетов о распределении запасов по срокам](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage.md) и [Отчет о стоимости запасов по складам](/dynamics365/supply-chain/cost-management/inventory-value-report-storage.md) позволяют Supply Chain Management отображать большие объемы складских проводок. В каждом случае результаты отчета сохраняются для просмотра и экспорта, в отличие от версий этих отчетов, не связанных с хранилищем. Однако некоторые функциональные возможности, существующие в версиях этих отчетов, не связанных с хранилищем, в версиях с хранилищами отсутствуют. В следующих подразделах приведены различия и предлагаются способы их обхода.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Отчеты с хранилищем не включают промежуточные суммы, даже если они включены в макете отчета

Промежуточные суммы могут вызывать ошибки при экспорте результатов, особенно если пользователи изменяют последовательность записей.

Для проверки промежуточных сумм можно экспортировать результат в Microsoft Excel. Кроме того, если необходимо проверить промежуточные суммы в Supply Chain Management, используйте раздел [Управление функциями](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), чтобы включить функции *Новый элемент управления сетки* и *Группировка в сетках*, которые обеспечивают более гибкий способ отображения промежуточных итогов для любого столбца, по которому производится группировка. Дополнительные сведения см. в разделе [Возможности сетки](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities.md).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Отчет о стоимости запасов с хранилищем не поддерживает сведения о счетах ГК

Можно выполнить пробный баланс для того, чтобы получить сальдо по счетам запасов, и сравнить их с отчетом **стоимости запасов по складам**.
