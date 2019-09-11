---
title: Порядок выполнения для первоначальной синхронизации Finance and Operations и Common Data Service
description: Эта тема определяет порядок синхронизации, который необходимо соблюдать для создания исходных данных.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873136"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Порядок выполнения для первоначальной синхронизации Finance and Operations и Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Перед использованием интеграции данных необходимо создать исходные данные, необходимые для клиентов, поставщиков и контактов. Например, необходимо создать новый элемент **Группа поставщиков** и установить для ее параметра **Условия оплаты** значение **Net30**. В этом случае, прежде чем пытаться создать элемент **Группа поставщиков**, необходимо убедиться, что **Net30** существует как в Microsoft Dynamics 365 for Finance and Operations, так и в Common Data Service. (В будущем Майкрософт выпустит функцию платформы двойной записи под названием "Начальная синхронизация". Эта функция будет делать одноразовую синхронизацию данных между Finance and Operations и Common Data Service в рамках настройки двойной записи.)

> [!TIP]
> Майкрософт выпускает карту двойной записи для всех справочных данных, включая **Условия оплаты** (условия оплаты). Если у вас уже есть исходные данные в одной системе, небольшая операция обновления для записи может вызвать двойную запись для этой записи.

Вы должны следовать следующему порядку приоритета и убедиться, что исходные данные доступны как в Finance and Operations, так и в Common Data Service.

## <a name="vendor"></a>Поставщик

Ниже представлен порядок выполнения для объекта **Поставщик**:

1. Группа поставщиков

    1. Условия оплаты

        1. Платежные дни и строки
        2. График оплаты

2. Метод платежа поставщикам

## <a name="customer-organization"></a>Клиент (Организация)

Ниже представлен порядок выполнения для объекта **Клиент**:

1. Группа клиентов

    1. Условия оплаты

        1. Платежные дни и строки
        2. Платеж 

2. Способ оплаты клиента

## <a name="contact-person"></a>Контакт (Физическое лицо)

Ниже представлен порядок выполнения для объекта **Контакт**:

1. Заказчик
2. Поставщик
