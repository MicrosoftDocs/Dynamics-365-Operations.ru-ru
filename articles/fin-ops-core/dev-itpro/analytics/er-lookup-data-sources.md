---
title: Настройка источников данных поиска для использования параметров для приложения электронной отчетности
description: В этой статье объясняется, как настроить источники данных поиска (для подстановки) в форматах электронной отчетности (ER), чтобы использовать параметры для конкретного приложения электронной отчетности.
author: kfend
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
ms.openlocfilehash: f3ce5837b1d20860588848a1b518b3d801a05db4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285132"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Настройка источников данных поиска для использования параметров для приложения электронной отчетности 

[!include[banner](../includes/banner.md)]

Параметры, зависящие от приложения [электронной отчетности (ER)](general-electronic-reporting.md), позволяют вам настраивать фильтрацию данных в формате электронной отчетности, чтобы они основывались на наборе абстрактных правил. Этот набор правил может быть настроен для использования источника данных типа **Поиск**, доступного в формате электронной отчетности. Можно затем указать реальные правила помимо разработчиков компонентов электронной отчетности, используя пользовательский интерфейс, который автоматически создается на основе настроек источника данных **Поиск** соответствующего формата электронной отчетности и текущих данных юридического лица. В конечном счете, указанные правила будут доступны из источника данных **Поиск** в формате электронной отчетности при выполнении этого формата электронной отчетности.

> [!NOTE]
> Используйте настроенные источники данных для редактируемого формата электронной отчетности, чтобы указать, какие данные приложения используются для настройки реальных правил.

Используйте [Конструктор операций электронной отчетности](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) для перевода источника данных типа **поиска** в формат электронной отчетности. Источник данных должен быть настроен для описания внешнего вида абстрактных правил, включая следующие:

   - Набор параметров определенного типа данных, значение которого указывается для указания одного правила.
   - Тип значения определенного типа данных, возвращаемых одним правилом, когда это правило считается наиболее подходящим среди других правил.

Можно настроить следующие типы источников данных **поиска** в зависимости от типа значения, возвращаемого любым настроенным правилом:

   - Используйте тип **Модель данных\Поиск**, если необходимо вернуть значение перечисления модели.
   - Используйте тип **Операции Dynamics 365\Поиск** при необходимости возврата значения перечисления приложения или значения [расширенного типа данных](../extensibility/extensible-edts.md) приложения.
   - Используйте тип **Перечисление форматов\Поиск**, если необходимо вернуть значение перечисления форматов.

На следующем рисунке показано, как можно настроить перечисление форматов в образце формата электронной отчетности.

   ![Отображение перечисления формата в качестве базы для настроенного источника данных поиска.](./media/er-lookup-data-sources-img1.gif)

На следующем рисунке показаны компоненты формата, которые были настроены для составления отчета о других типах налогов в отдельном разделе созданного отчета.

   ![Отображение разделов формата для отдельных типов налогов в отчете.](./media/er-lookup-data-sources-img2.png)

На следующем рисунке показано, как конструктор операций электронной отчетности позволяет добавить источник данных **Перечисление форматов\Поиск**.  Добавленный источник данных настраивается, возвращая значение перечисления форматов `List of taxation levels`.

   ![Добавление источника данных электронной отчетности из типа "Перечисление форматов\Поиск".](./media/er-lookup-data-sources-img3.gif)

На следующем рисунке показано, как настроить источник данных для использования поля **кода** списка записей **Model.Data.Tax** источника данных **Модель** в качестве параметра, который должен быть указан для каждого настраиваемого правила.

![Настройка параметров добавленного источника данных типа "Перечисление форматов\Поиск".](./media/er-lookup-data-sources-img4.gif)

Добавленный источник данных `Model.Data.Tax` настраивается для указания налогового кода для каждого настроенного правила путем доступа к записям таблицы приложения **TaxTable**.

   ![Проверка источника данных поиска для одной компании для "Перечисление форматов\Поиск".](./media/er-lookup-data-sources-img5.gif)

Можно настроить правила поиска для выбранного формата ER, используя пользовательский интерфейс, который автоматически выравнивается по структуре настроенного источника данных. В настоящее время этот интерфейс пользователя требует, чтобы для каждого правила было указано возвращаемое значение в качестве значения перечисления формата `List of taxation levels`, а также налоговый код в качестве параметра.

   ![Настройка правил для настроенного источника данных.](./media/er-lookup-data-sources-img6.gif)

