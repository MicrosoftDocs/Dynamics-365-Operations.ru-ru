---
title: Включение Azure Data Lake Storage в среде Dynamics 365 Commerce
description: В этой статье приводятся инструкции по подключению решения Azure Data Lake Storage 2 поколения к хранилище объектов среды Dynamics 365 Commerce. Это обязательный шаг перед включением рекомендаций по продукту.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6e0c84dd6b173a111b70a8adb6036be946149f7c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885179"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Включение Azure Data Lake Storage в среде Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

В этой статье приводятся инструкции по подключению решения Azure Data Lake Storage 2 поколения к хранилище объектов среды Dynamics 365 Commerce. Это обязательный шаг перед включением рекомендаций по продукту.

В решении Dynamics 365 Commerce данные, необходимые для расчета рекомендаций, продуктов и проводок, суммируются в хранилище объектов среды. Чтобы сделать эти данные доступными другим службам Dynamics 365, таким как анализ данных, бизнес-аналитика и персонализированные рекомендации, необходимо подключить среду к принадлежащему заказчику решению Azure Data Lake Storage 2 поколения.

После выполнения описанных выше действий все данные клиентов в хранилище объектов среды автоматически отражаются в решении клиента Azure Data Lake Storage 2 поколения. Когда функции рекомендаций включены через рабочую область управления функциями в Commerce headquarters, стеку рекомендаций будет предоставлен доступ к тому же решению Azure Data Lake Storage 2 поколения.

Во время всего процесса данные клиентов остаются защищенными и управляются ими.

## <a name="prerequisites"></a>Необходимые условия

Хранилище объектов среды Dynamics 365 Commerce должно быть подключено к учетной записи хранилища Azure Data Lake 2 поколения и сопутствующим службам.

Дополнительные сведения о Azure Data Lake Storage 2 поколения и как его настроить см. в разделе [Официальная документация по Azure Data Lake Storage](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Шаги конфигурации

В этом разделе описываются этапы настройки, необходимые для включения Azure Data Lake Storage 2 поколения в среде в соответствии с рекомендациями по продуктам.
Более подробное описание шагов, необходимых для включения Azure Data Lake Storage 2 поколения, см. в разделе [Предоставление хранилища объектов как Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Включение Azure Data Lake Storage в среде

1. Выполните вход на портал операционных отделов организации для среды.
1. Выполните поиск **Системные параметры** и перейдите на вкладку **Подключения данных**. 
1. Установите для **Разрешить интеграцию с Data Lake** значение **Да**.
1. Затем введите следующие необходимые сведения:
    1. **Код приложения** // **Секретный ключ приложения** // **DNS-имя** — требуется для подключения к KeyVault, где хранится секретный ключ Azure Data Lake Storage.
    1. **Имя секрета — имя секрета**, хранящееся в KeyVault и используемое для аутентификации в Azure Data Lake Storage.
1. Сохраните изменения в левом верхнем углу страницы.

На следующем рисунке показан пример конфигурации Azure Data Lake Storage.

![Пример конфигурации Azure Data Lake Storage.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Проверка подключения Azure Data Lake Storage

1. Проверьте подключение к KeyVault с помощью ссылки **Проверка Azure Key Vault**.
1. Проверьте подключение к Azure Data Lake Storage с помощью ссылки **Проверка хранилища Azure**.

> [!NOTE]
> Если какой-либо из вышеперечисленных проверка завершилась неудачно, проверьте правильность всех добавленных данных KeyVault и повторите попытку.

После успешного выполнения проверки подключения необходимо включить автоматическое обновление для хранилища объектов.

Чтобы включить автоматическое обновление хранилища объектов, выполните следующие действия.

1. Найдите **Хранилище объектов**.
1. В списке слева перейдите к записи **RetailSales** и выберите **Правка**.
1. Убедитесь, что для **Автоматическое обновление включено** выбрано значение **Да**, выберите **Обновить**, а затем выберите **Сохранить**.

На следующем рисунке показан пример хранилища объектов с включенным автоматическим обновлением.

![Пример хранилища объектов с включенным автоматическим обновлением.](./media/exampleADLSConfig2.png)

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
