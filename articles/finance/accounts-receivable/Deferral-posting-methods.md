---
title: Методы разноски выручки и расходов будущих периодов
description: В этой статье описываются различия между методами разноски РБП для выручки и расходов будущих периодов в выставлении счетов по подпискам.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9019103"
---
# <a name="deferral-posting-methods"></a>Методы разноски выручки и расходов будущих периодов

В этой статье описываются различия между методами разноски РБП для выручки и расходов будущих периодов в выставлении счетов по подпискам.

На странице **Параметры выручки и расходов будущих периодов** для методов разноски выручки и расходов будущих периодов доступны варианты **Балансовый отчет** и **Прибыли и убытки**. Пример в этой статье поможет объяснить различия между двумя методами и причины, по которым можно выбрать использование одного метода или другого.

Метод **Балансовый отчет** использует только два счета. Таким образом, требуется меньше настроек. Метод **Прибыли и убытки** включает в себя две дополнительных счета, **Первоначальное признание** и **Корр. счет признания** для выручки, скидок и затрат, в зависимости от типа проводки. Эти счета настраиваются на странице **Значения отсрочки по умолчанию** (**Выставление счетов по подпискам \> Отсрочки выручки и расхода \> Настройка**). Хотя пример ориентирован на выручку будущих периодов, эта же концепция может применяться к скидкам будущих периодов и затратам будущих периодов.

## <a name="example"></a>Пример

В накладной заказа на продажу 1 имеется общая сумма 3000 долларов США и выручка будущих периодов. В следующих таблицах показаны распределения при разноске этой накладной заказа на продажу.

**Метод балансового отчета**

| Тип | Организация | Дебет | Кредит|
|---|---|---|---|
| Дебет | Дебиторская задолженность | 3,000.00 | |
| Кредит | Выручка будущих периодов | | 3,000.00 |

**Метод прибылей и убытков**

| Тип | Организация | Дебет | Кредит |
|---|---|---|---|
| Дебет | Дебиторская задолженность | 3,000.00 | |
| Дебет | Корр. счет признания выручки | 3,000.00 | |
| Кредит | Выручка будущих периодов | | 3,000.00 |
| Кредит | Первоначальное признание выручки | | 3,000.00 |

В накладной заказа на продажу 2 имеется общая сумма 2000 долларов США и нет выручки будущих периодов.

| Тип | Организация | Сумма |
|---|---|---|
| Дебет | Дебиторская задолженность | 3,000.00 |
| Кредит | Реализация | 3,000.00 |

**Итоговые суммы метода балансового отчета для комбинирования накладных заказа на продажу 1 и 2**

| Организация | Дебет | Кредит |
|---|---|---|
| Дебиторская задолженность | 5,000.00 | |
| Реализация | | 2,000.00 |
| Выручка будущих периодов | | 3,000.00 |

При использовании метода **Балансовый отчет** сложно посмотреть валовую выручку за период. Часть выручки разнесена на счет **Выручка будущих периодов**. Имейте в виду, что по мере того, как выручка будет признаваться за каждый период, будут несколько проводок по дебету и кредиту для счета **Выручка будущих периодов**. Валовая выручка за определенный период будет смешиваться с поступлениями и выбытиями признания выручки.

**Итоговые суммы метода прибыли и убытков для комбинирования накладных заказа на продажу 1 и 2**

| Организация | Дебет | Кредит |
|---|---|---|
| Дебиторская задолженность | 5,000.00 | |
| Реализация | | 5,000.00 |
| Корр. счет выручки | 3,000.00 | |
| Выручка будущих периодов | | 3,000.00 |

Вся выручка переходит на счет прибылей и убытков **Выручка**. Затем выручка будущих периодов перемещается из отчета о прибылях и убытках в балансовый отчет. Можно легко просмотреть валовую выручку, так как все будет разноситься на счет **Выручка**. Однако часть этой валовой выручки относится к будущим периодам. Таким образом, она перемещается на счет **Выручка будущих периодов** и признается позже.

В методе **Прибыли и убытки** можно просмотреть счета **Выручка** и **Корр. счет выручки**, чтобы увидеть валовую выручку 5000 долларов США и чистую выручки (без выручки будущих периодов) 2000 долларов США. Хотя метод **Прибыли и убытки** может упростить отчетность, нужно настраивать дополнительные счета.