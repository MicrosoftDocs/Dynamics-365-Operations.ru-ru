---
title: Результаты амортизации со сторнированием
description: Эта статья описывает потенциальные последствия реверсирования проводки с основными средствами.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d47a25835eab16438ea47bf3960132debc8c975
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187900"
---
# <a name="depreciation-effects-with-reversals"></a>Результаты амортизации со сторнированием

[!include [banner](../includes/banner.md)]

Эта статья описывает потенциальные последствия реверсирования проводки с основными средствами. 

Имеется возможность реверсировать проводки по основным средствам, а также проводки, связанные с основными средствами. Кроме того, можно отменить реверсированную проводку. 

Можно реверсировать или отменить реверсированную проводку, которая не является последней проводкой, разнесенной в книге для средства. Сначала необходимо определить, разносились ли какие-либо проводки амортизации после той проводки, которая реверсируется. Это необходимо, потому что амортизация не пересчитывается при реверсировании проводки. Поэтому амортизация часто завышена или занижена после реверсирования, как показано в примерах. 

Чтобы гарантировать правильность амортизации при реверсировании проводки, не продолжайте реверсирование в том случае, когда в процессе его выполнения получено сообщение, информирующее о том, что амортизация не будет пересчитана. Вместо этого сначала отмените проводку по амортизации, которая была разнесена после той проводки, которую вы пытаетесь реверсировать, а затем продолжите реверсирование. Теперь сообщение о невозможности пересчета амортизации не появится, и можно будет выполнить реверсирование. 

Следующие примеры иллюстрируют вычисления, которые будут произведены в том случае, если проигнорировать предупреждающее сообщение и продолжить реверсирование проводки без предварительной отмены проводок по амортизации.

## <a name="example-1-depreciation-is-overstated"></a>Пример 1: Амортизация завышена
Настройка средства подразумевает 5-летний срок жизни и линейную амортизацию (60 периодов амортизации). В этом примере амортизация завышена.
#### <a name="asset-transaction-history"></a>Журнал проводок активов

| Дата       | Тип проводки                                                          | Сумма                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1 января  | Ввод в эксплуатацию                                                               | 59 000,00                                 |
| 1 января  | Переоценка стоимости ввода в эксплуатацию                                                    | 1 000,00                                  |
| 31 января | Амортизация (создано с помощью предложения для одного периода амортизации) | 1000,00 Расчет: остаточная стоимость (59000 + 1000) / Число оставшихся периодов амортизации (60) |

#### <a name="reversal-action"></a>Действие реверсирования

| Дата      | Тип проводки                | Сумма    |
|-----------|---------------------------------|-----------|
| 1 января | Сторнирование переоценки стоимости ввода в эксплуатацию | -1 000,00 |

#### <a name="depreciation-effect"></a>Влияние амортизации

| Дата        | Тип проводки        | Сумма                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28 февраля | Амортизация (предложение) | 983,05 Расчет: остаточная стоимость (59000 – 1000 амортизация) / Число оставшихся периодов амортизации (59) |

Амортизация завышена на 16,95 (1000 - 983,05).

## <a name="example-2-depreciation-is-understated"></a>Пример 2: Амортизация занижена
Настройка средства подразумевает 5-летний срок жизни и линейную амортизацию (60 периодов амортизации). В этом примере амортизация занижена.
#### <a name="asset-transaction-history"></a>Журнал проводок активов

| Дата       | Тип проводки                                                          | Сумма                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1 января  | Приобретение                                                               | 59 000,00                                   |
| 1 января  | Корректировка уценки                                                     | 1 000,00                                    |
| 31 января | Амортизация (создано с помощью предложения для одного периода амортизации) | 966,67 Расчет: остаточная стоимость (59000 + 1000) / Число оставшихся периодов амортизации (60) |

#### <a name="reversal-action"></a>Действие реверсирования

| Дата      | Тип проводки               | Сумма    |
|-----------|--------------------------------|-----------|
| 1 января | Реверсирование корректировки уценки | -1 000,00 |

#### <a name="depreciation-effect"></a>Влияние амортизации

| Дата        | Тип проводки        | Сумма                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28 февраля | Амортизация (предложение) | 983,62 Расчет: остаточная стоимость (59000 – 1000 амортизация) / Число оставшихся периодов амортизации (59) |

Амортизация занижена на 16,95 (983,62 - 966,67).



## <a name="additional-resources"></a>Дополнительные ресурсы

[Амортизация ОС](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]