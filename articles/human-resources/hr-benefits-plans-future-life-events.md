---
title: Настройка событий будущего
description: Можно планировать будущие жизненные события в Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010349"
---
# <a name="configure-future-life-events"></a>Настройка событий будущего

[!include [banner](includes/preview-feature.md)]

Можно планировать будущие жизненные события в Dynamics 365 Human Resources.

1. В рабочей области **Управление льготами** в разделе **Настройка** выберите **Будущие жизненные события**.

2. Выберите **Создать**.

3. Укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | Дата жизненного события | Система обрабатывает все события в течение периода регистрации, которые выполняются до этой даты. |
   | Жизненное событие зарегистрировано | Дата и время внесения жизненного события в журнал. |
   | Тип журнала | Показывает, является ли действие одним из следующих:</br></br>- **Обновить** — изменение существующей записи, которая отслеживает жизненные события</br></br>- **Вставить** — создание новой записи о жизненном событии |
   | Идентификатор типа жизненного события | Уникальный код типа жизненного события. |
   | Тип жизненного события | Катализатор для обновления регистрации льгот сотрудника. Дополнительные сведения см. в разделе триггеров жизненных событий. |
   | Состояние | Обработано ли жизненное событие или нет. |
   | Линейная | Номер строки будущего жизненного события. |

4. Нажмите **Сохранить**. 
