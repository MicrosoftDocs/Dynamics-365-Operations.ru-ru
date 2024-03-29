---
title: Корректировки кредит-нот (Россия)
description: В этой статье приводятся сведения о создании корректировок кредит-нот в модулях "Расчеты с клиентами" и "Расчеты с поставщиками".
author: AdamTrukawka
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.0
ms.search.form: ''
ms.openlocfilehash: ac28c93634888be84bdf43425238c76d3427dc48
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272949"
---
# <a name="credit-note-corrections-russia"></a>Корректировки кредит-нот (Россия)

[!include [banner](../includes/banner.md)]

## <a name="set-up-negative-amount-transactions-as-corrections"></a>Настройка проводок отрицательных сумм как коррекций

1. Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.
2. На вкладке **Главная книга** на экспресс-вкладке **Правила учета** установите для параметра **Коррекция** значение **Да**. Проводки, которые имеют отрицательные суммы, теперь можно разнести как корректировки в ГК.

## <a name="set-up-credit-notes-as-corrections"></a>Настройка кредит-нот в качестве корректировок

1. Перейдите в раздел **Расчеты с клиентами** \> **Настройка** \> **Параметры модуля расчетов с клиентами**.
2. На вкладке **Обновления** на экспресс-вкладке **Накладная** установите для параметра **Корректирующая кредит-нота** значение **Да**.
3. Перейдите в раздел **Расчеты с поставщиками** \> **Настройка** \> **Параметры расчетов с поставщиками**.
4. На вкладке **Накладная** на экспресс-вкладке **Накладная** установите для параметра **Корректирующая кредит-нота** значение **Да**.

## <a name="set-up-the-amount-sign-for-a-printed-invoice"></a>Настройка знака суммы для распечатанной накладной

1. Выберите **Расчеты с клиентами** \> **Настройка** \> **Формы** \> **Настройка форм**.
–или– Выберите **Расчеты с поставщиками** \> **Настройка** \> **Формы** \> **Настройка форм**.
2. На вкладке **Накладная** в поле **Печать кредит-нот** выберите значение. Это поле управляет знаком сумм в печатной форме накладной.

  - **Кредит-нота**: на странице **Печать** строки документа имеют противоположный знак суммы, чем в строках накладной. Иными словами, распечатанные суммы будут положительными.
  - **Возврат**: на странице **Печать** строки документа имеют тот же знак сумм, как и в строках накладной. Иными словами, распечатанные суммы будут отрицательными.

## <a name="create-a-credit-note-for-correction-in-accounts-receivable"></a>Создание кредит-ноты для коррекции в модуле "Расчеты с клиентами"

### <a name="post-free-text-invoices-as-credit-corrections"></a>Разноска накладных с произвольным текстом в качестве исправлений кредита
Вы можете создавать и разносить накладные с произвольным текстом в качестве корректировок по кредитам для проводок номенклатур возврата. Чтобы скорректировать накладную с произвольным текстом, содержащую как положительные, так и отрицательные суммы накладной, необходимо выполнить следующие действия.

1. Перейдите в раздел **Расчеты с клиентами** \> **Накладные** \> **Все накладные с произвольным текстом**.
2. Выберите существующую накладную с произвольным текстом для возвращенной номенклатуры.
3. На экспресс-вкладке **Строки накладной** добавьте строку накладной с положительной или отрицательной суммой накладной, в зависимости от типа коррекции.
4. Выберите **Разнести**, чтобы открыть диалоговое окно **Разноска накладной с произвольным текстом**.
5. Установите для параметра **Корректировка по кредиту** значение **Да**, затем выберите **ОК**, чтобы разнести накладную. В этой накладной суммы имеют либо положительный знак, либо отрицательный знак, в зависимости от направления корректировки. Если сумма накладной положительна, вы получите сообщение об активации параметра корректировки по кредиту.

> [!NOTE]
> Кредит-ноту можно создать, выбрав **Создать кредит-ноту** в группе **Отменить** на вкладке **Накладная** панели операций. Используйте флажок **Отметить**, чтобы выбрать накладную и строки накладной, затем выберите **ОК**. Создаются строки, идентичные строкам накладной, но имеющие противоположный знак суммы.

6. На панели операций на вкладке **Накладная** на вкладке **Связанные сведения** выберите **Журнал накладных**, чтобы открыть страницу **Журнал накладных**.
7. Выберите **Проводки**, чтобы открыть страницу **Проводки по клиенту**. Просмотрите столбец **Корректировка**, чтобы убедиться, что проводка была создана в качестве корректировки для проводки возврата номенклатуры.

> [!TIP]
> Если столбец **Коррекция** не отображается, щелкните правой кнопкой мыши в строке заголовка сетки, затем выберите **Добавить столбцы**. В диалоговом окне установите флажок для столбца **Коррекция**, затем выберите **Вставить**.

8. Выберите **Ваучер**, чтобы открыть страницу **Проводки ваучера**. Просмотрите столбец **Коррекция**, чтобы убедиться, что проводка была разнесена как корректировка.

### <a name="create-credit-corrections-for-sales-orders"></a>Корректировки кредит-нотами для заказов на продажу
Так же, как можно разносить накладные с произвольным текстом как корректировки по кредиту, можно создавать кредит-ноты для заказов на продажу. На странице **Заказ на продажу** выберите **Кредит-нота**. Выберите заказ на продажу, для которого будет создана кредит-нота, выберите строки заказа на продажу для корректировки, затем выберите **ОК**. Затем на странице **Разноска накладной** установите для параметра **Корректировка по кредиту** значение **Да**, чтобы разнести накладную.

На странице журнала накладных можно просмотреть исходную накладную и кредит-ноту. На страницах проводок по клиенту и проводок ваучера можно проверить, что проводки были разнесены в виде корректировок.

## <a name="create-a-credit-note-for-correction-in-accounts-payable"></a>Создание кредит-ноты для коррекции в модуле "Расчеты с поставщиками"

### <a name="post-and-print-a-reverse-transaction-for-a-purchase-order-credit-note"></a>Разноска и печать реверсирующей проводки для кредит-ноты заказа на покупку
Можно использовать кнопку **Кредит-нота** для разноски проводки по кредит-ноте заказа на покупку как сторнированной проводки. Выберите заказ на покупку для кредит-ноты, выберите строки заказа на покупку, затем выберите **ОК**. Затем на странице **Накладная поставщика** на панели операций на вкладке **Обработать** в группе **Задать** выберите **Настройка кредита**. Установите для параметра **Корректировка по кредиту** значение **Да** и разнесите накладную.

На странице **Журнал накладных** можно выполнить следующие действия:

- Выберите **Проводки**, чтобы открыть страницу **Проводки поставщика**, и просмотрите столбец **Коррекция**, чтобы убедиться, что проводка была создана в качестве корректировки.
- Выберите **Ваучер**, чтобы открыть страницу **Проводки ваучера**, и просмотрите столбец **Коррекция**, чтобы убедиться, что проводка была создана в качестве корректировки.
- Выберите **Просмотр/печать**, чтобы напечатать отчет.

### <a name="post-vendor-invoices-as-credit-corrections"></a>Разноска накладных поставщика как коррекций кредита
На странице **Открытые накладные поставщиков** вы можете создавать и разносить накладные поставщика в качестве корректировок по кредитам для проводок номенклатур возврата. Процедура похожа на процедуру разноски реверсирующей проводки для кредит-ноты по заказу на покупку, рассмотренной ранее в этой статье.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
