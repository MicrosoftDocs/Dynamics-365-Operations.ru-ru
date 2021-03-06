---
title: Настройка статуса рейса
description: В этой теме описывается, как установить значения статуса, которые пользователи могут назначить для рейса.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e19a54fc9de166c93fd68408ca8c8c692dc96cab
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022116"
---
# <a name="voyage-status-setup"></a>Настройка статуса рейса

[!include [banner](../../includes/banner.md)]

На странице **Статусы рейса** необходимо определить набор значений статуса, которые пользователи могут назначить для рейса. Пользователи могут назначить значения статуса рейса для всех уровней рейса: рейса, контейнера отгрузки, листа, заказа на покупку и номенклатуры (строки покупки и строки заказа на перемещение). Они используются для двух целей:

- Сообщает пользователю о статусе рейса, контейнера отгрузки, листа, заказа на покупку или номенклатуры (строки покупки и строки заказа на перемещение).
- Ограничить использование области затрат, запрещая изменение или удаление.

Чтобы настроить статусы рейсов, перейдите **Стоимость на складе \> Настройка \> Статусы рейса**. Здесь можно использовать кнопки на панели операций для добавления, удаления и редактирования статусов.

К каждой области затрат есть свой собственный набор и иерархия статусов рейса. Таким образом, на странице **Статусы рейса** в поле **Область затрат** необходимо сначала выбрать область затрат, для которой необходимо просмотреть или создать статусы рейса. Затем для каждого состояния рейса задайте необходимые поля, которые описаны в следующей таблице. Обратите внимание, что статус рейса также может быть автоматически изменен системными событиям, например, правилами, которые были установлены с помощью центра управления отслеживанием.

| Поле | описание |
|---|---|
| Статус поездки | Введите название статуса рейса. |
| описание | Введите описание статуса рейса. |
| Изменить | Установите этот флажок, если пользователям разрешено изменять рейсы с данным статусом. |
| Удаление | Установите этот флажок, если пользователям разрешено удалять рейсы с данным статусом. |
| Обязательно | Установите этот флажок, чтобы сделать статус рейса обязательным, чтобы он не мог быть пропущен. |
| Родительский | Это поле используется для определения иерархии между значениями статуса. Статусы рейса могут быть изменены (вручную или автоматически) только в направлении вниз по иерархии, от родительского статуса до одного из дочерних статусов.

> [!NOTE]
> Необходимо настроить только конкретные статусы рейса, используемые в организации. Обычно статусы рейсов включают *Подтверждено*, *Товары в пути*, *Получено*, *Готово к учету затрат* и *Учтено в затратах*. Однако могут присутствовать и другие статусы.
