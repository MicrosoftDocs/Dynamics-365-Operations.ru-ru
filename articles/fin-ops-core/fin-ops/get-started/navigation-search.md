---
title: Навигационный поиск
description: Этот раздел описывает порядок использования функции поиска для навигации к страницам.
author: aneesmsft
ms.date: 04/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2fc57579f817d2735aaa94a5f6834185961dab39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750236"
---
# <a name="navigation-search"></a>Навигационный поиск

[!include [banner](../includes/banner.md)]

Этот раздел описывает порядок использования функции поиска для навигации к страницам.

Приложение включает несколько областей и страниц, с помощью которых можно выполнять различные задачи. Чтобы быстро найти страницы, которые требуются для завершения задач, используйте функцию навигационного поиска.

Для использования этой функции щелкните значок **Поиск**, чтобы открыть окно **Поиск**. Затем введите одно или несколько слов в поле. Система немедленно выполнит поиск соответствующих страниц в приложении, которые соответствуют введенным словам. Например, если ввести "накладная поставщика", система отобразит результаты, которые соответствуют этим словам.

> [!NOTE]
> Поле **Поиск** помогает находить страницы и переходить к ним. С его помощью невозможно найти определенные данные или действия.

[![поле-поиска](media/navigation-search.png "Поле поиска")

## <a name="quickly-navigate-to-a-particular-page"></a>Быстрый переход на определенную страницу

Функция навигационного поиска — также отличный способ быстро переходить к определенной странице. Например, если вы сотрудник отдела по расчетам с поставщиками и часто используете страницу **Журнал платежей**, вы можете ввести "журнал платежей" в поле **Поиск**. Поскольку введенный запрос точно совпадает с заголовком страницы, страница будет указана вверху результатов поиска, и вы можете быстро перейти к ней.

В списке результатов поиска отображается заголовок страницы, а также навигационный путь. Это показывает расположение страницы в приложении. Также благодаря этому можно отличить две или более похожих страниц в результатах.

Когда вы ищете страницу, вводимый запрос сопоставляется с заголовком страницы и ее навигационным путем. Например, если ввести "с клиентами" в поле **Поиск**, отобразятся результаты для страниц, доступных вам в области "Расчеты с клиентами", даже если заголовки страниц не включают слова "с клиентами".

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Быстрый переход к странице на основе имени технической формы

Функция навигационного поиска также включает востребованную функцию для опытных пользователей: способность быстро переходить к странице на основании имени технической формы. Множество пользователей настолько знакомы с системой, что они знают точные имена форм, с которыми они работают. Если вы принадлежите к их числу, вы можете ввести **форма:**, а затем ввести имя искомой формы. Например, если ввести **форма: vendinvoice**, в результатах поиска отобразится все страницы, на которых имя формы начинает с **vendinvoice**.

## <a name="administration-and-security"></a>Администрирование и безопасность

В целях администрирования и обеспечения безопасности с помощью функции навигационного поиска можно найти только два типа результатов:

- Страницы, которые включены в текущей конфигурации (с помощью конфигурационных ключей).
- Страницы, к которым у пользователя есть доступ на основании его роли.

Список результатов поиска ограничен 10 позициями. Если в результатах отсутствует искомый элемент, уточните или обновите запрос поиска.

## <a name="development"></a>Разработка

С точки зрения разработки функцию навигационного поиска легко использовать, поскольку отсутствует задержка между развертыванием пунктов меню и их способностью отображаться в результатах поиска. Пока пункты меню связаны с областью перехода или панелью мониторинга, они автоматически становятся доступны для поиска.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]