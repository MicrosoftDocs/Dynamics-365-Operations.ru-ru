---
title: Обзор страниц сведений о продуктах
description: В этой статье представлен обзор страниц сведений о продукте (PDP) в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 4856e6e208834d7dcc16d19ad4afb63c329a5868
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278509"
---
# <a name="product-details-pages-overview"></a>Обзор страниц сведений о продуктах

[!include [banner](includes/banner.md)]

В этой статье представлен обзор страниц сведений о продукте (PDP) в Microsoft Dynamics 365 Commerce.

Страница PDP предоставляет подробные сведения о продукте, и клиенты могут выбирать параметры продукта, такие как размер, стиль и цвет. Страница PDP должна показать все сведения о продукте, необходимые клиенту для принятия решения о покупке.

Следующая иллюстрация показывает пример страницы сведений о продукте.

![Пример страницы сведений о продукте.](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Модули верхнего и нижнего колонтитулов

В верхней части страницы PDP имеется заголовок, отображающий все категории продуктов и другие страницы, которые предприятие розничной торговли хочет, чтобы они просматривались пользователями. В нижней части страницы находится нижний колонтитул, содержащий быстрые ссылки на различные статьи, которые могут интересовать клиентов.

## <a name="buy-box-module"></a>Модуль поля покупки

Наиболее важным модулем в PDP является модуль поля покупки, который отображается как первый элемент в главном разделе страницы. Модуль поля покупки содержит важную информацию о продукте, такую как наименование продукта, описание продукта, цену продукта, изображения продукта и оценки продукта.

Модуль поля покупки позволяет клиенту выбирать параметры продукта (например, размер, стиль и цвет) и добавить продукт в корзину. Он также позволяет покупателю купить продукт по Интернету и забрать его в магазине. Модель покупки через Интернет и получения в магазине использует интеграцию с интерфейсами прикладного программирования (API) карт Bing, чтобы найти ближайшие магазины или магазины в другом местоположении, указанном клиентом.

Для модуля поля покупки требуется код продукта. Этот код извлекается из контекста страницы. Если модуль поля покупки добавляется на страницу, где контекст страницы не содержит идентификатора продукта, информация не будет правильно отображена.

## <a name="product-specifications-module"></a>Модуль детализации продукта

Модуль спецификаций продукта может использоваться для демонстрации дополнительной информации о продукте. Эти сведения взяты из атрибутов продукта в Commerce. В модуле спецификаций продукта отображается каждый атрибут, в котором свойство **видимо** имеет значение **true**. Для получения атрибутов продукта требуется код продукта.

## <a name="recommendations-module"></a>Модуль рекомендаций

Модуль рекомендаций является важным модулем на странице PDP. Когда клиенты просматривают продукты, для них должны быть представлены дополнительные варианты продуктов, чтобы они могли найти правильный продукт и выполнить покупку. Рекомендации помогают клиентам легко обнаруживать связанное содержимое и продолжать покупать.

Доступны различные типы списков рекомендаций:

- Список **Людям также нравится** базируется на машинном обучении. Для обеспечения рекомендаций используется история проводок других клиентов. Этот список создается службой рекомендаций и напоминает списки "Клиенты, которые приобрели этот товар, также купили...". Для создания этого списка необходим код продукта.
- Список **Связанные** может быть настроен для продукта в Commerce. Например, для коричневой кожаной дорожной сумочки для списка связанных товаров могут быть настроены сумочки, изготовленные из кожи или предназначенные для путешествий. Другие типы связанных списков, такие как **Аксессуары** и **Еще похожие**, можно также настроить в Commerce. Для создания этого списка необходим код продукта. Таким образом, при добавлении на домашнюю страницу, в которой контекст страницы не содержит идентификатора продукта, список будет пустым.
- Алгоритмически созданные списки рекомендаций, такие как **Тенденции**, **Лидеры продаж** и **Новые**, могут использоваться на страницах сведений о продукте. Хотя эти списки могут не быть непосредственно связанными с продуктом на странице PDP, они являются еще одним способом помочь клиентам найти продукты, которые могут интересовать их. Эти типы списков не требуют наличия кода продукта. Они являются универсальными списками, которые создаются на основе шаблонов покупок внутри сайта.
- Редакционные списки — это созданные вручную списки. Например, розничная сеть может решить, что следует вручную создать списки продуктов, которые они хотят показать.

## <a name="ratings-and-reviews-modules"></a>Модули оценок и отзывов

Для просмотра и добавления отзывов можно использовать три модуля:

- **Оценки** — в этом модуле отображаются оценки и отзывы, предоставляемые другими клиентами. Клиенты могут отсортировать и отфильтровать оценки. Этот модуль также дает клиентам возможность ставить отметки "нравится" или "не нравится" и сообщать о проблемах.
- **Написать отзыв** — с помощью этого модуля клиенты могут создавать свои собственные отзывы о продукте.
- **Гистограмма оценок** — этот модуль содержит гистограмму, в которой показана тенденция оценок продукта.

Дополнительные сведения см. в разделе [Обзор оценок и отзывов](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Модули маркетинга

Если маркетинговое содержимое является уникальным для конкретного продукта, на странице сведений о продукте можно добавить любой модуль маркетинга. На страницу PDP можно добавлять модули маркетинга, "обогащая" страницу. Дополнительные сведения см. в разделе [Расширение возможностей страницы продукта](enrich-product-page.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор домашней страницы](quick-tour-home-page.md)

[Обзор страниц корзины и оформления заказа](quick-tour-cart-checkout.md)

[Обзор страниц управления учетной записью](quick-tour-account-management.md)

[Страница сведений о расширении возможностей страницы продукта](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
