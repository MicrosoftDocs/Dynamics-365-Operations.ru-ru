---
title: Обзор библиотеки модулей
description: Эта статья содержит обзор библиотеки модулей Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d9dc07b3f6417c7e284c6555c2818c2a782d7683
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268955"
---
# <a name="module-library-overview"></a>Обзор библиотеки модулей

[!include [banner](includes/banner.md)]

Эта статья содержит обзор библиотеки модулей Microsoft Dynamics 365 Commerce.

Библиотека модулей Dynamics 365 Commerce представляет собой набор модулей, которые могут использоваться для создания веб-сайта электронной коммерции. Модули имеют как аспекты интерфейса пользователя, так и аспекты функционального поведения.

Темы могут быть применены к модулям в библиотеке модулей для изменения их внешнего вида и поведения. В темах используются каскадные таблицы стилей (CSS). Тема вымышленного сайта электронной коммерции под названием "Fabrikam" предоставляется в качестве части библиотеки модулей и может использоваться в качестве ссылки.

## <a name="module-library-modules"></a>Модули библиотеки модулей

В библиотеке модулей представлены следующие типы модулей:

- **Контейнерный модуль** — это простой модуль, который служит для размещения других модулей. Он управляет макетом модулей, которые находятся внутри него.
- **Маркетинговые модули** — модули маркетинга включают в модуля блока содержимого, блока текста, видеопроигрывателя и карусели. Все эти модули могут использоваться для демонстрации содержимого. Их можно разместить на любой странице, и они управляются данными из системы управления контентом (CMS).
- **Модули заголовка и нижнего колонтитула** — модули заголовка и нижнего колонтитула отображаются в заголовке и нижнем колонтитуле всех страниц сайта. Эти модули могут быть настроены в качестве обязательных с помощью свойств.
- **Модули поиска** — продукты можно обнаружить, используя модуль поиска в заголовке. Результаты поиска отображаются на странице результатов поиска. Продукты также могут обнаруживаться на страницах категорий, являющихся выделенными страницами для каждой категории, поддерживаемой в иерархии навигации канала. Кроме того, модули уточнения могут использоваться для получения дальнейшей фильтрации результатов на страницах результатов поиска и категорий.
- **Модули страниц сведений о продукте** — страницы сведений о продукте используют несколько модулей для отображения информации о продукте. Модуль поля покупки позволяет клиентам просматривать продукты и добавлять их в корзину. В других модулях, таких как модуль технических спецификаций, отображаются подробные сведения о продукте. Модуль оценок и отзывов может использоваться для просмотра и предоставления отзывов.
- **Модуль покупки в Интернете с получением в магазине** — этот модуль интегрирован с картами Bing. Он может использоваться для поиска ближайших магазинов, в которых клиенты могут забрать товары, которые они приобрели.
- **Модули покупки** — модули покупки включают в себя модуль корзины, который может использоваться для добавления номенклатур в корзину. Модуль оформления заказа фиксирует адрес отгрузки, параметры доставки и сведения о подарочном сертификате, программе лояльности и кредитной карте, чтобы заказ мог быть обработан. После размещения заказа можно использовать модуль подтверждения заказа для отображения подробных сведений подтверждения.
- **Модули управления учетными записями** — модуль входа в систему позволяет клиентам войти в существующую учетную запись, а модуль регистрации позволяет им создать новую учетную запись. После создания учетной записи модуль истории заказов можно использовать для просмотра последних заказов, а для просмотра сведений о заказе можно использовать модуль сведений о заказе.
- **Модуль рекомендаций** — рекомендации отображаются с использованием модуля размещения продукта. Этот модуль поддерживает алгоритмические и редакционные списки, которые можно показать на любой странице.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Модуль контейнера](add-container-module.md)

[Модуль поля покупки](add-buy-box.md)

[Модуль корзины](add-cart-module.md)

[Модуль оформления заказа](add-checkout-module.md)

[Модуль подтверждения заказа](order-confirmation-module.md)

[Модуль заголовка](author-header-module.md)

[Модуль нижнего колонтитула](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
