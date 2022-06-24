---
title: Обзор темы Adventure Works
description: В этой статье приводится обзор темы Adventure Works и описывается применение ее к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4f13d6c1c4b0e2764c22dc3d7311c726fac7989d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874995"
---
# <a name="adventure-works-theme-overview"></a>Обзор темы Adventure Works

[!include [banner](includes/banner.md)]

В этой статье приводится обзор темы Adventure Works и описывается применение ее к страницам сайта в Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce имеет тему для электронной коммерции, которая называется Adventure Works. Тема Adventure Works используется для демонстрации спортивных и оздоровительных продуктов и оптимизирована для богатого и расширенного повествования. Она предоставляет современный внешний вид, новые макеты и анимационные эффекты, позволяющие создавать привлекательные и впечатляющие интерактивные покупки для клиентов электронной коммерции.

## <a name="trial-environments-in-commerce"></a>Пробные среды в модуле Commerce

Чтобы увидеть, как выглядит тема Adventure Works, когда она развернута для узлов «предприятие-потребитель» (B2C) и «предприятие-предприятие» (B2B), посетите следующие пробные веб-сайты:

- [Сайт Adventure Works B2C](https://www.adventure-works.com/)
- [Сайт Adventure Works B2B](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Возможности темы

Тема Adventure Works предоставляет следующие новые возможности:

- Модуль видеопроигрывателя поддерживает функции заголовка, абзацев и ссылок для дополнительного повествования.
- Имеются более качественные переходы по содержимому посредством анимации.
- Действие "Добавить в корзину" вызывает мини-корзину, вместо того, чтобы предоставлять уведомление.
- Модуль быстрого просмотра — это панель, в которой просматриваются слайды в окнах просмотра для настольных и мобильных устройств.
- Имеются новые макеты для страниц сайта. 
- Маркетинговые материалы могут быть настроены для корзины и мини-корзины, когда они пустые.
- В мини-корзине могут отображаться рекламные сообщения, такие как "Бесплатная доставка заказов стоимостью более 50 долларов США".
- Карточки описания отображаются на страницах поиска и категорий.

В тему Adventure Works теперь входят следующие модули повествования в библиотеке модуля Commerce:

- [Модуль списка плиток](tile-list-module.md)
- [Модуль интерактивной функции](interactive-feature-module.md)
- [Модуль активного изображения](active-image-module.md)
- [Модуль подписки](subscribe-module.md)
- [Модуль списка изображений](image-list-module.md)

Тема Adventure Works полностью реагирует и предоставляет оптимальный способ для просмотра с настольных, мобильных и планшетных компьютеров.

> [!IMPORTANT]
> Тема Adventure Works и новые модули доступны в выпуске Dynamics 365 Commerce версии 10.0.20.

На следующем рисунке показан пример домашней страницы, использующей тему Adventure Works.

![Пример домашней страницы, использующей тему Adventure Works](./media/aw_b2c.PNG)

На следующем рисунке показан пример страницы списка, использующей тему Adventure Works.

![Пример страницы списка, использующей тему Adventure Works](./media/Aw_list.PNG)

На следующем рисунке показан пример страницы сведений о продукте (PDP), использующей тему Adventure Works.

![Пример страницы сведений о продукте (PDP), использующей тему Adventure Works](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>Используйте тему Adventure Works для сайтов B2B

Тема Adventure Works является также эталонной темой для сайтов "бизнес-бизнес" (B2B). Все модули и бизнес-правила для B2B представлены в теме Adventure Works. Сведения о настройке сайта B2B см. в разделе [Настройка сайта B2B](./b2b/set-up-b2b-site.md).

На следующем рисунке показан пример страницы B2B, использующей тему Adventure Works.

![Пример страницы B2B, использующей тему Adventure Works](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Расширения тем

В тему Adventure Works включено несколько расширений тем, таких как **Расширения просмотра** и **Определение модуля**. Тема Adventure Works может использоваться в качестве эталонной темы для создания подобных расширений. Например, страница списка в теме Adventure Works реализована как расширение просмотра с горизонтальным уточнением. (Напротив, уточнение в левой области используется в теме Fabrikam.)

Аналогичным образом в других модулях имеются расширения определения модуля. Например, [модуль значка корзины](cart-icon-module.md) включает две дополнительные ячейки **Пустая корзина** и **Рекламные материалы**, которые реализуются с помощью расширений определения модуля. Кроме того, новое свойство **Логотип для мобильного устройства** добавлено в модуль заголовка для поддержки логотипа на мобильных устрйоствах. Это свойство реализовано как расширение определения модуля заголовка.

Дополнительные сведения о расширениях темы см. в разделе [Расширения темы](e-commerce-extensibility/theme-module-extensions.md).

## <a name="install-the-adventure-works-theme"></a>Установка темы Adventure Works

Сведения о том, как установить тему Adventure Works, см. в разделе [Установка темы Adventure Works](install-adventure-works.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор библиотеки модулей](starter-kit-overview.md)

[Модуль списка плиток](tile-list-module.md)

[Модуль интерактивных функций](interactive-feature-module.md)

[Модуль активного изображения](active-image-module.md)

[Модуль подписки](subscribe-module.md)

[Модуль списка изображений](image-list-module.md)

[Расширения тем](e-commerce-extensibility/theme-module-extensions.md)

[Модуль значка корзины](cart-icon-module.md)

[Настройка сайта электронной коммерции B2B](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
