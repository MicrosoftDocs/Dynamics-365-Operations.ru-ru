---
title: Настройка параметров аренды (предварительная версия)
description: В этой теме описываются параметры конфигурации для аренды активов, такие как сведения о безопасности и параметры учета.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 77caf751f9baf4abef534bac97e226484df7acf7
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881284"
---
# <a name="configure-lease-parameters"></a>Настройка параметров аренды

[!include [banner](../includes/banner.md)]

Несколько параметров конфигурации влияют на поведение модуля аренды активов. Эти параметры включают в себя имена журналов, общие параметры и настройки профиля разноски.

1. Перейдите в раздел **Аренда активов \> Настройка \> Параметры аренды активов**.
2. На вкладке **Аренды** выберите экспресс-вкладку **Общие**.

    Параметр **Разрешить переопределение классификации вручную** определяет, можно ли переопределить классификацию аренды до подтверждения графика оплаты.

    Параметр **Пакетная обработка между юридическими лицами** определяет, можно ли выполнять разноску других юридических лиц из текущего юридического лица. Если этот параметр включен, можно создавать записи журнала для юридических лиц, к которым имеется доступ.

3. Установите для параметра **Разрешить удаление подтвержденных аренд** значение **Да**, чтобы разрешить удаление аренд, для которых подтверждены графики платежей. Аренды не могут быть удалены, если с ними связаны разнесенные или неразнесенные проводки, независимо от значения этого параметра. Восстановить запись аренды после ее удаления невозможно. При отправке любых записей для удаленной аренды, вручную или через сущности данных, отправленная информация рассматривается как новая, а не как обновление существующей аренды.

    Если для этого параметра задано значение **Да**, а тип перехода книги — **Накопительное дополнение, параметр A или B**, система устанавливает в поле **Приростная ставка процента на заемный капитал** значение поля **Приростная ставка процента на заемный капитал при переходе** на странице **Настройка книги**. Если этот параметр имеет значение **Нет**, ставка в головной аренде устанавливается в значение поля **Приростная ставка процента на заемный капитал** на странице **Сведения о книге**, независимо от типа перехода книги.

4. Установите для параметра **Разрешить сторнирования амортизации для версии закрытой книги** значение **Да**, чтобы разрешить сторнирование проводок по затратам на амортизацию. Проводки расходов могут быть сторнированы, даже если версия книги закрыта.

    > [!NOTE]
    > Рекомендуется оставить для этого параметра значение **Нет**. Настройка этого параметра используется в качестве проверки и управления, чтобы предотвратить случайную амортизацию закрытой версии книги. Если для параметра установлено значение **Нет**, вы помогаете сохранить точные расчеты остаточной стоимости и будущей амортизации.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
