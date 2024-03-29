---
title: Внедрение сторонних приложений
description: В этой статье описывается, как внедрять сторонние приложения для расширения функциональных возможностей продукта.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef5ed6c3c99d62010643940f3e2f158963ff0dc2
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123729"
---
# <a name="embed-third-party-apps"></a>Внедрение сторонних приложений

[!include [banner](../includes/banner.md)]

Многие клиенты используют ряд приложений для работы в своем бизнесе. Некоторыми из этих приложений являются веб-приложения сторонних производителей, работающие в сочетании с приложениями для управления финансами и операциями. Чтобы обеспечить более гладкое взаимодействие с пользователем, вы можете использовать функцию **Приложения полной страницы** для встраивания этих сторонних приложений непосредственно в ваши приложения для управления финансами и операциями (при условии, что эти сторонние приложения допускают внедрение). Таким образом, пользователи могут получить доступ к веб-сайтам и приложениям, которые им необходимы, без переключения вкладок или окон.

Прежде чем внедрять сторонние приложения в продукт, необходимо включить функцию **Приложения полной страницы** в управлении функциями. Затем можно использовать один из следующих методов для встраивания стороннего приложения или веб-сайта. Эти методы аналогичны методам, используемым для встраивания приложений на основе холста из Microsoft Power Apps в приложения для управления финансами и операциями.

- Внедрите приложение или веб-сайт на существующую страницу как новую страницу вкладки (сводная вкладка, экспресс-вкладка, колонка или рабочая область).
- Создайте новое взаимодействие на полную страницу для приложения или веб-сайта с панели мониторинга.

## <a name="embed-a-website-on-an-existing-page"></a>Внедрение веб-узла на существующую страницу

Используйте эту процедуру, если требуется дополнить существующую страницу в системе встроенным приложением.

1. Откройте страницу, на которой вы хотите внедрить приложение.
2. Откройте область **Добавить приложение**:

    1. Выберите **Параметры**, затем **Персонализация**, чтобы открыть панель инструментов **Персонализация**.
    2. Выберите **Дополнительно \> Добавить приложение**.

3. Выберите область страницы, где вы хотите добавить приложение. Эта область должна быть *контейнером вкладки* для сводной вкладки, экспресс-вкладки, колонки или рабочей области.
4. Выберите **Веб-сайт**.
5. Настройка внедренного приложения:

    - **Имя** — введите текст, который должен отображаться для вкладки, содержащей встраиваемое приложение. Часто требуется, чтобы этот текст был именем приложения.
    - **URL** — укажите расположение приложения.

    > [!IMPORTANT]
    > - Из соображений безопасности URL-адрес должен использовать HTTPS.
    > - Приложение или веб-сайт должны быть настроены таким образом, чтобы их можно было внедрить.

