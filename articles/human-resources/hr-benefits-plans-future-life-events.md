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
ms.openlocfilehash: 2cb3ca03e0d9d7e5423a405f1eb0372e1c19588d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227996"
---
# <a name="configure-future-life-events"></a>Настройка событий будущего

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

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
   | Строка | Номер строки будущего жизненного события. |

4. Нажмите **Сохранить**. 

Будущие жизненные события можно удалять. Если удаляется обработанное будущее жизненное событие, будущая запись также удаляется. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
