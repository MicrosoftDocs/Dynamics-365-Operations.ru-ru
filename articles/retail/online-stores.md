---
title: "Обзор интернет-магазина"
description: "В этой статье представлена информация о розничных интернет-магазинах и их настройке в Microsoft Dynamics 365 for Retail."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 28ab301dc3aede6b23fb5d87fcb179916e0296e4
ms.contentlocale: ru-ru
ms.lasthandoff: 06/20/2017



---

# <a name="online-store-overview"></a>Обзор интернет-магазина

[!include[banner](includes/banner.md)]


В этой статье представлена информация о розничных интернет-магазинах и их настройке в Microsoft Dynamics 365 for Retail.

Dynamics 365 for Retail поддерживает множественные розничные каналы. Эти розничные каналы включают в себя интернет-магазины, центры обработки вызовов и розничные магазины (также называются физическими магазинами). Интернет-магазины обеспечивают розничным торговцам присутствие в Интернете, чтобы их клиенты могли покупать продукты не только в розничных магазинах торговца, но и в интернет-магазине. Если клиент покупает товары в интернет-магазине, они могут заказать доставку на дом или забрать товар в ближайшем розничном магазине. Вы создаете интернет-магазин в клиенте Dynamics 365 for Retail. Этот интернет-магазин после этого опубликуется в интернет-магазине третьей стороны, который интегрирован с Dynamics 365 for Retail. Интернет-магазин третьей стороны выполняет роль внешней витрины (пользовательского интерфейса) для интернет-магазина, и дает вам выбор системы управления клиентами (CMS) и возможностей пользовательского интерфейса. Для Dynamics 365 for Retail доступны несколько интеграций этого типа. Свойства, которые определяются для интернет-магазина, управляют поведением интернет-магазина. Например, можно определить иерархию навигационной категории в Dynamics 365 for Retail и назначить ее интернет-магазину. При публикации интернет-магазина в интернет-магазине третьей стороны иерархия навигационной категории отображается в интернет-версии магазина. Покупатели затем используют иерархию навигационной категории для осмотра интернет-магазина и поиска продуктов. Для создания интернет-магазина необходимо настроить компоненты, которые позволяют обрабатывать проводки для магазина. Например, вы должны добавить ассортименты, применить атрибуты, и настроить методы оплаты и методы доставки. Можно также определить цены, специальные акции, скидки, торговые соглашения, и условия доставки, относящиеся к интернет-магазину. После публикации интернет-магазина в интернет-магазине третьей стороны можно создать розничные каталоги продуктов для интернет-магазина. Продукты в каталоге будут перечислениями продуктов в интернет-магазине. Когда покупатель покупает продукты из интернет-магазина, доступные запасы обновляются и синхронизируются в клиенте. Кроме того, заказы на продажу создаются для покупок и отправляются в клиент для выполнения и обработки заказа.

## <a name="set-up-an-online-store"></a>Настройка онлайн-магазина
Чтобы настроить интернет-магазин, необходимо выполнить следующие задачи.

1.  Создайте интернет-магазин.
2.  Добавьте интернет-магазин к соответствующим организационным иерархиям.
3.  Добавьте ассортименты, включающие продукты, доступные в интернет-магазине.
4.  Назначьте или создайте группы цен для интернет-магазина.
5.  Настройте способы поставки, доступных в интернет-магазине.
6.  Назначьте способы оплаты, принимаемые интернет-магазином.
7.  Если разрешается покупателям заказывать продукты в Интернете а затем забирать их на локальном магазине, назначьте группы локатора магазинов к интернет-магазину.
8.  Присвоение атрибутов для каналов, продуктов и заказов на продажу к интернет-магазину. Атрибуты канала применяются ко всему интернет-магазину, атрибуты продуктов применяются к продуктам, предложенным в Интернете-магазине, и атрибуты заказа на продажу применяются к заказам на продажу, которые создаются из Интернета-магазина.
9.  Сопоставьте атрибуты, чтобы определить свойства, которые определяют, как эти атрибуты ведут себя в интернет-магазине. Например, можно определить атрибуты как обязательные или доступные для поиска.
10. Опубликуйте интернет-магазин для того, чтобы создать структуру магазина по вашему выбору в интернет-магазине третьей стороны. **Важно.** Перед публикацией интернет-магазина необходимо настроить местоположение распределения для него.

## <a name="retail-channel-navigation-hierarchies"></a>Навигационные иерархии каналов розничной торговли
Перед созданием интернет-магазина необходимо определить иерархию навигации канала розничной торговли, которую необходимо использовать в нем. Иерархия навигации канала розничной торговли представляет собой иерархию категорий, которая отображается в Интернете-магазине после того как магазин опубликован. При публикации каталога розничной продукции в интернет-магазине продукты в каталоге сопоставляются с категориями в иерархии навигации канала розничной торговли. Покупатели затем используют эту иерархию для навигации в интернет-магазине.

## <a name="organization-hierarchies"></a>Организационные иерархии
Организационные иерархии используются для структурирования розничных каналов. Организационные иерархии представляют собой связи между организациями, которые занимаются коммерческой деятельностью. При настройке интернет-магазинов их можно добавить в организационную иерархию. После этого магазины могут совместно использовать данные по ассортименту, пополнению и отчетности. При создании организационной иерархии ей назначается цель. Цель указывает, как иерархия используется в бизнес-структуре. Можно создать одну организационную иерархию для операций магазина и использовать эту иерархию для ассортиментов, пополнения и отчетности. Вместо этого можно создать отдельную организационную иерархию для каждой цели. Кроме того, можно создать несколько иерархий с одной и той же целью и назначить отдельный канал каждой из них. Если планируется опубликовать розничный каталог продуктов в интернет-магазине, необходимо, как минимум, добавить интернет-магазин в организационную иерархию для ассортиментов. Продукты в каталоге выбраны из ассортиментов, назначенных интернет-магазину. Когда каталог опубликован, процесс публикации сравнивает дату вступления в силу для ассортимента, который назначен Интернету-магазину, с продуктами, которые включены в каталоге, чтобы определить, какие продукты нужно сделать доступными в Интернете-магазине.



