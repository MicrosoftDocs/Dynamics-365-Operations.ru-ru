---
title: Настройка событий будущего
description: В этой статье описывается, как планировать будущие жизненные события в Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 183d0f13a17ffac723fac6c4801bd187dd54e976
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888864"
---
# <a name="configure-future-life-events"></a>Настройка событий будущего

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
