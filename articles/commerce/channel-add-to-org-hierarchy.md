---
title: Добавление канала в организационную иерархию
description: В этой статье описывается, как добавить канал в организационную иерархию в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 9def2d7c3cf17ecd9b74ce41f56bc3220a754597
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278606"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Добавление канала в организационную иерархию


[!include [banner](includes/banner.md)]

В этой статье описывается, как добавить канал в организационную иерархию в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Каналы должны быть связаны с одной или несколькими организационными иерархиями. Перед созданием каналов необходимо подтвердить настройку организационных иерархий.  

Дополнительные сведения о создании организационных иерархий см. [Организационные иерархии](channels-org-hierarchies.md).

## <a name="select-a-hierarchy"></a>Выберите иерархию

Чтобы выбрать иерархию, выполните следующие действия.

1. В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Организационные иерархии**.
1. В списке выберите организационную иерархию, к которой необходимо добавить канал.
1. В области действий выберите **Вид** для просмотра данных иерархии.

На следующем рисунке показаны данные организационной иерархии для выбранной иерархии.

![Данные организационной иерархии для выбранной иерархии.](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Добавление канала к узел иерархии

Чтобы добавить канал в узел иерархии, выполните следующие действия.

1. На панели операций выберите **Правка**.
1. Выберите узел иерархии, к которому требуется добавить канал, затем в раскрывающемся списке **Вставка** выберите **Канал Retail**. 
1. Выберите добавляемый канал, затем нажмите кнопку **ОК**.
1. На панели операций выберите **Сохранить**.
1. В области действий выберите **Опубликовать** и укажите **Действует с** в прошлом, чтобы это действие сразу запустилось.

На следующем рисунке показано, как выбрать канал для добавления в узел иерархии.

![Выбор канала для добавления в узел иерархии.](media/channel-add-to-org-hierarchy-2.png)

На следующем рисунке показана иерархия с различными добавленными каналами.

![Иерархия, в которую добавлены различные каналы.](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор каналов](channels-overview.md)

[Необходимые условия для настройки каналов](channels-prerequisites.md)

[Обзор организаций и организационных иерархий](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Планирование организационной иерархии](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Организационные иерархии](channels-org-hierarchies.md)

[Настройка канала розничной торговли](channel-setup-retail.md)
    
[Настройка интернет-канала](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