6. Выберите **Сохранить**, чтобы внедрить приложение на страницу. Приложение добавляется как последняя вкладка или раздел в группе.
7. Убедитесь, что приложение выглядит так, как ожидалось. Если приложение не отображается, см. раздел [Устранение неполадок](#troubleshooting) далее в этой статье.
8. Откройте селектор представлений и выберите **Сохранить** (если приложение должно быть связано с текущим представлением) или **Сохранить как** (чтобы сохранить приложение в других представлениях).

    Если на странице нет селектора представлений (например, если страница является диалоговым окном или рабочей областью), этот шаг можно пропустить.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Внедрение веб-сайта в качестве многостраничного взаимодействия с панели мониторинга

Используйте эту процедуру, если приложение, которое требуется внедрить, не связано с существующей страницей или если требуется только полностраничная работа с приложением внутри приложения для управления финансами и операциями.

1. Откройте панель мониторинга.
2. Выберите и удерживайте (или щелкните правой кнопкой мыши) панель мониторинга, выберите **Персонализация**, затем выберите **Добавить страницу**.
3. В области **Добавить страницу** выберите **Веб-сайт**.
4. Настройка внедренного приложения:

    - **Имя** — введите текст, который должен отображаться на плитке, добавляемой для встраиваемого приложения на панели мониторинга. Часто требуется, чтобы этот текст был именем приложения.
    - **URL** — укажите расположение приложения.

    > [!IMPORTANT]
    > - По соображениям безопасности URL-адрес должен использовать протокол HTTPS.
    > - Приложение или веб-сайт должны быть настроены таким образом, чтобы их можно было внедрить.

5. Выберите **Сохранить**, чтобы добавить приложение на панель мониторинга как новую плитку.
6. Выберите новую плитку на панели мониторинга и убедитесь, что приложение выглядит так, как ожидалось. Если приложение не отображается, см. раздел [Устранение неполадок](#troubleshooting) далее в этой статье.

## <a name="sharing-embedded-apps"></a>Совместное использование внедренных приложений

После внедрения приложения с помощью одного из методов, описанных в предыдущих разделах, может возникнуть необходимость совместного использования представления с другими пользователями системы. Для совместного использования внедренного приложения воспользуйтесь одним из следующих способов:

- **Опубликовать представление (рекомендуется):** если встроенное приложение сохранено в представлении, то, чтобы поделиться им, рекомендуется опубликовать представление для пользователей с соответствующими ролями безопасности в целевых юридических лицах. В этом случае встраиваемое приложение будет отображаться на этой странице только для выбранных пользователей. Дополнительные сведения о публикации представления см. в [Публикация представлений](saved-views.md#publishing-views).

    Можно также опубликовать приложение, встроенное в качестве полноэкранного из панели мониторинга. На панели мониторинга выберите и удерживайте (или щелкните правой кнопкой мыши) плитку, связанную с приложением, выберите **Персонализация** и выберите **Опубликовать страницу**. Отображается интерфейс, аналогичный *Публикация представлений*, и можно выбрать роли безопасности для публикации. В обновлении 10.0.21 или более поздней версии, если функция **Усовершенствованная поддержка юридических лиц для сохраненных представлений** включена, можно также опубликовать приложение в нужных юридических лицах.

- **Копировать персонализацию:** для страниц, не поддерживающих представления (например, диалоговых окон или рабочих областей) или полностраничного приложения можно скопировать персонализацию для соответствующих пользователей. Дополнительные сведения см. в разделе [Общий доступ к персонализациям](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Просмотр внедренных приложений

Для просмотра внедренного приложения на странице в приложениях для управления финансами и операциями откройте страницу, на которой находится внедренное приложение. Помните, что на некоторых страницах доступ к внедренным приложениям можно получить, нажав кнопку **Power Apps** на стандартной панели действий. Они могут также отображаться непосредственно на странице в виде новой вкладки, экспресс-вкладки или колонки либо в виде нового раздела в рабочей области.

## <a name="editing-or-removing-embedded-apps"></a>Редактирование или удаление внедренных приложений

После внедрения приложения на страницу можно изменить его конфигурацию (например, изменив метку раздела или URL-адрес). Или, возможно, придется удалить его со страницы. Чтобы изменить конфигурацию встраиваемого приложения или полностью удалить его, воспользуйтесь одной из следующих процедур.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Приложения, которые встроены в существующие страницы

1. Откройте страницу, где внедрено приложение.
2. Выберите **Параметры**, затем **Персонализация**, чтобы открыть панель инструментов **Персонализация**.
3. Выберите инструмент **Выбрать**, а затем выберите внедренное приложение.
4. Чтобы изменить приложение, внесите необходимые изменения в конфигурацию, а затем нажмите кнопку **Сохранить**.

    В качестве альтернативы для удаления приложения выберите **Удалить**.

5. Повторно сохраните или опубликуйте представление. Обратите внимание, что если закрыть страницу без явного сохранения представления, ни одно из действий, выполненных на панели **Изменить веб-сайт**, не будет сохранено.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Приложения, которые внедрены с панели мониторинга

1. Откройте панель мониторинга.
2. Выберите и удерживайте (или щелкните правой кнопкой мыши) плитку, связанную с внедренным приложением, выберите **Персонализация**.
3. Чтобы изменить приложение, выберите **Изменить страницу**. В области **Изменить веб-сайт** внесите необходимые изменения в конфигурацию приложения, а затем нажмите кнопку **Сохранить**.

    В качестве альтернативы для удаления приложения выберите **Удалить страницу**.

## <a name="appendix"></a>Приложение

### <a name="troubleshooting"></a>Устранение неполадок

Если веб-сайт не отображается правильно после встраивания в приложение Finance или Operation или если получено сообщение об ошибке, в котором говорится, что URL-адрес отклонен подключением, вероятно, веб-сайт настроен таким образом, чтобы не допустить его встраивания в iFrame. Выполните следующие действия, чтобы определить, может ли веб-сайт быть внедрен в систему.

1. Откройте средства для разработчиков для браузера, который вы используете.
2. На вкладке **Сеть** найдите и выберите ответ из встроенного сайта.
3. На вкладке **Заголовки** в области **Заголовки ответов** найдите **x-frame-options**. Если **x-frame-options** существует в заголовках ответа и имеет значение **DENY** или **SAMEORIGIN**, веб-сайт невозможно внедрить в данный момент. Вам придется работать с владельцем приложения, чтобы обеспечить его безопасное внедрение.

### <a name="developer-modeling-a-website-on-a-form"></a>[Разработчик] Моделирование веб-сайта в форме

Хотя эта статья посвящена внедрению приложений или веб-сайтов сторонних производителей посредством персонализации, разработчики также могут внедрить их в форму, используя среду разработки Visual Studio. Просто добавьте элемент управления **WebsiteHostControl** в форму. Свойства метаданных, доступные в элементе управления, обеспечивают те же возможности, что и персонализация.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

