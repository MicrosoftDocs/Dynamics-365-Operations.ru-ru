---
title: Добавление новой страницы сайта
description: В этой статье описывается, как добавить новую страницу сайта в Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f6714463c9d5dc844b03f78f0f6ff60c5f270da3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270327"
---
# <a name="add-a-new-site-page"></a>Добавление новой страницы сайта

[!include [banner](includes/banner.md)]

В этой статье описывается, как добавить новую страницу сайта в Microsoft Dynamics 365 Commerce.

Следующим шагом после создания шаблонов и фрагментов для сайта является начало создания страниц, использующих их. Чтобы приступить к работе, необходимо выбрать шаблон или макет, имя страницы и URL-адрес страницы.

## <a name="template-or-layout"></a>Шаблон или макет

Для новой страницы можно использовать либо шаблон, либо макет. Для получения дополнительных сведений см. раздел [Обзор шаблонов и макетов](templates-layouts-overview.md).

## <a name="specify-the-page-name"></a>Укажите имя страницы

Имя страницы должно быть уникальным для сайта и должно быть описательным, чтобы его можно было легко найти и понять, для чего предназначена страница. Можно переименовать страницу позже, отредактировав ее, а затем выбрав символ "перо" рядом с именем страницы в области свойств.

## <a name="specify-the-page-url"></a>Укажите URL-адрес страницы

Имеется возможность ввести URL-адрес для новой страницы. При создании страницы можно ввести строку, которая будет использоваться для формирования полного URL-адреса. Эта строка называется относительным URL-адресом или динамическим URL-адресом. Затем полный URL-адрес создается на основе динамического URL-адреса, и ему назначается новая страница. Можно изменить динамический URL-адрес позже, прежде чем опубликовать страницу. Дополнительные сведения см. в разделе [Создание URL-адреса страницы](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce разделяет URL-адреса и содержимое. Другими словами, можно создать страницу, не связанную с URL-адресом, и можно создать URL-адрес, не связанный со страницей. Таким образом, можно выполнить замену URL-адреса и не требовать простоя, а перенаправлениями легче управлять.

## <a name="add-a-new-page"></a>Добавление новой страницы

Чтобы добавить новую страницу сайта на сайт, выполните следующие действия.

1. В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).
1. Выберите **Создать страницу**.
1. В диалоговом окне **Создать страницу** выберите шаблон, затем выберите **ОК**.
1. В поле **Имя страницы** введите имя страницы (например, **Моя новая страница**).
1. В поле **URL-адрес** введите строку (динамический URL-адрес) для завершения URL-адреса (например, **mynewpage**).
1. Нажмите **ОК**. Появится редактор страниц. Обратите внимание, что заголовок и нижний колонтитул автоматически добавляются на страницу в соответствии с выбранным шаблоном.
1. В структуре страницы выберите слот **Главный**, нажмите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.
1. Выберите **Контейнер**, затем выберите **ОК**
1. Выберите **Гибкий контейнер**, выберите кнопку с многоточием, затем выберите **Добавить модуль**.
1. Выберите **Блок насыщенного содержимого**, затем выберите **ОК**.
1. Выберите **Блок насыщенного содержимого**, выберите кнопку с многоточием, затем выберите **Добавить модуль**.
1. Выберите **Элемент блока насыщенного содержимого**, затем выберите **ОК**.
1. В области свойств справа выберите **Абзац**, затем в поле введите **Мой тестовый текст**.
1. Выберите **Сохранить**, затем выберите **Завершить правку**.
1. В поле **Комментарии** введите **Добавлена новая страница**, затем выберите **ОК**.
1. Выберите **Предварительный просмотр** для предварительного просмотра страницы. По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.
1. Выберите **Опубликовать**.
1. В пути перехода (навигации) выберите **Fabrikam** (или имя вашего сайта).
1. В области переходов слева выберите **URL-адреса**.
1. Найдите и выберите свой URL-адрес (**mynewpage**) в списке.
1. Выберите **Опубликовать**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Изменение существующей страницы сайта](modify-existing-page.md)

[Выбор макета страницы](select-page-layouts.md)

[Управление метаданными для поисковой оптимизации](manage-seo-metadata.md)

[Сохранение, предварительный просмотр и публикация страницы](save-preview-publish-page.md)

[Расширение возможностей страницы продукта](enrich-product-page.md)

[Расширение возможностей целевой страницы категории](enrich-category-page.md)

[Проверка доступности контента страницы](verify-accessibility.md)

[Создание динамических страниц электронной коммерции на основе параметров URL-адреса](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
