---
title: Добавление сведений об управлении кредитом для клиентов
description: В этом разделе объясняется, как добавить информацию по управлению кредитом для клиента.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7ad1b8ff9f00dba41c02e6426662a03c6c6211b
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015369"
---
# <a name="add-credit-management-information-for-customers"></a>Добавление сведений об управлении кредитом для клиентов

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

После настройки параметров управления кредитами можно добавить дополнительные сведения для каждого клиента. Эти сведения контролируют процессы управления кредитами, а также предоставляют дополнительную информацию, помогающую участникам группы сбора задолженности управлять клиентами.

## <a name="customer-information"></a>Информация о клиенте

Сведения о клиенте можно добавить на экспресс -вкладке **Кредит и сбор задолженностей** на странице **Все клиенты** (**Расчеты с клиентами \> Клиенты \> Все клиенты**).

1. Установите для параметра **Кредит без ограничений** значение **Да**, если клиент не должен ограничиваться проверками кредитного лимита.
2. Установите для параметра **Исключить из управления кредитом** значение **Да**, чтобы исключить клиента из всех действий, которые обычно происходят в процессах управления кредитованием.
3. Выбор группы управления кредитом для клиента.
4. Чтобы рассчитать кредитный лимит в валюте клиента, введите в поле **Кредитный лимит в валюте клиента** кредитный лимит клиента. Кредитный лимит в валюте компании будет преобразован с использованием валютных курсов, которые определяются типом валютного курса с кредитным лимитом, выбранным в параметрах управления кредитом.
5. В поле **Дата последней проверки** введите дату, когда кредитный лимит клиента был последний раз просмотрен менеджером по кредиту.
6. В поле **Дата следующей плановой проверки** введите дату, когда планируется проверить и обновить кредит клиента.
7. В поле **Подходящий кредитный лимит** введите наибольший кредитный лимит, который может быть назначен клиенту, в зависимости от обзора истории кредита клиента. Подходящий кредитный лимит может отличаться от кредитного лимита, который отображается на экспресс- вкладке **Кредит и сбор задолженностей**.
8. В поле **Подходящая валюта кредитного лимита** введите подходящую валюту кредитного лимита.
9. В поле **Подходящая дата кредитного лимита** введите дату создания кредитного лимита.
10. В поле **Состояние кредитного счета** введите состояние кредитного счета клиента.
11. В поле **Причина состояния** введите причину, связанную со статусом счета.
12. Установите для параметра **С агентством** значение **Да**, чтобы указать, что клиент в данный момент назначен кредитному агентству. Это значение предназначено только для информационных целей. В процессах управления кредитом оно не используется.
13. Установите для параметра **Заголовок** значение **Да**, чтобы указать, что для компании используется заголовок. Это значение предназначено только для информационных целей. В процессе управления кредитом оно не используется.
14. В поле **Дата начала бизнеса** введите дату, когда клиент впервые начал выполнять коммерческую деятельность. Эти сведения используются при создании показателей риска.
15. В поле **Срок обслуживания клиента** введите дату, когда первые проводки были обработаны для данного клиента. Эти сведения используются при создании показателей риска.
16. Введите примечания, которые кредитная группа может использовать для дальнейшей оценки кредитоспособности клиента.

Обратите внимание, что часть информации, отображаемая на странице **Клиент**, создается другим процессом:

- В поле **Дата окончания срока действия кредитного лимита** отображается дата истечения срока действия кредитного лимита. Если это поле не задано, кредитный лимит клиента не будет действовать.
- В поле **Дата кредитного лимита** отображается дата создания кредитного лимита. Это поле обновляется всякий раз, когда кредитный лимит корректируется.
- Временные кредитные лимиты переопределяют кредитный лимит клиента для периода. Они используются вместо кредитного лимита для расчета общего кредитного лимита. Эта информация отображается только в том случае, если имеется активный кредитный лимит. Временные кредитные лимиты можно добавить через корректировку кредитного лимита.
- В поле **Страхование и гарантии** отображается общая стоимость страхования и гарантий, которая может увеличить кредитный лимит для клиента.
- В поле **Общий кредитный лимит** отображается окончательный кредитный лимит для клиента. Общий кредитный лимит включает страховку и гарантии и временные кредитные лимиты.

