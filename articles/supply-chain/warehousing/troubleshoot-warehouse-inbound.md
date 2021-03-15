---
title: Устранение неполадок входящих операций склада
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с входящими операциями склада в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970263"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Устранение неполадок входящих операций склада

[!include [banner](../includes/banner.md)]

В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с входящими операциями склада в Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Получено следующее сообщение об ошибке: "Создан заказ для контроля качества %1. Не удалось найти профиль кластера. Проверьте конфигурацию."

### <a name="issue-description"></a>Описание проблемы

Это сообщение об ошибке относится к процессу приемки, когда включено управление качеством (QMS). В зависимости от конфигураций в вашей среде, для устранения проблемы могут помочь дополнительные сведения о проводке, которая создает это сообщение об ошибке.

### <a name="issue-resolution"></a>Устранение проблемы

Сначала проверьте настройку [комплектации кластера](set-up-cluster-picking.md) и убедитесь, что профили кластеров настроены правильно. Нельзя использовать пункт меню мобильного устройства для комплектации кластера, если не настроены профили кластера. В зависимости от среды, возможно, придется также просмотреть и другие связанные конфигурации.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Использование смешанных грузомест не работает для любого метода обработки, за исключением кредита.

### <a name="issue-description"></a>Описание проблемы

Если для поля **Действие** для кода метода обработки выбрано *Кредит* или *Отходы*, для обработки возвращенных номенклатур можно использовать только пункт меню [Получение грузоместа со смешанными номенклатурами](mixed-license-plate-receiving.md).

### <a name="issue-resolution"></a>Устранение проблемы

Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции. В настоящее время только [коды методов обработки](../service-management/set-up-disposition-codes.md), у которых в поле **Действие** задано значение *Кредит* или *отходы*, поддерживаются для получения грузомест со смешанными номенклатурами.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>При выполнении периодической задачи обновления поступлений продуктов подтверждаются неподтвержденные заказы на покупку.

### <a name="issue-description"></a>Описание проблемы

После запуска периодической задачи *Обновление поступлений продуктов* система автоматически подтверждает неподтвержденные заказы на покупку, имеющие статус складской проводки *Зарегистрировано*.

### <a name="issue-resolution"></a>Устранение проблемы

Новая функция обработки входящей загрузки *Получение сверх количества загрузки* решает эту проблему. Чтобы включить эту функцию, перейдите в раздел [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите следующие функции (в порядке, в котором они перечислены):

1. Связать складские проводки по заказу на покупку с загрузкой
1. Получение сверх количества загрузки

Дополнительные сведения см. в разделе [Разноска зарегистрированных количеств товаров по заказам на покупку](inbound-load-handling.md#post-registered-quantities).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]