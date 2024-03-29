---
title: Обработка процента
description: В этой процедуре показано, как создать, напечатать и разнести процент-ноты.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcffce8f7d2b2c8a8ab2bf6fecaa855df2800382
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725019"
---
# <a name="process-interest"></a>Обработка процента

[!include [banner](../../includes/banner.md)]

В этой процедуре показано, как создать, напечатать и разнести процент-ноты. В этой задаче используется демонстрационная компания USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Настройка процента в профиле разноски
1. В области **Область перехода** выберите **Модули > Кредит и сборы > Настройка > Профили разноски по клиенту**.
2. Выберите **Изменить**.
3. На экспресс-вкладке **Настройка** в поле **Код процента** выберите код процента из раскрывающегося списка. Если вы не хотите рассчитывать процент для проводок с использованием этого профиля разноски, оставьте поле пустым. Экспресс-вкладка **Табличные ограничения** позволяет изменить способ обработки процента. Если в этом поле установить значение "Да", процент будет рассчитан для данного профиля разноски.  

## <a name="calculate-interest"></a>Рассчитать процент
1. В области **Область перехода** выберите **Модули > Кредит и сборы > Процент > Создание процент-нот**.
2. Необходимо выбрать типы проводки, для которых будет рассчитываться процент. Все открытые проводки для этих типов будут включены в расчет.  
3. Если в поле **Процент** задано значение "Да", будет рассчитан процент по процентам. Возможно, потребуется проверить законодательство по расчету процентов по процентам до их включения в проводку.  
4. В поле **Начальная дата** введите дату, с которой будут рассчитываться проценты. Если не указать значение в поле **Дата начала**, все неразнесенные процент-ноты будут отменены и процент будет пересчитан от даты проводки.
5. В поле **Конечная дата** введите дату, до которой будут рассчитываться проценты.
6. В поле **Использовать профиль разноски из** выберите параметр. Имеются три варианта профиля разноски:
    - Счет — используется профиль разноски, назначенный для счета клиента, для каждой процент-ноты. 
    - "Выбор" — используется профиль разноски, выбранный в поле "Профиль разноски".
    - "Проводка" — используется отдельный профиль разноски из проводок, по которым рассчитывается процент для каждой процент-ноты. Проводки без назначенного профиля разноски используют профиль разноски, который указан в области "Главная книга и налог" формы "Параметры расчетов с клиентами".  
7. Разверните экспресс-вкладку **Записи для добавления**.
8. Щелкните **Фильтр**.
9. В поле **Критерии** введите код клиента. Например, введите "US-001".
6. Щелкните **OK**.
7. Щелкните **OK**.

## <a name="print-interest-notes"></a>Печать процент-нот
1. В области **Область перехода** выберите **Модули > Кредит и сборы > Процент > Просмотр и обработка процент-нот**.
2. В поле **Статус** выберите "Создано".
3. В поле **Напечатано** выберите "Не напечатано".
4. Нажмите кнопку **Печать**.
5. Разверните экспресс-вкладку **Записи для добавления**.
6. Щелкните **OK**.
7. Закройте страницу.

## <a name="post-the-interest-note"></a>Разноска процент-ноты
1. Выберите процент-ноту, готовую к разноске (статус "Создано").
2. Щелкните **Разнести**.
3. Введите дату разноски для процент-ноты. Выберите значение "Да", чтобы создать проводку главной книги для каждой процент-ноты. В противном случае процент во всех процент-нотах для клиента накапливается и разносится в ГК в одной проводке.  
4. Разверните экспресс-вкладку **Записи для добавления**.
5. Щелкните **OK**.
6. В поле **Статус** выберите "Разнесено".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
