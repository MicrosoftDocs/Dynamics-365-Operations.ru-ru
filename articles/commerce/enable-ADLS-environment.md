---
title: Включение Azure Data Lake Storage в среде Dynamics 365 Commerce
description: В этой теме объясняется, как включить и проверить Azure Data Lake Storage для среды Dynamics 365 Commerce, что является необходимым условием для включения рекомендаций по продукту.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c10802d66ba9e241a042cc1a0bba01457da20126
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010107"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Включение Azure Data Lake Storage в среде Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

В этой теме объясняется, как включить и проверить Azure Data Lake Storage для среды Dynamics 365 Commerce, что является необходимым условием для включения рекомендаций по продукту.

## <a name="overview"></a>Обзор

В решении Dynamics 365 Commerce все сведения о продуктах и проводках отслеживаются в хранилище объектов среды. Чтобы сделать эти данные доступными другим службам Dynamics 365, таким как анализ данных, бизнес-аналитика и персонализированные рекомендации, необходимо подключить среду к принадлежащему заказчику решению Azure Data Lake Storage Gen 2.

После настройки Azure Data Lake Storage в среде все необходимые данные будут зеркально отражены из хранилища объектов, а также защищены и будут управляться клиентом.

Если в среде также включены рекомендации по продукту или персонализированные рекомендации, то в стеке рекомендаций по продукту будет предоставлен доступ к выделенной папке в Azure Data Lake Storage, чтобы извлечь данные клиента и вычислить рекомендации на их основе.

## <a name="prerequisites"></a>Необходимые условия

У клиентов должны быть настроены Azure Data Lake Storage в подписке Azure, которая им принадлежит. Этот раздел не охватывает покупку подписки Azure или настройки учетной записи хранения с Azure Data Lake Storage.

Дополнительные сведения о Azure Data Lake Storage см. в разделе [Официальная документация по Azure Data Lake Storage](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Шаги конфигурации

В этом разделе описываются этапы настройки, необходимые для включения Azure Data Lake Storage в среде в соответствии с рекомендациями по продуктам.
Более подробное описание шагов, необходимых для включения Azure Data Lake Storage, см. в разделе [Предоставление хранилища объектов как Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Включение Azure Data Lake Storage в среде

1. Выполните вход на портал операционных отделов организации для среды.
1. Выполните поиск **Системные параметры** и перейдите на вкладку **Подключения данных**. 
1. Установите для **Разрешить интеграцию с Data Lake** значение **Да**.
1. Установите для **Постепенное обновление Data Lake** значение **Да**.
1. Затем введите следующие необходимые сведения:
    1. **Код приложения** // **Секретный ключ приложения** // **DNS-имя** — требуется для подключения к KeyVault, где хранится секретный ключ Azure Data Lake Storage.
    1. **Имя секрета — имя секрета**, хранящееся в KeyVault и используемое для аутентификации в Azure Data Lake Storage.
1. Сохраните изменения в левом верхнем углу страницы.

На следующем рисунке показан пример конфигурации Azure Data Lake Storage.

![Пример конфигурации Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Проверка подключения Azure Data Lake Storage

1. Проверьте подключение к KeyVault с помощью ссылки **Проверка Azure Key Vault**.
1. Проверьте подключение к Azure Data Lake Storage с помощью ссылки **Проверка хранилища Azure**.

> [!NOTE]
> Если проверка завершилась неудачно, проверьте правильность всех добавленных данных KeyVault, а затем повторите попытку.

После успешного выполнения проверки подключения необходимо включить автоматическое обновление для хранилища объектов.

Чтобы включить автоматическое обновление хранилища объектов, выполните следующие действия.

1. Найдите **Хранилище объектов**.
1. В списке слева перейдите к записи **RetailSales** и выберите **Правка**.
1. Убедитесь, что для **Автоматическое обновление включено** выбрано значение **Да**, выберите **Обновить**, а затем выберите **Сохранить**.

На следующем рисунке показан пример хранилища объектов с включенным автоматическим обновлением.

![Пример хранилища объектов с включенным автоматическим обновлением](./media/exampleADLSConfig2.png)

Теперь Azure Data Lake Storage настроено для среды. 

Если это еще не было выполнено, выполните шаги, необходимые для [включения рекомендаций по продукту и персонализации](enable-product-recommendations.md) для среды.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Предоставление хранилища объектов как Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Обзор рекомендаций по продуктам](product-recommendations.md)

[Включить рекомендации по продуктам](enable-product-recommendations.md)

[Включение персонализированных рекомендаций](personalized-recommendations.md)

[Отказ от персонализированных рекомендаций](personalization-gdpr.md)

[Включение рекомендаций "покупать похожие образы"](shop-similar-looks.md)

[Добавление рекомендаций по продуктам в POS](product.md)

[Добавление рекомендаций на экран проводок](add-recommendations-control-pos-screen.md)

[Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения](modify-product-recommendation-results.md)

[Создание контролируемых рекомендаций вручную](create-editorial-recommendation-lists.md)

[Создание рекомендаций с помощью демонстрационных данных](product-recommendations-demo-data.md)

[Вопросы и ответы по рекомендациям по продуктам](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]