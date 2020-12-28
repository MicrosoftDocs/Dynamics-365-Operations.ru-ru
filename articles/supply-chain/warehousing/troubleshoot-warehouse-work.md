---
title: Устранение неполадок работы склада
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с работой склада в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a00ae517ff583e4231099d8e9f5d5b5a696cf7f7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645801"
---
# <a name="troubleshoot-warehouse-work"></a>Устранение неполадок работы склада

[!include [banner](../includes/banner.md)]

В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с работой склада в Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Не удается переместить грузоместа с серийными номерами номенклатуры, если для группы аналитик отслеживания разрешены пустой расход и пустой приход.

### <a name="issue-description"></a>Описание проблемы

Нельзя переместить грузоместо, используя пункт меню **Перемещение**, если серийный номер имеет настройки *Пропуск для расходов* и *Пропуск для приходов* в группе аналитик отслеживания, и если в одном местоположении имеется несколько грузомест, некоторые из которых имеют серийные номера, а другие — не имеют.

### <a name="issue-resolution"></a>Устранение проблемы

Эта проблема будет устранена изменениями, которые разворачиваются в [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Эти изменения сделают поле **Серийный номер** необязательным, если разрешены пустой прием и пустой расход.

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>При обработке перемещений в приложении склада выводится следующее сообщение об ошибке: "Владелец запасов %1не разрешен в этом процессе."

### <a name="issue-description"></a>Описание проблемы

Аналитика отслеживания **Владелец** отсутствует, если приложение склада используется для выполнения перемещений. Обычный журнал перемещения запасов из клиента Supply Chain Management будет работать правильно и может быть разнесен только в том случае, если заполнена аналитика **Владелец**.

### <a name="issue-resolution"></a>Устранение проблемы

Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции. В настоящее время процессы управления складом поддерживают только запасы, которыми владеет юридическое лицо.
