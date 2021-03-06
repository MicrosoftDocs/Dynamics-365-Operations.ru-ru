---
title: Что нового или что изменено в мобильном приложении Warehouse Management
description: В этой теме перечислены новые и измененные функции для каждой выпущенной версии мобильного приложения Warehouse Management для Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261796"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Что нового или что изменено в мобильном приложении Warehouse Management

[!include [banner](../includes/banner.md)]

В этой теме перечислены новые функции, исправления, улучшения и известные проблемы для каждой выпущенной версии мобильного приложения Warehouse Management для Microsoft Dynamics 365 Supply Chain Management.

## <a name="version-2060"></a>Версия 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Новые функции, исправления и улучшения в 2.0.6.0

Эта версия вводит следующие новые функции, исправления и улучшения:

- Демонстрационный режим теперь показывает все метки на языке устройства.
- Вы реже получаете следующее сообщение об ошибке: "Не удается найти подходящее представление для указанного размера".
- Минимальная высота карточек работы была увеличена (для случаев, когда в списке работы настроены три или меньше полей).
- Границы (обесцвечивание) в нижней части карточек сведений были улучшены.
- Недопустимые символы в файлах XML, которыми система обменивается с сервером, теперь обрабатываются правильно. (Например, непечатаемые символы теперь обрабатываются правильно и больше не приводят к тому, что приложение перестало отвечать.)
- Ошибки HTTP (например, "ошибка 503") при отправлении запроса на сервер теперь обрабатываются правильно.
- Показывается ошибка, список параметров больше не отображается автоматически для элементов управления полей со списком.
- Приложение больше не перестает отвечать из-за ориентации дисплея, которая выбрана в настройках пользователя.
- Изображения продуктов теперь отображаются в средах самообслуживания. (Это изменение распространяется только на версии с низким разрешением. Служба управления файлами не поддерживает полноразмерные изображения в средах самообслуживания.)
- Исправлена проблема, связанная с короткими комплектациями с нулевым количеством.
- Приложение больше не перестает отвечать, когда карточка сведений показывает несколько одинаковых полей.

### <a name="known-issues-in-version-2060"></a>Известные проблемы в версии 2.0.6.0

В этой версии существуют следующие известные проблемы:

- Приложение (особенно список работ) становится медленнее с течением времени.
- **Версия для Windows:** когда USB используется для сканирования в Windows, несоответствующие результаты вызывают смешивание отсканированных символов.

## <a name="version-2050"></a>Версия 2.0.5.0

Эта версия вводит следующие новые функции, исправления и улучшения:

- Секрет клиента больше не скрыт в настройке параметров соединения.
- Теперь вы можете долго нажимать на любой текст, чтобы увидеть его полностью.
- Сообщение об ошибке при отсутствии разрешений на хранение улучшено.
- Для некоторых потоков были добавлены новые последовательности управления.
- Кнопка отправки больше не становится доступной (что неправильно) из-за размера окна.
- Ползунки теперь могут работать на меньших экранах при использовании больших размеров кнопок.
- Наложение из четырех кнопок больше не обрезано.
- Клавиатура теперь поддерживает кнопку удаления.
- Исправлена проблема яркости, которая может возникнуть при нажатии клавиатуры.
- Исправлены различные проблемы с демонстрационными данными.
- Исправлена проблема, которая затронула числовые поля на странице сведений.
- Экранная клавиатура больше не исчезает на некоторых устройствах.
- Исправлены различные ошибки пользовательского интерфейса (UI), такие как ошибки, влияющие на цвет фона и позиционирование.
- Улучшен русский пользовательский интерфейс.
- Исправлены различные проблемы, из-за которых система перестала отвечать.
- Проблема, связанная с повторным открытием калькулятора, устранена.
- **Версия для Android:** исправлена проблема, из-за которой Android 4.4 переставал отвечать при запуске.
- **Версия для Android:** минимальный масштаб был сокращен до 50 процентов.

## <a name="version-2040"></a>Версия 2.0.4.0

Версия 2.0.4.0 стала первой общедоступной версией мобильного приложения Warehouse Management.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Новые функции, исправления и улучшения в 2.0.4.0

Эта версия содержит следующие новые функции, исправления и улучшения, которые не были доступны в предварительной версии:

- Если карточка сведений включает в себя две метки, которые имеют одинаковые данные, одна из меток скрыта.
- Специальные символы теперь отображаются по умолчанию, и возможность скрыть их была удалена из настроек пользователя.
- Отключенные кнопки отправки теперь показаны как недоступные в компактном представлении для портативных устройств.
- Изменение логики последовательности элементов управления обеспечивает более плавное масштабирование на устройствах. Поэтому меньше необходимости в настройке масштабирования шрифтов или кнопок.
- Тема цвета по умолчанию была изменена на *Темная*.
- Отсутствующий значок для отключенной кнопки отправки добавлен в представлении ленты.
- Исключения тайм-аута теперь переводят на страницу соединения вместо того, чтобы показывать ошибку в строке.
- Если нет действия отправки (например, **OK**, **Да**, **Принять**, **Готово** или **Завершено**), кнопка представления будет отключена.
- Стабильность приложений была улучшена.
- Существует исправление уязвимости безопасности [CVE--2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Версия для Windows:** исправлена проблема в Windows, когда меню не отвечало после того, как размер окна был изменен.

### <a name="known-issue-in-version-2040"></a>Известные проблемы в версии 2.0.4.0

В этой версии существуют следующие известные проблемы:

- Эта версия имеет проблемы с устройствами, которые используют Android 4.4. Могут возникнуть проблемы при использовании приложения в этой версии Android.
