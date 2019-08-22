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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797306"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Порядок выполнения для первоначальной синхронизации Finance and Operations и Common Data Service

Перед использованием интеграции данных необходимо создать исходные данные, необходимые для клиентов, поставщиков и контактов. Например, если вы хотите создать новый элемент **Группа поставщиков** и установить для него **Условия оплаты** как **Net30**, то перед попыткой создать элемент **Группа поставщиков** необходимо убедиться, что **Net30** существует как в Finance and Operations, так и в Common Data Service. (В будущем мы выпустим функцию платформы двойной записи под названием **Начальная синхронизация**. Она будет делать одноразовую синхронизацию данных между Finance and Operations и Common Data Service в рамках настройки двойной записи.)

Советы. Мы выпускаем карту двойной записи для всех справочных данных, включая **Условия оплаты** (Условия оплаты). Если у вас уже есть исходные данные в одной системе, небольшая операция обновления для записи может вызвать двойную запись для этой записи. 

Вы должны следовать следующему порядку приоритета и убедиться, что исходные данные доступны как в Finance and Operations, так и в Common Data Service.   

## <a name="vendor"></a>Поставщик

Порядок выполнения для поставщика:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Клиент (Организация)

Порядок выполнения для клиента:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Контакт (Физическое лицо)

Порядок выполнения для контакта:

```
Customer
Vendor               
```
