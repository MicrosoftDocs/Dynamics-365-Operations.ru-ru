---
title: Включение рекомендаций "Выбрать похожие по виду"
description: В этой статье описывается, как включить рекомендации по продуктам "Выбрать похожие по виду" в Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 26eb436d889ac81cde730daca9b44d1deeda6c74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282059"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Включение рекомендаций "Выбрать похожие по виду"

[!include [banner](includes/banner.md)]

В этой статье описывается, как включить рекомендации по продуктам "Выбрать похожие по виду" в Microsoft Dynamics 365 Commerce.

Функция рекомендаций "покупать похожие образы" в Dynamics 365 Commerce использует возможности искусственного интеллекта и машинного обучения (ИИ-ML) для предоставления пользователям рекомендаций по визуально похожим продуктам для клиентов. Благодаря созданию рекомендаций "покупать похожие образы" для всех каналов розничной Commerce предприятия розничной торговли могут повысить уровень удовлетворенности клиентов, помогая клиентам легко находить то, что им нужно.

Функция рекомендаций "покупать похожие образы" использует изображения продукта с вариантами начального продукта, чтобы найти и рекомендовать визуально схожие продукты в каталоге продуктов предприятия розничной торговли. 

Рекомендации "покупать похожие образы" доступны как в POS-приложениях, так и в электронной коммерции.

### <a name="example-scenarios"></a>Пример сценариев

- Клиент смотрит на черный полосатый свитер и получает рекомендацию на аналогичный свитер красного цвета. Клиент выбирает рекомендуемый продукт вместо первоначально просмотренного, после чего получает рекомендации для подобных продуктов красного цвета. 
- Клиент использует рекомендации "покупать похожие образы", чтобы обнаружить подходящие серьги для кольца, которое он хочет купить.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Включение рекомендаций "покупать похожие образы" в модуле Commerce headquarters

Рекомендации продуктов поддерживаются только для пользователей Commerce, перенесших свои хранилища в Azure Data Lake Gen2.

### <a name="prerequisites"></a>Необходимые условия

Прежде чем предприятия розничной торговли смогут отобразить для клиентов рекомендации "покупать похожие образы", необходимо выполнить два необходимых действия:

- [Включение рекомендаций по продукту](enable-product-recommendations.md) в Commerce headquarters.
- Убедитесь, что сервер мультимедиа поддерживает вызовы HTTPS.

Чтобы модуль рекомендаций был доступен для доступа к изображениям продуктов, предприятиям розничной торговли необходимо создать URL-адреса продуктов. Чтобы сгенерировать URL-адреса продуктов в Commerce headquarters, выполните следующие действия.

1. Перейдите к **Изображения продуктов**.
1. В области действий выберите **Определить шаблон СМИ**.
1. В области свойств **Определить шаблон СМИ** в разделе **URL-адреса СМИ** выберите **создать URL-адреса**.

> [!NOTE]
> При включении рекомендаций "покупать похожие образы" начинается процесс создания списков рекомендаций по продуктам. Доступность и отображение этих список в интернете-магазине и POS-терминалах может занять до одного дня.

Чтобы включить функцию рекомендаций "покупать похожие образы" в Commerce headquarters, выполните следующие действия.

1. Перейдите к **Управление функциями**.
1. В списке доступных функций выполните поиск и выберите вариант **покупать похожие образы**.
1. В правой области выберите **Включить**, чтобы включить службу.

На следующем рисунке показана функция **покупать похожие образы** на странице **управления функциями** в Commerce Headquarters.

![Функция "покупать похожие образы" на странице управления функциями в центральном офисе Commerce.](./media/enableshopsimilarlooks.png)

После выполнения предыдущих задач POS-приложения автоматически расширяются с помощью контекстной области **покупать похожие продукты**. Если установить флажок **Показать больше**, пользователи POS-терминала могут быть направлены на специальную страницу "покупать похожие образы", которая может быть отфильтрована в дальнейшем.

> [!NOTE]
> Если отключить функцию рекомендаций "покупать похожие образы", никакие другие типы рекомендаций не затрагиваются. Дополнительные сведения о рекомендациях продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Добавление кнопки "покупать похожие образы" к страницам со сведениями о продукте с помощью конфигуратора сайта Commerce

После включения функции рекомендаций "покупать похожие образы" в Commerce headquarters в конфигураторе сайта Commerce предприятий розничной торговли могут добавить кнопку **покупать похожие образы** в поле "Покупка" на любой странице сведений о продукте (PDP). Клиент, который выбрал эту кнопку, переводится на специальную страницу «покупать похожие образы», которая возвращает визуально похожие продукты. В этом случае клиент может использовать селекторы для дальнейшей фильтрации продуктов.

Чтобы добавить кнопку **покупать похожие образы** к страницам сведений о продукте с помощью конфигуратора сайта Commerce, выполните следующие действия.

1. Откройте существующую страницу построителя сайтов, которая содержит модуль поля покупки.
1. В области переходов слева выберите модуль поля покупки.
1. В правой области перехода, установите флажок **Включить ссылку "покупать похожие образы"**.
1. Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее. После публикации страницы сведения о продукте включают кнопку **покупать похожие образы**.

На следующем рисунке показан флажок **Включить ссылку "покупать похожие образы"** и кнопка **покупать похожие образы** на примере PDP в конструкторе сайтов.

![Флажок Включить ссылку "покупать похожие образы" и кнопка "покупать похожие образы" на примере PDP в конструкторе сайтов.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор рекомендаций по продуктам](product-recommendations.md)

[Включение Azure Data Lake Storage в среде Dynamics 365 Commerce](enable-adls-environment.md)

[Включить рекомендации по продуктам](enable-product-recommendations.md)

[Отказ от персонализированных рекомендаций](personalization-gdpr.md)

[Добавление рекомендаций по продуктам в POS](product.md)

[Добавление рекомендаций на экран проводки](add-recommendations-control-pos-screen.md)

[Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения](modify-product-recommendation-results.md)

[Создание контролируемых рекомендаций вручную](create-editorial-recommendation-lists.md)

[Создание рекомендаций с помощью демонстрационных данных](product-recommendations-demo-data.md)

[Вопросы и ответы по рекомендациям по продуктам](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
