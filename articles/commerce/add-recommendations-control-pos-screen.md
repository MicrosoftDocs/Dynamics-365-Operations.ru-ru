---
title: Добавление элемента управления рекомендациями на экране проводки на устройствах POS
description: В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d6f48197a36f633e3cd63cbad4518f53946fc7f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023760"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>Добавление элемента управления рекомендациями на экране проводки на устройствах POS

[!include [banner](includes/banner.md)]


В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 Commerce. Дополнительные сведения о рекомендациях продуктов см. в разделе [Документация по рекомендациям продуктов в POS-терминалах](product.md).


При использовании Commerce можно отображать рекомендации по продукту на устройстве POS. Чтобы отобразить рекомендации по продуктам необходимо добавить элемент управления на экран проводки, используя конструктор макета экрана. 

## <a name="open-layout-designer"></a>Откройте конструктор макета

1. Перейдите в раздел **Retail и Commerce** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **POS** &gt; **Макеты экрана**.
2. Используйте экспресс-фильтр для поиска экрана, на который требуется добавить элемент управления. Например, выполните фильтрацию по полю **Код макета экрана**, используя значение **F2CP16:9M**.
3. В списке найдите и выберите требуемую запись. Например, выберите **Имя: F2CP16:9M Код макета экрана: F2CP16:9M**.
4. Нажмите **Конструктор макета**.
5. Следуйте инструкциям на экране для запуска конструктора макета. В ответ на запрос учетных данных следует ввести те же учетные данные, которые были использованы при запуске конструктора макета со страницы **Макеты экрана**.
6. После входа отображается страница, аналогичная приведенной ниже. Макет будет отличаться в зависимости от настроек, которые были сделаны в хранилище.


    [![Конструктор макета](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Выберите параметр отображения

Доступны два варианта конфигурации. Выберите вариант, который лучше всего подходит для вашего хранилища, и следуйте оставшимся инструкциям, чтобы завершить настройку элемента управления. Имеется две возможности:

- Рекомендации отображаются всегда.
- Вкладка **Рекомендации** отображается в сетке в правой части экрана.

### <a name="make-recommendations-always-visible"></a>Задайте, чтобы рекомендации отображались всегда


1. Уменьшите высоту области подробных сведений о строках проводки, чтобы ее высота была равна высоте панели клиента слева.


    [![Высота области сведений строк проводок уменьшена](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Из левого меню перетащите элемент управления рекомендаций в зону между областью сведений строки проводки и сеткой кнопок в нижней центральной части экрана проводок. Измените размер элемента управления, чтобы он помещался в этой области.

    [![Элемент управления рекомендаций добавлен к макету](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.
4. В Commerce перейдите в раздел **Retail и Commerce** &gt; **ИТ Retail и Commerce** &gt; **График распределения**.
5. В списке выберите **1090, Регистры**.
6. Щелкните **Запустить сейчас**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Добавление вкладки "Рекомендации" в сетку кнопок в правой части экрана

1. Щелкните правой кнопкой мыши пустое пространство под последней вкладкой в сетке кнопок, находящейся в правой части страницы.

2. Щелкните **Настройка**.

    [![Диалоговое окно "Настройка" — элемент управления вкладки](./media/pic-5.png)](./media/pic-5.png)

3. Нажмите **Создать вкладку**.
4. Найдите новую вкладку, которая была добавлена. Может потребоваться выполнить прокрутку вниз.
5. В раскрывающемся списке **Содержание** выберите **Рекомендуемые продукты**.

    [![Выбор рекомендуемых продуктов в поле содержания](./media/pic-6.png)](./media/pic-6.png)

6. В **Метка** введите имя для вкладки рекомендаций. Например, введите "Рекомендуемые продукты".
7. В поле **Изображение** выберите изображение, которое должно появляться на вкладке.
8. Щелкните **OK**. Новая вкладка отображается в сетке кнопок.
9. Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.
10. В Commerce перейдите в раздел **Retail и Commerce** &gt; **ИТ Retail и Commerce** &gt; **График распределения**.
11. В списке выберите **1090, Регистры**.
12. Щелкните **Запустить сейчас**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Рекомендации по продуктам на POS](product.md)

[Обзор рекомендаций по продуктам](../commerce/product-recommendations.md)