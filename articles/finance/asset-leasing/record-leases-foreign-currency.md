---
title: Запись аренды в иностранной валюте
description: В этой статье объясняется, как записывать аренды в валютах, отличных от валюты учета или валюты отчетности.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 56c15e648d6aa515192a6f41ba06df6405ca79f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878112"
---
# <a name="record-leases-in-foreign-currencies"></a>Запись аренды в иностранной валюте

[!include [banner](../includes/banner.md)]

Счета аренды актива для аренд, которые ведутся в валютах, отличных от валюты учета или валюты отчетности, задаются на странице **Настройка книги учета**. Все аренды должны быть введены в валюте проводки. Другими словами, они должны вводиться в валюте, указанной в контракте аренды. В этой статье объясняется, как записывать аренды в валютах, отличных от валюты учета или валюты отчетности.

При вводе аренды в иностранной валюте, актив в форме права пользования (ФПП) амортизируется как в валюте учета, так и в валюте отчетности. Эти валюты настраиваются на странице **Настройка книги учета**. Это поведение также используется в модуле основных средств. При создании аренды в иностранной валюте выберите валюту проводки в поле **Валюта**.

Валютный курс валюты учета является значением по умолчанию в поле **Валютный курс валюты учета**. Валютный курс валюты отчетности является значением по умолчанию в поле **Валютный курс валюты отчетности**. Эти валютные курсы действовали на дату начала аренды. Поля **Валютный курс валюты учета** и **Валютный курс валюты отчетности** находятся на экспресс-вкладке **Сведения об обмене для финансов и отчетности** на странице **Сведения об аренде**.

1. Установите флажок **Фиксированный курс**, чтобы переопределить введенный автоматически валютный курс, а затем введите новый курс.
2. В других полях введите сведения, необходимые для аренды, а затем выберите **Создать расписания**.
3. На странице **Сведения об аренде** выберите **Книги**.
4. На странице **Книга аренды** на вкладке **Сведения об обмене для финансов и отчетности** проверьте значения полей **Первоначальный актив в форме права пользования в валюте учета** и **Первоначальный актив в форме права пользования в валюте отчетности**. Каждое из этих полей показывает переведенное сальдо актива ФПП в соответствующей валюте. Эти поля обновляются при каждом изменении любой финансовой информации. Выберите **Создать расписания** до подтверждения графика оплаты.

    Запись журнала первоначального признания записывает актив ФПП, который использует валютные курсы, перечисленные в аренде. Запись журнала также включает значения в полях **Первоначальный актив в форме права пользования в валюте учета** и **Первоначальный актив в форме права пользования в валюте отчетности**.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Последующее измерение для аренды в иностранной валюте

График амортизации показывает ожидаемые суммы расходов по амортизации в валюте отчетности, валюте учета и валюте проводки.

Чтобы просмотреть сальдо актива ФПП и суммы амортизации в валюте отчетности или в валюте учета, откройте страницу **График амортизации актива** и установите флажок **Показать суммы в валюте учета** или **Показать суммы в валюте отчетности**.

При создании записей журнала расходов на амортизацию по аренде, которая была определена в иностранной валюте, в записи используются валютные курсы, перечисленные в аренде. Также используются значения в полях **Первоначальный актив в форме права пользования в валюте учета** и **Первоначальный актив в форме права пользования в валюте отчетности**.

Окончательную сумму расходов на амортизацию можно рассчитать, используя слегка отличающийся валютный курс, чтобы актив ФПП был полностью амортизировать в валюте учета и в валюте отчетности.

Если аренда была реклассифицирована как **Отложенная рента**, система автоматически очищает обменные курсы в валютах учета и отчетности, если они уже были определены.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
