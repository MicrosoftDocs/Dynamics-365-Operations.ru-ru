---
title: Эксперименты в Dynamics 365 Commerce
description: Эксперименты позволяют создавать, изменять и управлять разметкой страниц и обработкой контента в конструкторе сайтов. Поддержка сквозного эксперимента включена для страниц и сущностей электронной коммерции на странице.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946222"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Эксперименты в Dynamics 365 Commerce
Используйте эксперименты в Dynamics 365 Commerce для подтверждения гипотез об эффективности страниц электронной коммерции и принятия решений относительно надежности, управляемой данными. Commerce поддерживает тестирование A/B на страницах, модулях и фрагментах и позволяет измерять влияние предложенных изменений на веб-сайт.

Можно создавать, изменять и управлять страницами и обработкой содержимого, известной как **варианты**, в конструкторе сайтов Commerce. Commerce интегрируется со службами сторонних производителей, которые можно использовать для создания экспериментов и назначений обработки. Потоки событий реального времени, захваченные в модуле Commerce, включают аналитику, определяющую результаты экспериментов, в сторонней службе. Затем эту аналитику можно использовать, чтобы помочь в поддержке или опровержении вашей гипотезы.

## <a name="set-up-prerequisites"></a>Предварительные условия настройки

1. **Получите правильную версию Commerce** — обновите библиотеку модулей, пакет разработки программного обучения (SDK) для расширения интернет-канала и Commerce Scale Unit до версии Commerce 10.0.13 или более поздней.
1. **Настройте соединитель эксперимента** — соединитель эксперимента позволяет Commerce подключаться к сторонним службам для получения списка экспериментов и определения, когда следует показывать эксперимент для пользователя. Можно купить соединитель третьей стороны из [AppSource](https://appsource.microsoft.com). Следуйте инструкциям по настройке, предоставленным издателем. Можно также использовать образец тестового соединителя из Commerce для тестирования процесса эксперимента без необходимости настройки внешней службы. Дополнительные сведения см. в разделе [Настройка и включение соединителей](e-commerce-extensibility/connectors.md). 
1. **Включите в Commerce флаг возможностей экспериментов** — можно включить эксперименты на уровне клиента в разделе **Параметры клиента \> Функций** или на уровне сайта, перейдя в раздел **Параметры сайта \> Функции**. Включите флаг **Эксперименты**, чтобы начать создавать варианты модуля. Отключение этого флага приводит к прекращению отображения всех экспериментов пользователям и удалению всех функции редактирования в конфигураторе сайтов.
    
## <a name="experimentation-lifecycle"></a>Жизненный цикл экспериментирования

Настройка эксперимента, создание вариаций и запуск эксперимента являются итеративным процессом. На следующей схеме показан жизненный цикл экспериментов в модуле Commerce и в сторонней службе. 

[ ![Жизненный цикл экспериментирования.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Дополнительные сведения о каждом шаге процесса экспериментов см. в следующих статьях.
- [Определение гипотезы и определение метрик для эксперимента](experimentation-identify.md)
- [Настройка эксперимента](experimentation-setup.md)
- [Подключение и изменение эксперимента](experimentation-connect-edit.md)
- [Предварительный просмотр и публикация эксперимента](experimentation-preview-publish.md)
- [Запуск и контроль эксперимента](experimentation-run-monitor.md)
- [Повышение уровня вариации и выполнение эксперимента](experimentation-review-complete.md)

> [!NOTE]
> Чтобы узнать, где находится эксперимент в жизненном цикле, выберите **Эксперименты** в левой области навигации конфигуратора сайтов. Отображается список экспериментов со статусом каждого эксперимента в Commerce и в сторонней службе. Дополнительные сведения см. в разделе [Проверка статуса эксперимента](experimentation-status.md).

## <a name="next-step"></a>Далее
[Определение гипотезы и определение метрики успеха для эксперимента](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
