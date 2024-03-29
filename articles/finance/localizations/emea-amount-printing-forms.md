---
title: Обновление способа отображения сумм в отчетах и документах
description: В этой статье представлена информация о том, как обновить способ отображения сумм в отчетах и других документах для Эстонии, Латвии, Литвы, Польши, Чешской Республики, Венгрии и России.
author: AdamTrukawka
ms.date: 01/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264254
ms.search.form: Currency
ms.openlocfilehash: f9ddb4e2616c858bf8d68e485b88bf4fb7d9d5c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273819"
---
# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Обновление способа отображения сумм в отчетах и документах

[!include [banner](../includes/banner.md)]

В этой статье представлена информация о том, как обновить способ отображения сумм в отчетах и других документах для Эстонии, Латвии, Литвы, Польши, Чешской Республики, Венгрии и России.

Для юридических лиц в Эстонии, Латвии, Литве, Польше, Чехии, Венгрии и России можно настроить полные имена и краткие имена денежных единиц и субединиц. Эти имена можно использовать для преобразования представления сумм в документах и отчетах. Например: сумма **100,20 литов** может отображаться как **100 литов 20 центов**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Настройка полных и кратких имен для денежных единиц и субединиц
Чтобы настроить полные и краткие имена денежных единиц и субединиц для языка, выполните следующие действия:

1. Откройте страницу **Валюты**.
2. Выбор валюты.
3. В области действий выберите **Склонение**.
4. Чтобы добавить полное имя и краткое имя для языка, выберите **Создать** и введите сведения в следующие поля.

   |             Поле                                                           |                        описание                                                                                                                                                                                                                                                |
   |------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                       <strong>Язык</strong>                        |                                                                                                               Выбрать язык для текущего текста.                                                                                                                |
   |    <strong>Именительный падеж единственное число (имя группы полей единиц)</strong>    |                                                                                       Введите форму единственного числа для валюты. Например, форма единственного числа для литов — лит.                                                                                       |
   |     <strong>Именительный падеж множественное число (имя группы полей единиц)</strong>     | Введите форму множественного числа для валюты. Например, введите "Литы". <strong>Примечание</strong>. Поля <strong>Родительный падеж единственное число</strong> и <strong>Родительный падеж множественное число</strong> доступны в зависимости от языка, выбранного в поле <strong>Язык</strong>. |
   | <strong>Поле именительного падежа единственного числа (имя группы полей частей)</strong> |                                                                                                        Введите форму единственного числа субединицы для валюты.                                                                                                         |
   |     <strong>Именительный падеж множественное число (имя группы полей частей)</strong>     |                                                                                                         Введите форму множественного числа субединицы для валюты.                                                                                                          |
   |    <strong>Сокращенное наименование единиц (группа полей краткого имени)</strong>    |                                                                                         Введите код ISO для идентификации валюты. Например, введите LTL для определения литовских литов.                                                                                         |
   |   <strong>Сокращенное наименование частей (группа полей краткого имени)</strong>    |                                                                                               Введите обозначение субединицы валюты. Например, введите "Центы".                                                                                               |
   |       <strong>Соединительный союз "и" между единицами и частями</strong>       |                                     Установите этот флажок для печати союза «и» между единицами и частями валюты. Например, в накладных или отчетах сумма 100,20 литов будет отображаться как «100 литов и 20 центов».                                      |
   |       <strong>Род</strong>       |  Выберите **Мужской**, **Женский** или **Нейтральный**. Этот параметр может влиять на текст склонения суммы, которая отображается в тексте на локальном языке по кассовому ордеру. Например, при настройке значения **Пол** для валюты EUR как **Нейтральный**, сумма 1,01 EUR записывается на чешском языке в кассовый ордер как *Jedno euro 01 cent*.  |

5. Нажмите **Сохранить**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
