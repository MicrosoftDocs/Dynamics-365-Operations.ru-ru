---
title: Удаленные или устаревшие функции Dynamics 365 Commerce
description: В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 357f4673d77ee990c4e1b0ce84a704fd4d778402
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240227"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Удаленные или устаревшие функции Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Commerce.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании. 

> [!NOTE]
> Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://docs.microsoft.com/dynamics/s-e/). Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Функции, удаленные или устаревшие в выпуске Commerce 10.0.17

> [!Important]
> Версия 10.0.17 доступна как часть выпуска предварительной версии. Содержимое и функциональность могут быть изменены. Дополнительные сведения о предварительных выпусках см. в разделе [Вопросы и ответы по обновлениям службы с одной версией](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

### <a name="full-dataset-generation-interval-is-deprecated"></a>Интервал создания полного набора данных устарел

|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Начиная с данного выпуска в форме **Параметры планировщика Commerce** в Dynamics 365 headquarters поле **Интервал создания полного набора данных в днях** станет устаревшим. Кроме того, начиная с этого выпуска это поле будет визуально удалено, чтобы значение невозможно было изменить. Оно останется со значением **0**. |
| **Заменена другой функцией?**   | Нет |
| **Затрагиваемые области продукта**         | Dynamics 365 Commerce |
| **Вариант развертывания**              | Все|
| **Состояние**                         | Устарело. Не используйте это поле и не изменяйте значение в нем.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Функции, удаленные или устаревшие в выпуске Commerce 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Поддержка Internet Explorer 11 для Dynamics 365 устарела

|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Начиная с декабря 2020 года поддержка Microsoft Internet Explorer 11 всех продуктов Dynamics 365 устарела, и Internet Explorer 11 не будет поддерживаться после августа 2021 года.<br><br>Это повлияет на клиентов, использующих продукты Dynamics 365, которые разработаны для использования с помощью интерфейса Internet Explorer 11. После августа 2021 года Internet Explorer 11 не будет поддерживаться для подобных продуктов Dynamics 365. |
| **Заменена другой функцией?**   | Мы рекомендуем пользователям переходить на Microsoft Edge.|
| **Затрагиваемые области продукта**         | Все продукты Dynamics 365 |
| **Вариант развертывания**              | Все|
| **Состояние**                         | Устарело. Internet Explorer 11 не будет поддерживаться после августа 2021 года.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Функции, удаленные или устаревшие в выпуске Commerce 10.0.11
### <a name="data-action-hooks"></a>Обработчики действий с данными
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Функция перехватчиков действий с данными устарела из-за проблем с производительностью. |
| **Заменена другой функцией?**   | Рекомендуется использовать [переопределения действий данных](../e-commerce-extensibility/data-action-overrides.md) для изменения бизнес-логики на уровне действий с данными.|
| **Затрагиваемые области продукта**         | Действия данных расширяемости электронной коммерции |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: на момент выпуска 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Поддержка Retail SDK для Visual Studio 2015, msbuild 14.0 и библиотек и средств Retail SDK\Reference
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Поддержка Retail SDK для Visual Studio 2015 устарела и обновлена для поддержки VS 2017, msbuild 15.0 и всех ссылочных библиотек и средств создания прокси-серверов Commerce в папке RetailSDK\References, перемещены в пакеты NuGet, чтобы упростить процесс обновления модели расширения и пакета SDK.|
| **Заменена другой функцией?**   | Рекомендуется следовать сведениям, приведенным в разделе [Перенос пакета Retail SDK с Visual Studio 2015 в Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md), чтобы обновить систему. |
| **Затрагиваемые области продукта**         | Расширения пакета Retail SDK |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: на момент выпуска 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Расширение сервера розничной торговли с помощью IEdmModelExtender и CommerceController
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Расширение сервера розничной торговли с помощью IEdmModelExtender и CommerceController устарело для предоставления упрощенной модели расширения. Новая реализация будет иметь только класс controller без каких-либо дополнительных реализаций класса IEdmModelExtender. Это также позволяет избежать зависимости от определенной версии OData (если версия OData обновлена, это может привести к нарушению работы расширений.) |
| **Заменена другой функцией?**   |  Рекомендуется использовать модель расширения класса IController, импортировав пакет NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Затрагиваемые области продукта**         | Расширения сервера розничной торговли |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: на момент выпуска 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Расширение Hardware Station с помощью IHardwareStationController
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Расширение Hardware Station с помощью IHardwareStationController устарело для предоставления упрощенной модели расширения. Новая реализация будет иметь только класс IController без какой-либо дополнительной реализации класса, чтобы избежать зависимости от основных библиотек Hardware Station, ранее расширение должно было ссылаться на несколько библиотек.) |
| **Заменена другой функцией?**   | Рекомендуется использовать модель расширения класса IController, импортировав пакет NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Затрагиваемые области продукта**         | Расширения Hardware Station |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: на момент выпуска 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Функции, удаленные или устаревшие в выпуске Commerce 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>Операций POS 803 — Комплектация и получение
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Операции комплектации и получения устарели в связи с новой архитектурой операций. |
| **Заменена другой функцией?**   | Да. Она заменяется двумя новыми операциями POS: Входящая операция (804) и исходящая операция (805).|
| **Затрагиваемые области продукта**         | Приложение POS |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: с выпуска 10.0.10 операции комплектации и получения больше не будут получать новые обновления. В будущих выпусках для этих операций будут только исправляться критические ошибки. Всем клиентам рекомендуется перейти на новые [входящие операции](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) и [исходящие операции](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), которые еще долго будут поддерживаться в продукте. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Функции, удаленные или устаревшие в выпуске Commerce 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>API Commerce GetProductAvailabilities и GetAvailableInventoryNearby
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Новые оптимизированные API созданы для замены API GetProductAvailabilities и GetAvailableInventoryNearby. |
| **Заменена другой функцией?**   | Да: он заменен API GetEstimatedAvailabilty и GetEstimatedProductWarehouseAvailability. |
| **Затрагиваемые области продукта**         | SDK приложения электронной коммерции |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарел: с выпуска 10.0.7 GetProductAvailabilities и GetAvailableInventoryNearby больше не будут развиваться. Организации, использующие эти API в развертываниях электронной коммерции, должны преобразовать их в новые API GetEstimatedAvailabilty и GetEstimatedProductWarehouseAvailability и включить [оптимизированную функцию расчета наличия продукта](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Предыдущие объявления об удаленных или устаревших функциях
Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]