---
title: Создание модели конфигурации продукта
description: Ниже описан порядок создания модели конфигурации продукта и ввода основных сведений, таких как атрибуты и субкомпоненты.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca99c0346a3f982164076167c3429587aac18be6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568432"
---
# <a name="create-a-product-configuration-model"></a>Создание модели конфигурации продукта

[!include [banner](../../includes/banner.md)]

Ниже описан порядок создания модели конфигурации продукта и ввода основных сведений, таких как атрибуты и субкомпоненты. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.


## <a name="create-a-product-model"></a>Создание модели продукции

1. Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.
1. Выберите **Создать**.
1. В поле **Имя** введите значение.
1. В поле **Описание** введите значение.
1. В поле **Стратегия поиска решения** выберите один из вариантов.
    * Стратегия поиска решения определяет, как обрабатываются ограничения в модели конфигурации на основе ограничений. Этот выбор может повлиять на производительность модели конфигурации продукта.  
1. В поле **Имя** введите значение.
    * Корневой компонент представляет модель конфигурации продукта, но его также можно использовать в других моделях продуктов.  
1. Нажмите **ОК**.
1. В поле **Повторно использовать конфигурации** выберите один из вариантов.
    * Если параметр повторного использования конфигураций установлен как "Да", система выполнит поиск одинаковых конфигураций после каждого сеанса конфигурации и осуществит повторное использование, если найдено точное соответствие.  

## <a name="add-attributes"></a>Добавить атрибуты

1. Разверните раздел **Атрибуты**.
2. Выберите **Добавить**.
3. В списке пометьте выбранную строку.
4. В поле **Имя** введите значение.
5. В поле **Имя решателя** введите значение.
    * Имя решателя используется решателем ограничения конфигуратора продукта. Оно не должен содержать пробелы или специальные символы кроме _ (подчеркивания).  
6. В поле **Описание** введите значение.
    * Текст описания отображается для пользователя конфигурация и поэтому может служить справкой для выбора правильного значения атрибута.  
7. В поле **Тип атрибута** введите или выберите значение.
    * Тип атрибута определяет, какие значения доступны для атрибута.  
8. Установите флажок **Включить в повторное использование**.
    * Эта форма доступна только в том случае, когда выбран параметр повторного использования конфигураций. Включение атрибута с помощью флажка повторного использования означает, что этот атрибут будет учитываться, когда система выполняет поиск точного соответствия.  

## <a name="add-subcomponents"></a>Добавление субкомпонентов

1. Разверните раздел **Субкомпоненты**.
2. Выберите **Добавить**.
3. В списке пометьте выбранную строку.
4. В поле **Имя** введите значение.
5. В поле **Имя решателя** введите значение.
6. В поле **Описание** введите значение.
7. В поле **Компонент** введите или выберите значение.
    * Каждый субкомпонент должен ссылаться на определение компонента. Эта структура поддерживает многоразовые компоненты и гарантирует, что после определения компонента его можно использовать во многих моделях продуктов.  
8. Нажмите **Сохранить**.
9. Выберите **Сведения о строке спецификации**.
    * Форма сведений строки спецификации позволяет пользователю выбрать нужные свойства для субкомпонента. Каждому свойству можно задать фиксированное значение или сопоставить с атрибутом. Сопоставление с атрибутом приведет к тому, что в свойстве строки спецификации будут разные значения в зависимости от выбора конфигурации.  
10. В поле **Код номенклатуры** введите или выберите значение.
    * Каждый субкомпонент представляет настраиваемый шаблон продукта с учетом технологии конфигурации на основе ограничений. Ссылка дается с помощью кода номенклатуры.  
11. Установите флажок **Задать**.
12. Выберите значение **Да** в поле **Расчет**.
    * Установка параметра расчета гарантирует, что продукт будет включен при выполнении расчета затрат для продукта.  
13. Выберите вкладку **Настройка**.
14. Установите флажок **Задать**.
15. В поле **Количество** введите число.
    * Поле количества определяет, сколько этого продукта будет потреблено в настроенном продукте.  
16. Установите флажок **Задать**.
17. В поле **В серии** введите число.
18. Нажмите **ОК**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]