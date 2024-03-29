---
title: Настройка коносамента
description: В этой статье описаны способы использования входящих процессов консигнационных запасов.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchTablePart, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0087abebccca107a094a40d3e2d5a5de330532af
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014919"
---
# <a name="set-up-consignment"></a>Настройка коносамента

[!include [banner](../includes/banner.md)]

В этой статье описаны способы использования входящих процессов консигнационных запасов.

Консигнационные запасы — это запасы, принадлежащие поставщику, но хранящиеся на вашем сайте. Когда вы готовы потребить или использовать запасы, вы принимаете на себя владение запасами. Эта статья содержит информацию о том, как физически получить принадлежащие поставщику запасы в наличии без создания проводок главной книги, как запустить процесс производства, где принадлежащий поставщику запас может быть физически зарезервирован, и как изменить владельца сырья в заказе, чтобы можно было обрабатывать потребление как часть обработки производственного заказа. Также приводится некоторая информация о том, как поставщики могут контролировать потребление их запасов, используя интерфейс для совместной работы с поставщиками.

## <a name="overview-of-the-consignment-process"></a>Обзор процесса коносамента

В этом примере сценария компания USMF имеет соглашение коносамента с поставщиком US-104 для сырья M9211CI.

1. Заказ на пополнение коносамента вручную создается сотрудником USMF на основе предполагаемой потребности. Заказ создан для поставщика US-104, и строка добавляется для номенклатуры MS9211CI.
1. Поставщик получает уведомление об ожидаемой доставке. Это можно сделать одним из трех способов:
    - Один из сотрудников компании USMF отправляет сведения о заказе поставщику.
    - Поставщик может контролировать ожидаемые запасы в наличии с использованием интерфейса совместной работы с поставщиками.
    - Сотрудник компании USMF фильтрует данные на странице **Запасы в наличии** для отображения только записей для поставщика US-104, где статус прихода **Заказано**, затем отправляет эту информацию поставщику.
1. Запасы поставляются от компании US-104 в компанию USMF.
1. Когда материал прибывает в USMF, заказ на пополнение коносамента обновляется с поступлением продуктов. Регистрируются только физические количества принадлежащих поставщику запасов. Никакие проводки главной книги не создаются, потому что запасы все еще принадлежат поставщику.
1. Поставщик контролирует обновление физических запасов в наличии с помощью страницы **Консигнационные запасы в наличии**.
1. Теперь, когда физические запасы имеются в наличии, процесс производства резервирует принадлежащие поставщику запасы и запускает производственный заказ готовых товаров, который будет потреблять сырье M9211CI.
1. Владелец зарезервированного сырья, которое будет потреблено сегодня в производстве, меняется с US-104 на USMF. Это выполняется с использованием журнала изменения владельца запасов. Этот процесс создает заказы на покупку, в котором в поле **Источник** задано значение **Коносамент**.
1. Поставщик контролирует потребление (изменение владельца) на странице **Продукты, полученные из консигнационных запасов** и создает накладную на основе соглашений между двумя компаниями.
1. Процесс производства потребляет сырье через отгрузочную накладную производства. Физическое резервирование автоматически обновляется, чтобы отразить, что запасы в наличии принадлежат компании USMF.
1. Накладная от US-104 обрабатывается относительно заказов на покупку, которые были автоматически созданы при обработке журнала изменения владельца запасов. Выполняется платеж поставщику US-104 для запасов, которые были потреблены.

USMF выполняет дополнительные периодические процессы:

- Физическое перемещение принадлежащих поставщику запасов между различными складами обрабатывается с использованием журнала перемещения.
- Физические запасы в наличии обновляются с помощью журнала **Учет номенклатур**. Инвентаризация также может использоваться поставщиком для обновления запасов в наличии, если он имеет разрешение на выполнение этого.

Поставщик, US-104, может контролировать обновления с помощью страницы **Консигнационные запасы в наличии**.

## <a name="consignment-replenishment-orders"></a>Заказы пополнения коносамента

Заказ на пополнение коносамента — это документ, используемый для запроса и отслеживания количества запасов продуктов, которые поставщик планирует поставить в пределах определенного интервала дат путем создания проводок заказанных запасов. Обычно это будет основано на прогнозируемом и фактическом спросе конкретных продуктов. Запасы, которые должны быть получены в соответствии с заказом пополнения коносамента, остаются в собственности поставщика. Записывается только владение продуктами, связанное с обновлением физического получения, и поэтому никакие обновления проводки главной книги не происходят.

