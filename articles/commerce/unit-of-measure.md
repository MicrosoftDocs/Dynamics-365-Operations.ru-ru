---
title: Применение параметров единиц измерения
description: В этой статье описываются настройки единицы измерения и описывается порядок их применения в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7a7be6395a8bfce38e84f850bd792f358941c18a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275580"
---
# <a name="apply-unit-of-measure-settings"></a>Применение параметров единиц измерения

[!include [banner](includes/banner.md)]

В этой статье описываются настройки единицы измерения и описывается порядок их применения в Microsoft Dynamics 365 Commerce.

Продукт может продаваться в различных единицах измерения, таких как "штука", "пара", "десяток". В Commerce Headquarters единица измерения продажи может быть определена для продукта и показана на сайте электронной коммерции. Например, если розничный продавец продает продукт как отдельно, так и десятками, доступные единицы измерения могут отображаться вместе с другими сведениями о продукте.

В примере на следующем рисунке для продукта в Commerce Headquarters сконфигурирована единица измерения **шт** (штука).

![Пример продукта, сконфигурированного с единицей измерения в модуле Commerce Headquarters.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Поддержка применения и отображения единицы измерения доступна в Commerce версии 10.0.19.

## <a name="unit-of-measure-settings"></a>Настройки единицы измерения

Параметры отображения единицы измерения определяются в конструкторе сайтов Commerce в **Параметры сайта \> Расширения \> Отображение единиц измерения для продуктов**. Имеется три поддерживаемые настройки:

- **Не отображать** — если этот параметр выбран, на сайте электронной коммерции не будет отображаться единица измерения для продукта. Такое поведение является поведением по умолчанию.
- **Отображение во время приобретения продукта** — когда выбран этот параметр, единица измерения отображается на страницах сведений о продукте, корзины, оформления заказа, журнала заказов и сведений о заказах.
- **Отображение при просмотре товаров и при покупке** — если выбран этот параметр, единица измерения отображается на страницах покупки продукта, а также во время просмотра продуктов. В рамках такого поведения единицы измерения отображаются в результатах поиска и модулях коллекции продуктов.

> [!IMPORTANT]
> Параметры отображения единиц измерения доступны в Commerce в версии 10.0.19. Если выполняется обновление с более ранней версии Commerce, необходимо вручную обновить файл appsettings.json. Дополнительные инструкции см. в разделе [Обновления пакета SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Модули, в которых используется настройка единиц измерения

Модули, в которых используются параметры единицы измерения, включают в себя модули поля покупки, списка желаемого, корзины, значка корзины, контейнера результатов поиска, коллекции продуктов, оформления заказа и сведений о заказах.

В примере на следующем рисунке страница сведения о продукте (PDP) содержит единицу измерения (**шт**) для продукта.

![Пример PDP, отображающей единицу измерения.](./media/Productunit-PDP.png)

В примере на следующем рисунке модуль коллекции продуктов содержит единицу измерения (**шт**) для продукта.

![Пример модуля коллекции продуктов, отображающего единицу измерения.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор библиотеки модулей](starter-kit-overview.md)

[Модуль корзины](add-cart-module.md)

[Модуль поля покупки](add-buy-box.md)

[Страницы и модули управления учетной записью](account-management.md)

[Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
