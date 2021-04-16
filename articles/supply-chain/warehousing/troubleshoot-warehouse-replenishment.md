---
title: Устранение неполадок пополнения склада
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с пополнением склада в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828090"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Устранение неполадок пополнения склада

[!include [banner](../includes/banner.md)]

В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с пополнением склада в Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Я получаю следующее сообщение об ошибке: "Код работы %1 не может быть разблокирован, поскольку у него есть незаконченная работу по пополнению".

### <a name="issue-description"></a>Описание проблемы

Работа по комплектации заблокирована из-за зависимой работы пополнения.

### <a name="issue-resolution"></a>Устранение проблемы

При использовании пополнения по спросу волны, если местонахождение комплектации должно быть пополнено для удовлетворения спроса по исходному заказу, система создает и работу пополнения, и работу комплектации. Однако она блокирует работу комплектации, пока не будет завершена работа пополнения. Такое поведение является умышленным, поскольку местонахождение комплектации не имеет достаточного количества запасов, если только работа по пополнению не завершена. Выполните работу по пополнению, а затем обработайте работу комплектации.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]