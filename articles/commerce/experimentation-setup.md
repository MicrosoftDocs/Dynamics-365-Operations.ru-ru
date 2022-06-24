---
title: Настройка эксперимента
description: В этой статье описывается, как настроить эксперимент в сторонней службе.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946174"
---
# <a name="set-up-an-experiment"></a>Настройка эксперимента

После [определения гипотезы и определения, какие метрики успеха требуется использовать](experimentation-identify.md), необходимо настроить эксперимент в сторонней службе. На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce. Дополнительные шаги описаны в отдельных статьях.

[ ![Путь взаимодействия пользователя с экспериментами — настройка.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Настройка эксперимента в сторонней службе
К этому моменту вы должны были выбрать стороннюю службу, чтобы запустить и отслеживать свой эксперимент, и настроить соединитель экспериментирования. Эти предварительные условия описаны в разделе [Экспериментирование в Dynamics 365 Commerce](experimentation-overview.md).

Выполните шаги, необходимые для создания эксперимента в сторонней службе. Если соединитель настроен правильно, полный список экспериментов, которые вы настраиваете в сторонней службе, появится в конструкторе сайтов Commerce в течение 5 минут.

## <a name="set-up-your-success-metrics"></a>Настройка метрик успешности
Каждый эксперимент нуждается в метриках для измерения воздействия вариаций и подтверждения гипотезы. Выполните приведенные ниже шаги, чтобы разрешить вычисление метрик в сторонней службе с использованием событий телеметрии в режиме реального времени из Dynamics 365 Commerce.

Чтобы настроить метрики успешности для готовых модулей из комплекта поставки, выполните следующие действия.

1. В конструкторе сайтов Commerce выберите вкладку **Страницы** в левой области переходов, затем выберите страницу, по которой необходимо собрать метрики. 
1. Перейдите к разделу **Коды событий для отслеживания** в правой области свойств страницы или модуля, которые необходимо отследить.
1. Выберите **Представление**. Отображается список всех кодов событий щелчка. Скопируйте событие, которое требуется отслеживать, затем вставьте ключ события в указанное место в сторонней службе. Если требуется более одного события, скопируйте ключи по одному. 
1. Для просмотров страниц используйте значение хэша SHA-256 имени страницы в конструкторе сайтов с добавлением `.PageView`. Например, кодом события для `Homepage.PageView` может быть `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Выполните все другие шаги для отслеживания метрик в соответствии с требованиями сторонней службы.

Для щелчков настраиваемого модуля выполните следующие шаги для инструментирования событий щелчка:

1. Подготовьте объект **TelemetryContent** для модуля, используя функцию, приведенную далее. Эта функция берет в качестве входных данных имя страницы, имя модуля и предоставляемый SDK объект телеметрии по умолчанию.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Ниже приведен пример: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Создайте полезные данные, содержащие сведения о том, что необходимо записать. Для кнопок и других статических элементов управления можно включить **etext**, например "Купить" или "Поиск". И для компонентов с щелчками мышью, например щелчками карты продукта, можно отправить **recid**, который является кодом записи продукта или кодом продукта.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    В качестве примера для статических элементов управления передайте текстовую строку кнопки, как показано ниже:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    В качестве примера для щелчков по продукту передается recordId продукта, как показано ниже:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Чтобы зарегистрировать событие, вызовите функцию **OnClick**.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Ниже приведен пример:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Предыдущий шаг
[Определение гипотезы и определение метрик для эксперимента](experimentation-identify.md) 


## <a name="next-step"></a>Далее
[Подключение и редактирование эксперимента](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
