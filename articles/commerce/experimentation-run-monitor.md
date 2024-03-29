---
title: Запуск и контроль эксперимента
description: В этой статье описывается, как выполнять и отслеживать эксперимент в сторонней службе. В нем также описывается, как вносить изменения в вариации после запуска эксперимента.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c9f62c97b46fa00791de52b2804dad5edde7f625
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909591"
---
# <a name="run-and-monitor-an-experiment"></a>Запуск и контроль эксперимента

В этой статье описывается, как выполнять и отслеживать свой эксперимент в приложении стороннего производителя и изменять вариации, если это необходимо. Перед выполнением шагов, описанных в этой статье, необходимо сначала [опубликовать](experimentation-preview-publish.md) ваш эксперимент в модуле Commerce. 

На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce. Дополнительные шаги описаны в отдельных статьях.

[ ![Путь взаимодействия пользователя с экспериментами — запуск и контроль.](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

После публикации вариаций выполняются все этапы, необходимые для выполнения эксперимента в модуле Commerce. Следующим шагом является определение вариации, которая будет отображаться для каждого пользователя при запросе страницы. Сторонняя служба выполняет эту определение, но сначала необходимо активировать эксперимент внутри службы. Так как шаги по активации эксперимента могут различаться в зависимости от службы, необходимо следовать инструкциям, прилагаемым к службе или поставщику услуг. Если эксперимент не активирован, пользователи будут видеть только версию страницы по умолчанию (никакие вариации не будут отображаться).

Необходимо обеспечить достаточное время выполнения эксперимента, чтобы собрать данные для получения статистически значимых результатов. Воспользуйтесь сторонней службой для отслеживания данных и аналитики, относящихся к эксперименту, в ходе выполнения эксперимента.

## <a name="adjust-your-variations"></a>Корректировка вариантов
Если по какой-либо причине необходимо изменить ваши вариации, выполните следующие действия.

> [!IMPORTANT]
> При внесении изменений в действующий эксперимент в модуле Commerce или в сторонней службе могут быть значительные воздействия на результаты. Попробуйте позволить эксперименту выполнить свою программу, а затем создать новый эксперимент для внесения серьезных изменений.

1. В конструкторе сайта Commerce выберите **Эксперименты** в левой области переходов, затем выберите эксперимент. 
1. В раскрывающемся меню выберите вариант, который необходимо обновить.
1. Внесите все необходимые изменения, а затем просмотрите и опубликуйте варианты. Дополнительные сведения см. в разделе [Предварительный просмотр и публикация эксперимента](experimentation-preview-publish.md).
1. Перейдите к сторонней службе, чтобы внести любые изменения, связанные с настройкой эксперимента.
    
## <a name="previous-step"></a>Предыдущий шаг
[Предварительный просмотр и публикация эксперимента](experimentation-preview-publish.md)

## <a name="next-step"></a>Далее
[Повышение вариации и завершение эксперимента](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]