---
title: Создание и разноска журналов бюджета для приобретений ОС (Россия)
description: В этой статье поясняется, как создать и разнести журнал бюджета для приобретения основных средств для России.
author: AdamTrukawka
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.search.form: BudgetModel
ms.openlocfilehash: fe35639cd4f31cbadcff899b5ff9265244de36bb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282973"
---
# <a name="create-and-post-budget-journals-for-fixed-asset-acquisitions-russia"></a>Создание и разноска журналов бюджета для приобретений ОС (Россия)

[!include [banner](../includes/banner.md)]

В модуле **Основные средства** можно создавать финансовые планы и текущие бюджеты с помощью бюджетных моделей. Модель бюджета представляет собой коллекцию планируемых оборотов для конкретных счетов и периодов.

1. Выберите **Бюджетирование** \> **Настройка** \> **Основное бюджетирование** \> **Бюджетные модели**.
2. Выберите **Создать**, чтобы создать бюджетную модель.
3. В поле **Бюджетная модель** введите код для бюджетной модели. В поле **Имя** введите имя для модели бюджета.
4. Закройте страницу **Бюджетные модели**.
5. Выберите **Основные средства (Россия)** \> **Журналы** \> **Журнал бюджетов ОС**.
6. Выберите вкладку **Список** и выберите **Создать**, чтобы создать журнал.
7. В поле **Имя** выберите имя журнала.
8. Выберите **Строки**, чтобы открыть страницу **Ваучер журнала**, на которой можно вводить проводки по бюджету основных средств.
9. Выберите вкладку **Список** и выберите **Создать**, чтобы создать проводку бюджета.
10. В поле **Модель бюджета** выберите модель бюджета.
11. В поле **Учет** можно изменить модель стоимости основных средств.
12. В поле **Тип проводки** выберите **Ввод в действие**.
13. В поле **Дата** можно изменить дату проводки.
14. В поле **Тип счета** можно изменить тип счета.
15. В поле **Счет** выберите номер основного средства.
16. В поле **Текст проводки** выберите текст проводки.
17. В поле **Дебет** или **Кредит** введите сумму транзакции.
18. В поле **Тип корр. счета** выберите тип счета ГК.
19. В поле **Корр. счет** выберите номер счета ГК.

    > [!NOTE]
    > Если для этой проводки установлен профиль разноски, в поле **Корр. счет** автоматически отображается номер счета.

20. Повторите шаги с 9 по 19 для каждого дополнительного типа проводки по основным средствам.

    > [!NOTE]
    > Чтобы создать проводки группового приобретения или группового расчета амортизации, выберите **Ввод в эксплуатацию** или **Амортизация**. При создании проводки приобретения укажите дату проводки и бюджетную модель. При создании проводки для расчета амортизации укажите дату проводки, бюджетную модель и модель стоимости для проводки.

21. Выберите **Проверить** \> **Проверить**, чтобы проверить в журнале сведения об основном средстве.
22. Выберите **Разнести** \> **Перенос в бюджет ОС**, чтобы перенести проводки в бюджет основных средств.
23. Выберите **Разнести** \> **Перенос в бюджет ОС и в бюджет ГК**, чтобы перенести проводки в бюджет основных средств и ГК.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
