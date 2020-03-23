---
title: Добавление уведомления об авторском праве
description: В этом разделе описывается, как добавить уведомление об авторском праве на веб-сайт электронной коммерции.
author: psimolin
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 54b48ee74bc9d9f2b77f0584a0bf1739a8dfdbdb
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025490"
---
# <a name="add-a-copyright-notice"></a>Добавление уведомления об авторском праве


[!include [banner](includes/banner.md)]

В этом разделе описывается, как добавить уведомление об авторском праве на веб-сайт электронной коммерции.

## <a name="prerequisites"></a>Необходимые условия

Перед добавлением уведомления об авторском праве на сайт необходимо иметь следующие компоненты:

- Шаблон, содержащий общий фрагмент нижнего колонтитула.
- Страница, использующая этот шаблон.

## <a name="add-a-copyright-notice"></a>Добавление уведомления об авторском праве

Чтобы добавить уведомление об авторских правах в нижнюю часть каждой страницы, использующей конкретный шаблон, выполните следующие действия.

1. Перейдите к разделу **Фрагменты**, затем выберите **Создать фрагмент страницы**.
1. В диалоговом окне выберите модуль **Нижний колонтитул** и название фрагмента. Например, введите **Нижний колонтитул-авторские права**.
1. Нажмите **ОК**.
1. В области переходов выберите кнопку с многоточием (**...**) рядом с пунктом **Нижний колонтитул**, затем выберите **Добавить модуль**.
1. В диалоговом окне выберите **Категория нижнего колонтитула**, затем выберите **ОК**.
1. В области переходов выберите кнопку с многоточием рядом с пунктом **Категория нижнего колонтитула**, затем выберите **Добавить модуль**.
1. В диалоговом окне выберите **Блок текста**, затем выберите **ОК**.
1. В области переходов выберите **Блок текста**.
1. В области свойств справа в поле **Абзац** добавьте сообщение об авторском праве. Например, введите **(C) Fabrikam 2019**.
1. Выберите **Сохранить**, выберите **Вернуть**, затем выберите **Опубликовать**.
1. Перейдите к пункту **Шаблоны**, выберите шаблон, затем выберите **Извлечь**.
1. В разделе **Структура страницы** разверните **Основной текст**, затем разверните пункт **Страница по умолчанию**.
1. Нажмите кнопку с многоточием рядом в пунктом **Слот нижнего колонтитула**, затем выберите **Добавить фрагмент**.
1. Выберите созданный ранее фрагмент, затем выберите **Выбрать**.
1. Верните шаблон и опубликуйте его.

Нижний колонтитул, содержащий уведомление об авторском праве, автоматически появляется внизу всех страниц, использующих выбранный шаблон.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Добавление логотипа](add-logo.md)

[Выбор темы сайта](select-site-theme.md)

[Работа с переопределением файлов CSS](css-override-files.md)

[Добавление значка сайта](add-favicon.md)

[Добавление приветственного сообщения](add-welcome-message.md)

[Добавление языков на сайт](add-languages-to-site.md)

[Добавление кода скрипта на страницы сайта для поддержки телеметрии](add-telemetry.md)