На следующем рисунке показано, как можно настроить источник данных `Model.Data.Summary.LevelByLookup` для типа **Вычисляемое поле** для вызова настроенного источника данных **Поиск**, предоставляющих необходимые параметры. Чтобы обработать этот вызов в среда выполнения, в списке настроенных правил в заданной последовательности будет обнаружено первое правило, удовлетворяющее заданным условиям. В этом примере это правило, содержащее налоговый код, который соответствует указанному коду. В результате будет найдено наиболее подходящее правило, а для этого источника данных будет возвращено значение перечисления, настроенное для найденного правила.

> [!NOTE]
> Если применимое правило не найдено, создается исключение. Чтобы не допустить подобных исключений, настройте дополнительные правила в конце списка правил, чтобы обрабатывать случаи, когда не задано ненастроенное значение или значение не указано. Используйте параметры **\*Не пустой**\* и **\*Пустой**\*, соответственно.  
>
> ![Добавление источника данных для вызова настроенного источника данных "Поиск".](./media/er-lookup-data-sources-img7.png)

При установке для параметра **Межфирменный** значения **Да** для редактируемого источника данных поиска, вы добавляете новый обязательный параметр **Компания** к набору параметров этого источника данных. Значение параметра **компания** должно быть указано во время выполнения, когда был вызван источник данных поиска. Когда код компании указывается во время выполнения, правила, настроенные для этой компании, используются для поиска наиболее подходящего правила, и возвращается соответствующее значение. На следующем рисунке показано, как это можно сделать и как изменяется набор параметров изменяемого источника данных.

   ![Проверка источника данных поиска между компаниями для типа "Перечисление форматов\Поиск".](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Выберите каждую компанию отдельно, чтобы настроить набор правил для этого источника данных поиска для редактируемого формата электронной отчетности. Исключение создается в среде выполнения, когда поиск между компаниями вызывается с кодом компании, для которой настройка поиска не была завершена.
>
> Убедитесь, что вы предоставляете разрешения для пользователя, который запускает формат электронной отчетности с межфирменным источником данных **Поиск** для получения доступа к данным каждой компании, входящей в область действия этого источника данных. В противном случае исключение создается в среда выполнения.

Начиная с версии 10.0.19, доступны расширенные возможности источников данных **поиска**. Когда вы устанавливаете для параметра **Расширенный** значение **Да** для редактируемого источника данных поиска, настроенный источник данных поиска преобразуется в структурированный источник данных, предоставляющий дополнительные возможности анализа настроенного набора правил. Следующая иллюстрация показывает это преобразование.

   ![Проверка структурированного источника данных поиска для "Перечисление форматов\Поиск".](./media/er-lookup-data-sources-img9.gif)

- Подэлемент **поиска** используется в качестве функции для поиска наиболее подходящего правила из набора настраиваемых правил на основе указанного набора параметров.
- Подэлемент **IsLookupResultSet** используется в качестве функции для принятия предоставленного значения базового источника данных перечисления и возвращения *логического* значения **Истина**, если набор правил содержит по крайней мере одно правило, для которого указанное значение перечисления было настроено как возвращаемое значение. Эта функция возвращает *логическое* значение **Ложь**, если нет настроенных правил для возврата предоставленного значения перечисления.
- Подэлемент **Настройка** предназначен в качестве функции, которая возвращает набор настроенных правил в виде записей списка записей. Возвращаемые значения и набор параметров настроенных правил представлены в каждой возвращаемой записи в виде полей соответствующих типов данных:

    - Возвращаемое значение представляется в поле **Результат поиска**.
    - Настроенные параметры представляются в виде полей с именами параметров (поле **код** в этом примере).

Дополнительные сведения о настройке источника данных **поиска** см. в [Настройка формата электронной отчетности для использования параметров, указанных для юридического лица](er-app-specific-parameters-configure-format.md). Сведения о настройке правил поиска см. в разделе [Настройка параметров формата электронной отчетности для юридического лица](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка форматов электронной отчетности для использования параметров, указанных для юридического лица](er-app-specific-parameters-configure-format.md)

[Настройка параметров формата электронной отчетности для юридического лица](er-app-specific-parameters-set-up.md)
