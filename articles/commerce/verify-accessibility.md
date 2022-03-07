---
title: Проверка доступности контента страницы
description: В этой теме описывается, как проверить специальные возможности конвента страницы в Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6f92d5c34896e284a40a4806cd83e469c2db4c9181c919d2d967dacc84076201
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748456"
---
# <a name="verify-page-content-accessibility"></a>Проверка доступности контента страницы

[!include [banner](includes/banner.md)]

В этой теме описывается, как проверить специальные возможности конвента страницы в Microsoft Dynamics 365 Commerce.

После того, как вы закончите менять страницу, вы должны убедиться, что контент доступен для всех в Интернете. В инструментах разработки Commerce вы можете легко проверить специальные возможности контента страницы с помощью интегрированной службы [Microsoft Accessibility Insights](https://accessibilityinsights.io/). Эта служба проверяет содержимое страницы в соответствии с последними руководящими принципами [Специальные возможности World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility).

Перед тем, как использовать ее, необходимо включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) на уровне клиента или сайта.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Включите Microsoft Accessibility Insights для всех сайтов вашего клиента

Чтобы включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для всех сайтов Commerce в вашем клиенте, выполните следующие действия.

> [!NOTE]
> Чтобы открыть настройки клиента, вы должны войти в Commerce как системный администратор.

1. Войдите в Commerce в качестве системного администратора.
1. В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.
1. В **Настройки клиента** выберите **Функции**.
1. Установите параметр **Проверка специальных возможностей** как **Вкл**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Включите Microsoft Accessibility Insights для одного сайта

Чтобы включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для одного сайта Commerce, выполните следующие действия.

1. В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).
1. На левом панели навигации выберите **Настройки сайта**, чтобы развернуть.
1. В **Настройки сайта** выберите **Функции**.
1. Установите параметр **Проверка специальных возможностей** как **Вкл**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Проверить специальные возможности содержимого на главной странице

Чтобы использовать интегрированную службу [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для сканирования и проверки содержимого вашей домашней страницы в Commerce, выполните следующие действия.

1. В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).
1. В левой области переходов выберите **Страницы**.
1. Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.
1. На панели команд выберите **Проверить специальные возможности**. Отображается страница **Проверка специальных возможностей**.
1. После завершения сканирования просмотрите содержание отчета.
1. Если какие-либо проверки не удались, выберите каждый элемент с ошибкой, чтобы развернуть его, чтобы просмотреть более подробную информацию.
1. Чтобы закрыть отчет после его проверки, прокрутите в нижней части страницы **Проверить специальные возможности** и выберите **OK**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Изменение существующей страницы сайта](modify-existing-page.md)

[Добавление новой страницы сайта](add-new-page.md)

[Выбор макета страницы](select-page-layouts.md)

[Управление метаданными SEO](manage-seo-metadata.md)

[Сохранение, предварительный просмотр и публикация страницы](save-preview-publish-page.md)

[Расширение возможностей страницы продукта](enrich-product-page.md)

[Расширение возможностей целевой страницы категории](enrich-category-page.md)

[Создание динамических страниц электронной коммерции на основе параметров URL-адреса](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
