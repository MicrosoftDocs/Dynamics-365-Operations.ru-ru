---
title: Функция ER FORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FORMAT.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ee53ef3c1a8820f75580e2f9fbd48575d6a828f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746469"
---
# <a name="format-er-function"></a>Функция ER FORMAT

[!include [banner](../includes/banner.md)]

Функция `FORMAT` возвращает указанную строку как *строковое* значение после ее форматирования путем замены любых вхождений **%N** с *n*-м аргументом.

## <a name="syntax"></a>Синтаксис

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Аргументы

`string`: *Строка*

Ссылка на источник данных типа данных *Строка*, который должен быть отформатирован. Этот аргумент обязательный.

`argument 1`: *Строка*

Первый аргумент, который используется для замены вхождений **%1**. Этот аргумент обязательный.

`argument N`: *Строка*

*n*-й аргумент, который используется для замены вхождений **%2**, **%3** и т. д. Эти дополнительные аргументы являются необязательными.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Если аргумент не предусмотрен для параметра, параметр возвращается как **"%N"** в строке. Для значений типа *Вещественный* преобразование строки по умолчанию ограничено до двух десятичных знаков.

## <a name="example"></a>Пример

В следующем примере источник данных **PaymentModel** возвращает список записей клиентов с помощью компонента **Клиент**. Он возвращает значение даты обработки с помощью поля **ProcessingDate**.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

В формате электронной отчетности (ER), который создан для генерации электронного файла для выбранных клиентов, **PaymentModel** выбирается в качестве источника данных и управляет потоком операций. Если выбранный клиент остановлен на дату обработки отчета, исключение создается для информирования пользователя. Формула, которая предназначена для этого типа управления обработкой, может использовать следующие ресурсы:

- Метка SYS70894, которая имеет следующий текст:

    - **Для языка EN-US:** "Nothing to print"
    - **Для языка DE:** "Nichts zu drucken"

- Метка SYS18389, которая имеет следующий текст:

    - **Для языка EN-US:** "Customer %1 is stopped for %2."
    - **Для языка DE:** "Debitor '%1' wird für %2 gesperrt."

Вот выражение, которое можно разработать.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Если отчет обрабатывается для клиента **Litware Retail** 17 декабря 2015 г., в культуре **EN-US** и языке **EN-US**, эта формула возвращает следующий текст, который можно представить для пользователя в виде сообщения исключения:

*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*

Если этот же отчет обрабатывается для клиента **Litware Retail** 17 декабря 2015 г. в культуре **DE** и языке **DE**, эта формула возвращает следующий текст, который использует другой формат даты:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Следующий синтаксис применяется в формулах ER для меток:
>
> - **Для меток из ресурсов в приложении Microsoft Dynamics 365 Finance:** **\@X**, где **Х** — идентификатор метки в репозитории прикладных объектов (AOT)
> - **Для меток, которые находятся в конфигурациях ER:** **@"GER_LABEL:X"**, где **Х** — код метки в конфигурации ER

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]