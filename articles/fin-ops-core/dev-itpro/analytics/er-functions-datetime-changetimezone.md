---
title: Функция ER CHANGETIMEZONE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности (ER) CHANGETIMEZONE.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 48e96cfbc19503daf6a20363c4520c765f11a249
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647953"
---
# <a name="changetimezone-er-function"></a>Функция ER CHANGETIMEZONE

[!include [banner](../includes/banner.md)]

Функция `CHANGETIMEZONE` возвращает значение *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* в формате UTC (Greenwich Mean Time \[GMT\]), которое преобразуется из заданного значения даты/времени одного часового пояса в значение даты/времени другого часового пояса.

## <a name="syntax"></a>Синтаксис

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Аргументы

`datetime`: *DateTime*

Значение типа дата/время в часовом поясе UTC, представляющее значение даты/времени, которое требуется преобразовать.

`base time zone`: *[Строка](er-formula-supported-data-types-primitive.md#string)*

Имя часового пояса, для которого заданное значение даты/времени смещается до преобразования.

`target time zone`: *Строка*

Имя часового пояса, в которое смещается преобразованное значение даты/времени во время преобразования.

## <a name="return-values"></a>Возвращаемые значения

*DateTime*

Итоговое значение даты/времени в часовом поясе UTC.

## <a name="usage-notes"></a>Примечания по использованию

Для указания исходных и целевых часовых поясов можно использовать имена часовых поясов, [указанных](https://data.iana.org/time-zones/releases/) [Internet Assigned Numbers Authority (IANA)](https://www.iana.org/) или [поддерживаемых](/windows-hardware/manufacture/desktop/default-time-zones) Microsoft Windows.

Во время выполнения исключение "Часовой пояс \<time zone name\> не существует" выдается, если предоставленное имя не найдено в списке IANA или в реестре Windows.

Для часовых поясов, в которых есть переход на летнее время, при преобразовании учитывается смещение экономии летнего времени в формате UTC. В процессе преобразования используется последняя доступная информация об этом смещении.

## <a name="example-1"></a>Пример 1

В этом примере используются имена часовых поясов для Windows.

Вы настраиваете источник данных **DSX** типа **Вычисляемое поле**. В нем содержится следующее выражение.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

При настройке выражения источника данных **DSY** типа **Вычисляемое поле** как `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, источник данных **DSX** возвращает текст **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Этот текст показывает, что разница времени между двумя предоставленными часовыми поясами 1 июня превышает 24 часа. Таким образом, преобразованное значение даты/времени — на один день раньше указанного значения даты/времени, так как базовый часовой пояс опережает целевой часовой пояс.

При настройке выражения источника данных **DSY** типа **Вычисляемое поле** как `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, источник данных **DSX** возвращает текст **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Этот текст показывает, что разница времени между двумя предоставленными часовыми поясами 1 декабря меньше 24 часов. Таким образом, преобразованное значение даты/времени совпадает с данным значением даты/времени.

> [!NOTE]
> Одно и то же выражение возвращает разное расхождение между предоставленными и преобразованным значениями даты/времени для одной и той же пары часовых поясов, так как для предоставленных часовых поясов в заданное время/дату будет разное смещение летнего времени UTC.

## <a name="example-2"></a>Пример 2

В этом примере используются имена часовых поясов IANA.

Вы настраиваете источник данных **DSX** типа **Вычисляемое поле**. В нем содержится следующее выражение.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

При настройке выражения источника данных **DSY** типа **Вычисляемое поле** как `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, источник данных **DSX** возвращает текст **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Этот текст показывает, что разница времени между двумя предоставленными часовыми поясами 1 июня превышает 24 часа. Таким образом, преобразованное значение даты/времени — на один день раньше указанного значения даты/времени, так как базовый часовой пояс опережает целевой часовой пояс.

При настройке выражения источника данных **DSY** типа **Вычисляемое поле** как `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, источник данных **DSX** возвращает текст **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Этот текст показывает, что разница времени между двумя предоставленными часовыми поясами 1 декабря меньше 24 часов. Таким образом, преобразованное значение даты/времени совпадает с данным значением даты/времени.

## <a name="example-3"></a>Пример 3

Вы настраиваете источник данных **DSX** типа **Вычисляемое поле**. В нем содержится следующее выражение.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

При настройке выражения источника данных **DSY** типа **Вычисляемое поле** как `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, источник данных **DSX** возвращает текст **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**. Этот текст показывает, что разница времени между двумя предоставленными часовыми поясами 1 июня превышает 24 часа. Таким образом, преобразованное значение даты/времени — на один день позже указанного значения даты/времени, так как целевой часовой пояс опережает базовый часовой пояс.

## <a name="example-4"></a>Пример 4

Можно получить отметку даты/времени из внешнего источника в виде текста, который не содержит сведений о часовом поясе. Однако может быть известен часовой пояс, в котором осуществляется находится источник. Например, вы получаете метку даты/времени **01/12/2021 12:55:00** из службы, управляемой в Испании. Чтобы правильно сохранить значение даты/времени в базе данных, необходимо выполнить следующее преобразование:

- Настройте источник данных **DSY** для типа **Вычисляемое поле** , чтобы преобразовать отметку даты/времени из текста в значение даты/времени в формате UTC.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Настройте источник данных **DSX** для типа **Вычисляемое поле** для смещения преобразованного значения даты/времени в UTC как значение даты/времени для часового пояса внешнего источника.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> При использовании функции `CHANGETIMEZONE` для преобразования даты/времени имейте в виду, что все значения даты/времени хранятся в базе данных в качестве значения часового пояса UTC. Если это значение может быть представлено на страницах приложения, оно преобразуется. Преобразование учитывает часовой пояс, который [устанавливается](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) в качестве предпочитаемого для пользователя приложения, выполнившего вход в систему.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]