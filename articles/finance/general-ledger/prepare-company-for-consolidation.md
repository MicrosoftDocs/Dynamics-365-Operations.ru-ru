---
title: Подготовка юридического лица для процесса консолидации
description: Во время консолидации проводки из нескольких наборов счетов юридического лица собираются в единый набор счетов юридического лица. В этой статье объясняется, как подготовить юридическое лицо для консолидации.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 2a3d4645c79ec30df2bbb7a32a82a59fdb7016e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894036"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Подготовка юридического лица для процесса консолидации

[!include [banner](../includes/banner.md)]

Во время консолидации проводки из нескольких наборов счетов юридического лица собираются в единый набор счетов юридического лица. В этой статье объясняется, как подготовить юридическое лицо для консолидации.

> [!NOTE]
> Рекомендуется использовать Management Reporter для Microsoft Dynamics 365 Finance для объединения финансовых результатов для нескольких юридических лиц в консолидированном формате. Management Reporter позволяет создавать консолидированные финансовые отчеты для юридических лиц, использовать Excel для импорта данных консолидации из других источников и перевода сумм в любое количество валют отчетности без выполнения процесса консолидации в Dynamics 365 Finance.

Из консолидированного юридического лица также можно напечатать отчеты, например финансовые отчеты. Однако консолидированное юридическое лицо нельзя использовать для ежедневных проводок.

Можно консолидировать данные из юридических лиц, использующих базы данных, отличные от консолидированного юридического лица. Этот процесс консолидации называется *консолидацией импорта*. Или же юридические лица могут использовать ту же базу данных, что и консолидированное юридическое лицо. Этот процесс консолидации называется *консолидацией в интерактивном режиме*.

Консолидированное юридическое лицо собирает результаты и сальдо филиалов. Чтобы подготовить консолидированное юридическое лицо к консолидации, выполните следующие действия.

1. Перейдите в раздел **Главная книга \> Настройка \> Организация \> Юридические лица**.
2. Выберите **Создать**, чтобы создать юридическое лицо, которое будет консолидированным юридическим лицом.
3. Выберите флажок **Использовать для процесса финансовой консолидации**, затем введите сведения о консолидированном юридическом лице. Обязательно введите эту информацию именно в том виде, в котором она будет отображаться в финансовых отчетах для консолидированного юридического лица.
4. Закройте страницу.
5. Выберите консолидированное юридическое лицо в поле в верхнем правом углу страницы, затем выберите **ОК**.
6. Перейдите в раздел **Главная книга \> Настройка \> Книга учета**.
7. Выберите план счетов, финансовый календарь, валюту учета, дополнительную валюту отчетности и тип по умолчанию валютного курса для консолидированного юридического лица. 
8. Перейдите в раздел **Главная книга \> Настройка \> Валюта \> Валютные курсы**.
9. Настройте курсы обмена валют за соответствующие периоды для валют дочерних юридических лиц.
10. Закройте страницу.
11. Если у консолидированного юридического лица есть подразделения, в которых используется иностранная валюта, выполните следующие действия:

    1. Перейдите в раздел **Главная книга \> Настройка \> Разноска \> Счета для автоматических проводок**.
    2. В поле **Тип разноски** выберите соответствующий счет:

        - Если у юридического лица есть иностранные дочерние компании, которые финансово или операционно взаимосвязаны с родительским юридическим лицом, выберите соответствующий счет для типа разноски **Счет прибыли и убытка для разниц консолидации**.
        - При консолидации подразделения, которое не зависит от родительского юридического лица в финансовом и операционном плане, или при консолидации юридического лица, имеющего результаты нескольких независимых подразделений, и при использовании методов трансляции для консолидации данных выберите соответствующий счет для типа разноски **Балансовый счет для разниц консолидации**.

    3. В поле **Счет ГК** введите счета ГК, которые должны использоваться для переоценок в иностранной валюте.
    4. Закройте страницу.

    Если консолидированное юридическое лицо создается в начале периода, суммы в валюте можно переоценить, так как валютные курсы изменяются в течение периода консолидации.

Теперь консолидированное юридическое лицо настроено для периодического задания **Консолидировать**. Можно выполнить консолидацию импорта или интерактивную консолидацию.

- Для выполнения консолидации импорта перейдите в раздел **Главная книга \> Периодические \> Консолидировать \> Консолидировать \[импорт из\]**.
- Для выполнения интерактивной консолидации перейдите в раздел **Главная книга \> Периодические \> Консолидировать \> Консолидировать \[в Интернете\]**.

> [!NOTE]
> Прежде чем можно будет обработать консолидацию, вы должны подготовить подразделения юридического лица к консолидации. Дополнительные сведения см. в разделе [Настройка дочернего юридического лица для консолидации](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