## <a name="temporary-credit-limits"></a>Временные кредитные лимиты

Временные кредитные лимиты переопределяют кредитные лимиты клиента для указанного периода. Временные кредитные лимиты можно добавить через корректировку кредитного лимита. Корректировка кредитного лимита позволяет менеджерам по кредитам обновлять кредитные лимиты и даты истечения срока действия отдельного клиента, группы клиентов или всех клиентов через процесс разноски.

Можно создать записи корректировки кредитного лимита на странице **Корректировки кредитного лимита** (**Управление кредитом \> Корректировки кредитного лимита \> Корректировки кредитного лимита**).

## <a name="create-insurance-policies-and-guarantees"></a>Создание страховых полисов и гарантий

Можно создать один или несколько страховых полисов и гарантий для каждого клиента. После этого их можно использовать для расчета обязательств, которые ваша компания предлагает для кредитования клиента. Страховые полисы и гарантии также могут быть включены в кредитный лимит клиента.

Можно создавать страховые полисы и гарантии на странице **Все клиенты** (**Расчеты с клиентами \> Клиенты \> Все клиенты**). Выберите клиента, а затем на панели операций на вкладке **Управление кредитом** выберите **Страхование и гарантии**.

> [!NOTE]
> В следующей процедуре вы выбираете страховщика или поручителя из глобальной адресной книги. Поэтому перед началом выполнения этой процедуры необходимо убедиться, что в глобальную адресную книгу добавлены страховщики и поручители.

1. В поле **Код** введите **Гарантия** или **Страхование**.
2. В поле **Тип гарантии/страхования** выберите один из ранее настроенных типов гарантии или страховки.
3. В поле **Страховщик/поручитель** вы выбираете страховщика или поручителя из глобальной адресной книги. 
4. Если выбрано **Страхование** в поле **Код**, в поле **Тип покрытия полиса** выберите один из ранее настроенных типов покрытия. Выбор типа покрытия полиса для гарантии невозможен.
5. В поле **Код** введите идентификационный код полиса. Этот код обычно является номером политики.
6. В поле **Действует** введите дату начала действия страхового полиса или гарантии.
7. В поле **Срок действия** введите дату истечения срока действия страхового полиса или гарантии.
8. В поле **Значение** введите значение страхового полиса или гарантии. Это значение является полной суммой полиса.
9. В поле **Валюта** выберите код валюты для значения полиса. 
10. В поле **Обновить кредитный лимит** укажите процент от **0** до **100**. Этот процент будет применяться к значению полиса, а полученная сумма будет использоваться для увеличения кредитного лимита, используемого в расчетах кредитного лимита. Расчетное значение отображается **Общий кредитный лимит, страхование и гарантии** на экспресс-вкладке **Кредит и сбор задолженностей** на странице **Клиенты**.

    Рассмотрим пример:

    - Кредитный лимит (A) 100 000.
    - Значение полиса (B) — 50 000.
    - Процент **Обновить кредитный лимит** (C) — 50,00.
    
    В этом случае эффективный кредитный лимит равен 125 000 (= A + \[B × C\]).

11. Установите флажок **Включено в обязательства**, чтобы уменьшить кредитный лимит, используемый в расчетах кредитного лимита, по полному значению полиса. Если этот флажок установлен, значение, рассчитанное при указании процента **Обновить кредитный лимит**, не будет использоваться в расчетах кредитного лимита.

    Рассмотрим пример:

    - Кредитный лимит (A) 100 000.
    - Значение полиса (B) — 50 000.
    - Процент **Обновить кредитный лимит** (C) — 50,00.

    В этом случае эффективный кредитный лимит равен 125 000 (= A + \[B × C\]).
    
    Однако, если установлен флажок **Включено в обязательства**, значение **Обновить кредитный лимит** 50 000 (= 50,00% от 100 000) удаляется, а значение обязательств равно 75 000 (= A + \[B × C\] – B).