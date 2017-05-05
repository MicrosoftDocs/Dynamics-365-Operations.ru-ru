---
title: "Настройка интернет-магазина"
description: "В этой статье приводятся ссылки на разделы, которые помогут централизованно настраивать и управлять интернет-магазином из Microsoft Dynamics 365 for Operations."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Retail
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: 4da710b57d03621fdf9abbf5a9598859e1e9aafd
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-online-store"></a>Настройка интернет-магазина

[!include[banner](../includes/banner.md)]


В этой статье приводятся ссылки на разделы, которые помогут централизованно настраивать и управлять интернет-магазином из Microsoft Dynamics 365 for Operations.

Разделы, перечисленные в следующей таблице, помогут настроить компоненты Dynamics 365 for Operations - Retail и розничные интернет-магазин в клиенте Dynamics 365 for Operations.

## <a name="configure-an-online-store"></a>Настройка интернет-магазина
| Задача                                                | Подробности                                                                                                                                                                                                                                                                                                                                                   | Разделы                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Настройте компоненты модуля Retail.                        | Настройте и выполняйте ведение сведений для розничных операций. Эта информация включает магазины, налоги, продукты, подарочные карты, специальные акции и скидки.                                                                                                                                                                                                          | [Настройка и ведение модуля Retail](https://technet.microsoft.com/en-us/library/hh597201.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                          |
| Настройте навигационную иерархию канала розничной торговли.    | Создайте иерархию навигационных категорий канала розничной торговли, которая может быть использована чтобы настроить структуру категорий для продуктов, которые вы предлагаете через Интернет-магазин. Вы определяете иерархию категорий, а затем назначаете продукты, группы атрибутов продукта, и значения атрибутов категориям. Затем вы назначаете иерархию категорий для интернет-магазина.                            | [Настройка розничной иерархии](https://technet.microsoft.com/en-us/library/hh580593.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012) [Настройка атрибутов и типов атрибутов](https://technet.microsoft.com/en-us/library/hh227548.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012) [Настройка групп розничных атрибутов](https://technet.microsoft.com/en-us/library/jj728713.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012) |
| Добавьте интернет-магазин в организационную иерархию. | Перед назначением ассортиментов продукции или выполнения заказов для интернет-магазина, который вы создали, или созданием отчетов, которые включают сведения из интернет-магазина, необходимо назначить магазин к одной или нескольким организационным иерархиям. Как минимум интернет-магазин необходимо назначить организационной иерархии, которая включает ассортименты продуктов. | [Настройка интернет-магазина](https://technet.microsoft.com/en-us/library/jj682095.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                                     |
| Добавьте режимы поставки в интернет-магазин.          | Выберите режимы доставки, которые предлагает интернет-магазин.                                                                                                                                                                                                                                                                                                 | [Настройка интернет-магазина](https://technet.microsoft.com/en-us/library/jj682095.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                                     |
| Выполните сопоставление атрибутов и добавьте метаданные.                   | Выберите параметры, которые определяют, как атрибуты для каждой категории или продукта канала должны вести себя в интернет-магазине на сайте Microsoft SharePoint.                                                                                                                                                                                              | [Настройка интернет-магазина](https://technet.microsoft.com/en-us/library/jj682095.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Настройка продуктов интернет-магазина
| Задача                                 | Подробности                                                                                                                                           | Разделы                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Добавьте ассортименты в интернет-магазин. | Добавьте ассортименты, включающие продукты, предлагаемые в интернет-магазине.                                                                  | [Настройка интернет-магазина](https://technet.microsoft.com/en-us/library/jj682095.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                                              |
| Управляйте каталогами.                     | Используйте каталоги продуктов для определения продуктов, которые будут предлагаться в магазинах.                                                              | [Основные задачи: создание каталогов розничной продукции](https://technet.microsoft.com/en-us/library/jj728712.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                           |
| Управляйте ценами.                       | Настройте и используйте группы цен, которые являются центральной связью между ценами и скидками, и каналами, каталогами, назначениями и программами лояльности. | [Настройка цен с использованием ценовых групп](https://technet.microsoft.com/en-us/library/hh597169.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012) [Настройка налогов](https://technet.microsoft.com/en-us/library/hh580571.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012) |
| Управляйте скидками.                    | Настройте и управляйте корректировками цен и скидками четырех типов.                                                                                  | [Настройка корректировок цен и скидок](https://technet.microsoft.com/en-us/library/hh597114.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                          |
| Управляйте расходами на поставку.             | Настройте и управляйте расходами на доставку, характерными для интернет-магазина.                                                                     | [Настройка расходов на доставку из интернет-магазинов](https://technet.microsoft.com/en-us/library/jj728714.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                           |
| Управляйте способами поставки.            | Управляйте способами поставки, которые доступны в интернет-магазине.                                                                                        | [Настройка способов поставки](https://technet.microsoft.com/en-us/library/jj728719.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012)                                                                                                                                            |

## <a name="set-up-data-exchange-between-dynamics-365-for-operations-and-the-online-store"></a>Настройка обмена данными между Dynamics 365 for Operations и интернет-магазином
| Задача                                 | Подробности                                                                                                                               | Разделы                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Настройте профили интеграции канала. | Профили позволяют компонентам модуля Retail взаимодействовать друг с другом. Настройте профили, прежде чем настраивать параметры обмена данными. | [Настройка профиля "Услуга реального времени"](https://technet.microsoft.com/en-us/library/hh580631.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012) [Настройка профиля канала](https://technet.microsoft.com/en-us/library/jj677402.aspx) (содержимое TechNet для Microsoft Dynamics AX 2012) |

 



