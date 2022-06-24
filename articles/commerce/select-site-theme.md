---
title: Выбор темы сайта
description: В этой статье описывается, как задать или изменить тему сайта в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b038dc996c571d54dce3f2aec679f7af8af85074
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900394"
---
# <a name="select-a-site-theme"></a>Выбор темы сайта

[!include [banner](includes/banner.md)]

В этой статье описывается, как задать или изменить тему сайта в Microsoft Dynamics 365 Commerce.

Макет и стиль сайта (например, шрифты, размеры и цвета) определяются темой, которая выбрана и применена для сайта. Тема создается и развертывается разработчиком в компании. Обзор тем см. в разделе [Обзор тем](e-commerce-extensibility/theming.md). Дополнительные сведения о создании и развертывание тем см. в разделе [Создание новой темы](e-commerce-extensibility/create-theme.md).

По умолчанию при первом создании сайта используется тема, которая называется **Fabrikam**. Эта тема по умолчанию предоставляется в составе библиотеки модулей Commerce. После развертывания дополнительных тем для сайта можно настроить сайт так, чтобы он использовал одну из них.

## <a name="select-the-site-theme"></a>Выбор темы сайта

Чтобы выбрать тему, применяемую к сайту, выполните следующие действия.

1. В среде разработки сайтов перейдите на ваш сайт.
1. Перейдите к пункту **Управление сайтом** \> **Расширяемость**.
1. В области **Тема** выберите тему в раскрывающемся меню.
1. Чтобы применить выбранную тему к сайту, выберите **Сохранить и опубликовать**.

> [!NOTE]
> Выбранная тема будет опубликована на сайте сразу после выбора пункта **Сохранить и опубликовать** на странице **Расширяемость**. Чтобы предварительно просмотреть тему на сайте до ее применения, можно использовать среду разработки или песочницы.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Добавление логотипа](add-logo.md)

[Работа с переопределением файлов CSS](css-override-files.md)

[Добавление значка сайта](add-favicon.md)

[Добавление уведомления об авторском праве](add-copyright-notice.md)

[Добавление языков на сайт](add-languages-to-site.md)

[Добавление кода скрипта на страницы сайта для поддержки телеметрии](add-telemetry.md)

[Обзор тематического оформления](e-commerce-extensibility/theming.md)

[Создание новой темы](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