Аналитика **Владелец** используется для разделения сведений о том, какие запасы принадлежат поставщику, а какие — получающему юридическому лицу. Строки заказа пополнения коносамента имеют статус **Открытый заказ**, пока не будет получено или отменено полное количество по строкам. Когда было получено или отменено полное количество, статус изменяется на **Завершено**. Физические запасы в наличии, которые относятся к заказу пополнения коносамента, могут быть зарегистрированы с помощью процесса регистрации, а также с помощью процесса обновления поступления продуктов. Регистрация может быть выполнена в процессе прихода номенклатуры или путем ручного обновления строк заказа. Когда используется процесс обновления поступления, запись делается запись в журнале поступления продуктов, которая может быть использована, чтобы подтвердить поступление товаров поставщикам.

[![Заказы пополнения коносамента.](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Журнал изменения владельца запасов

Журнал **Изменение владельца запасов** используется для регистрации передачи прав собственности на запасы коносамента от поставщика юридическому лицу, которое потребляет их. Ожидаемые складские проводки создаваться для журнала не будут. Как и любой журнал запасов, его необходимо определить с именем журнала запасов. Эти имена создаются на странице **Имена журналов запасов**, а для параметра **Тип журнала** должно быть установлено значение **Изменение владельца**.

Создаются только проводки запасов, относящиеся к разнесенному журналу. Когда журнал разносится:

- Запасы, принадлежащие поставщику, расходуются с помощью ссылки **Изменение владельца** со статусом **Продано**.
- Запасы в наличии получаются юридическим лицом, которое потребляет их, с помощью складской проводки обновления поступления продуктов по заказу на покупку. При этом статус заказа изменяется на **Получено**. Для заказов на покупку, используемых для коносамента, в поле **Источник** установлено значение **Коносамент**.

Невозможно обновить количество в строках заказа на покупку коносамента после создания заказа.

[![Журнал изменения владельца запасов.](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Совместная работа с поставщиками в процессах коносамента

Если поставщики используют интерфейс совместной работы с поставщиками, они могут использовать его, чтобы контролировать потребление запасов на вашем сайте. Интерфейс совместной работы с поставщиками имеет три страницы, связанные с процессом входящего коносамента:

- **Заказы на покупку,** **потребляющие консигнационные запасы** — отображаются подробные сведения о заказе на покупку, связанном с изменением собственности в процессе коносамента.
- **Продукты, полученные из консигнационных запасов** — отображаются сведения о номенклатурах и количествах, для которых обновились поступления продуктов в процессе изменения владельца.
- **Консигнационные запасы в наличии** — отображаются сведения о номенклатурах коносамента, для которых ожидается поставка, и номенклатуры, которые физически уже доступны на сайте клиента.

Дополнительные сведения о настройке поставщиков для использования совместной работы с поставщиками см. в разделе [Управление пользователями совместной работы с поставщиками](../procurement/manage-vendor-collaboration-users.md).

## <a name="inventory-owners"></a>Владельцы запасов

Для записи физических входящих консигнационных запасов необходимо указать владельца поставщика. Это выполняется на странице **Владелец запасов**. При выборе параметра **Счет поставщика** это создает значения по умолчанию для полей **Наименование** и **Владелец**. Значение в поле **Владелец** будет отображаться поставщику, поэтому возможно, потребуется изменить его, если ваши названия счетов поставщика непонятны внешним лицам. Можно изменить поле **Владелец**, но только до момента, когда вы сохраняете запись **Владелец запасов**. Поле **Наименование** заполняется именем субъекта, с которым связан счет поставщика, и это невозможно изменить.

[![Владельцы запасов.](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Группа аналитик отслеживания

Номенклатуры, которые будут использоваться в процессе коносамента, необходимо связать с параметром **Группа аналитик отслеживания**, в которой для аналитики **Владелец** задано значение **Активна**. У аналитики "Владелец" всегда выбраны параметры **Физические запасы** и **Финансовые запасы**. Параметр **План покрытия по аналитикам** никогда не выбран.

[![Группа аналитик отслеживания.](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
