---
title: Устранение неполадок непрерывного производства
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с непрерывным производством.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 938820b6cd2bb470b440fea7b70124efc0faf7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824998"
---
# <a name="troubleshoot-process-manufacturing"></a>Устранение неполадок непрерывного производства

В этом разделе описывается устранение проблем, которые могут встретиться при работе с непрерывным производством.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Когда используется устройство карты задания для отчета о частичном количестве по последнему заданию в производственном заказе, все предыдущие задания в этом заказе, имеющие статус "Выполняется", автоматически закрываются.

Такое поведение предусмотрено разработчиками. На странице **Значения по умолчанию для производственного заказа** на вкладке **Приемка** имеется параметр, который называется **Метка конца маршрута**. Если для этого раздела установлено значение *Да*, журнал карт маршрутов разносится, когда работник использует устройство карты задания или терминал карты задания для регистрации последней операции. Этот журнал помечает все операции как завершенные и завершает все производственные задания. Когда для параметра **Метка конца маршрута** установлено значение *Да*, система не учитывает статус задания, который выбран сотрудником при регистрации последней операции. Кроме того, система не учитывает, сообщает ли работник о полном или частичном количестве.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>При попытке закрытия запасов получено следующее предупредительное сообщение: "Не было зарегистрировано выполнение вычисления backflush-расчета себестоимости с датой %1, соответствующее концу периода."

В выпусках до выпуска 10.0.13 если не используется поток расчета себестоимости бережливого производства, при закрытии запасов выводится следующее сообщение об ошибке:

> Вы собираетесь выполнить закрытие запасов с датой %1. Не было зарегистрировано выполнение вычисления backflush-расчета себестоимости с датой %1, соответствующее концу периода. Не забудьте выполнить вычисление backflush-расчета себестоимости с датой %1, соответствующее концу периода. Оценка стоимости запасов, себестоимости проданных товаров и отклонений может быть неверна в субкниге или в главной книге до тех пор, пока оно не будет выполнено.

Эта проблема исправлена в версии 10.0.13 и более поздних версиях. Дополнительные сведения см. в статье базы знаний [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]