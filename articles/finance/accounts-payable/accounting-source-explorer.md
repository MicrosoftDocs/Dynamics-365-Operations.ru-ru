---
title: Анализатор источника учета
description: Эта статья представляет информацию о странице Анализатора источника учета, которую можно использовать для подробного анализа сведений об источнике за учетными записями ГК.
author: RyanCCarlson2
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806442"
---
# <a name="accounting-source-explorer"></a>Анализатор источника учета

[!include [banner](../includes/banner.md)]

Эта статья представляет информацию о странице **Анализатора источника учета**, которую можно использовать для подробного анализа сведений об источнике за учетными записями ГК.

**Анализатор источника учета** — это страница, на которой представлены сведения об источнике. Его можно использовать как отдельное средство или для анализа сведений записей учета ГК. Например, эту страницу можно использовать для получения самых подробных сведений об источнике для сальдо в пробном балансе или для проводки по ваучеру. Затем можно использовать функцию **Экспорт в MS Excel** для дальнейшего анализа сведений в Microsoft Excel (например, в сводной таблице или сводном отчете).

Страница **Анализатор источника учета** всегда показывает ту же итоговую сумму на счет ГК, что и в ГК (например, в пробном балансе). Как и в пробном балансе, можно отобразить сегменты в отдельных столбцах. Достаточно выбрать соответствующий набора финансовых аналитик. 

Можно использовать параметры для определения интервала дат для анализа. Эта функциональность также напоминает функциональность в пробном балансе.

Для всех документов, которые используют платформу документа-источника, страница **Анализатор источника учета** показывает дополнительные сведения на основании распределений по бухгалтерским счетам и, если это применимо, распределений по бухгалтерским счетам проекта. Эти сведения включают значения **Тип денежных сумм**, **Проект**, **Мероприятие**, **Категория** и **Свойство строки**. Вот несколько примеров анализа, который можно выполнить:

- Отклонения между заказами на покупку и накладными поставщика, поскольку каждое отклонение представлено типом денежной суммы, например отклонение по накладным расходам.
- Оплачиваемые и неоплачиваемые часы и расходы по проекту, бизнес-единице и счету ГК.

Для документов-источников, которые используют понятие удостоверений ссылок документа-источника, страница **Анализатор источника учета** показывает еще больше сведений, таких как значения **Клиент**, **Поставщик**, **Работник**, **Продукт**, **Количество**, **Текст единиц измерений** и **Описание**. Вот несколько примеров анализа, который можно выполнить:

- Гостиничные расходы на бизнес-единицу и бренд гостиницы за финансовый период на основании отчетов по расходам.
- Скидки по поставщику, продукту и подразделению.

В случае этих документов также можно перейти к фактическому документу-источнику со страницы **Анализатор источника учета**.

> [!NOTE]
> По состоянию на версию 10.0.31 новая функция **Расширенной фильтрации анализатора источников учета** доступна в разделе Управление функциями. Эта функция заменяет кнопку **Обновить** для обеспечения более надежного функционала расширенных запросов, который напоминает доступные на странице **Проводки по ваучеру** инструменты. Расширенный фильтр позволяет выполнять фильтрацию по аналогичным полям на странице **Запрос проводок по ваучеру**, например по **Счету учета**, **Бизнес-единице** **Центру затрат** и **Подразделению**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
