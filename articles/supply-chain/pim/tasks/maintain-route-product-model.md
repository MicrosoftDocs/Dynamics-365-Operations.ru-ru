---
title: Ведение маршрута для модели продукта
description: Выполнение этой процедуры требует наличия модели конфигурации продукта.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88df8b867ac7f354417add0462e7999747333451
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577272"
---
# <a name="maintain-route-for-a-product-model"></a>Ведение маршрута для модели продукта

[!include [banner](../../includes/banner.md)]

Выполнение этой процедуры требует наличия модели конфигурации продукта. Эта процедура использует модель динамика класса Hi-End в демонстрационной компании USMF для описания процесса.

## <a name="add-a-route-operation"></a>Добавление операции маршрута

1. Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.
1. В списке найдите и выберите требуемую запись.
    * Выберите модель динамика класса Hi--End для этого упражнения.  
1. В списке выберите ссылку в выбранной строке.
1. Разверните раздел **Операции маршрута**.
1. Выберите **Добавить**.
1. В поле **Имя** введите значение.
1. В поле **Описание** введите значение.
1. Нажмите **Сохранить**.

## <a name="enter-route-operation-details"></a>Ввод сведений об операции маршрута

1. Выберите **Сведения об операции маршрута**.
1. В поле **Операция** введите или выберите значение.
1. В поле **Операция №** введите число.
    * Номера операции определяют последовательность маршрута.  
    * Каждое свойство операции маршрута может получить статическое значение или быть сопоставленным с атрибутом. Сопоставление с атрибутом приведет к тому, что значение будет задано в рамках конфигурации.  
1. В поле **Маршрутная группа** введите или выберите значение.
    * Маршрутная группа определяет важное поведение для учета затрат, потребления и настройки.  
1. Выберите вкладку **Настройка**.
1. Выберите вкладку **Время**.
1. В поле **К-во процесса** введите число.
    * Укажите количество, которое будет обработано в течение одной операции.  
1. В поле **Часы/время** введите число.
    * Введите коэффициент времени.  
1. Установите флажок **Задать**.
1. В поле **Время выполнения** введите число.
    * Определите время обработки для указанного количества.  
1. Выберите вкладку **Потребности ресурса**.
1. Выберите **Добавить**.
1. В списке пометьте выбранную строку.
1. В поле **Тип потребности** выберите вариант.
    * Укажите при необходимости определенные ресурсы или возможности, которыми они должны обладать.  
1. В поле **Потребность** введите или выберите значение.
1. Нажмите **ОК**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]