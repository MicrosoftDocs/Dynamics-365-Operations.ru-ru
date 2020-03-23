---
title: Создание или генерация РБП (Россия)
description: В этом разделе объясняется, как вручную создавать РБП и как их генерировать с помощью периодической задачи.
author: anasyash
manager: AnnBe
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6ed2f33fc5503355b320266621004570a48072dc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183925"
---
# <a name="create-or-generate-deferrals-russia"></a>Создание или генерация РБП (Россия)

[!include [banner](../includes/banner.md)]

## <a name="manually-create-deferrals"></a>Создание РБП вручную

Можно использовать страницу **Расходы будущего периода** для создания РБП вручную. Необходимо указать модель РБП для РБП. Статус РБП, который создан вручную, обновляется до **Запланированный**. Нельзя изменить статус вручную.

1. Перейти к **главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов**.
2. На панели операций выберите **Создать** для создания РБП.
3. В поле **Идентификатор РБП** введите уникальный идентификационный номер РБП.
4. В поле **Имя** введите имя РБП.
5. В поле **Комментарий** введите подробное описание РБП.
6. В поле **Дата присоединения** выберите дату, когда создан РБП.
7. В поле **Код расхода** выберите код расходов.
8. В поле **Метод зачета НДС для РБП** выберите метод, который используется, чтобы вычитать налог на добавленную стоимость (НДС) для РБП. Имеются следующие варианты:

    - **Стандарт** — обработка входящего НДС для счетов-фактур, связанных с расходами будущих периодов с использованием стандартного метода вычета НДС.
    - **Пропорциональный** — обработка входящего НДС для счетов-фактур, связанных с расходами будущих периодов с использованием пропорционального метода вычета НДС.

    ![Страница РБП](media/rus-create-generate-deferrals-01.png)

9. На панели операций на вкладке **Расходы будущих периодов** в группе **Книги** выберите **Модели РБП**, чтобы открыть страницу **Модели РБП**.
10. Определите модель РБП, которая должна быть применена для РБП.

    ![Страница моделей РБП](media/rus-create-generate-deferrals-02.png)

11. На панели операций выберите **Проводки**, чтобы открыть страницу **Проводки по РБП**.
12. Просмотрите проводки, связанные с выбранной моделью для РБП, а затем закройте страницу.

    ![Страница проводок по РБП](media/rus-create-generate-deferrals-03.png)

13. На странице **Модели РБП** на панели операций выберите **Баланс**, чтобы открыть страницу **Баланс по РБП**.
14. Просмотрите балансы, связанные с выбранной моделью для РБП, а затем закройте страницу.

    ![Страница балансов по РБП](media/rus-create-generate-deferrals-04.png)

15. На странице **Модели РБП** на панели операций выберите **Сумма списания**, чтобы открыть страницу **Профиль списания расходов будущего периода**.
16. На панели операций выберите **Рассчитать** для рассмотрения рассчитанных сумм списания, которые связаны с выбранной моделью для РБП.

    ![Страница профиля списания РБП](media/rus-create-generate-deferrals-05.png)

## <a name="generate-deferrals-by-using-a-periodic-task"></a>Создание РБП с помощью периодической задачи

Чтобы автоматически создавать РБП, необходимо настроить последовательности расчета и счетчиков для групп РБП.

1. Перейдите к **Главная книга** \> **Периодические задачи** \> **Расходы будущих периодов** \> **Создание РБП**.

    Можно использовать страницу **Создание РБП** для обновления расчета для РБП или автоматического создания РБП с помощью периодической задачи.

    > [!NOTE]
    > Прежде чем создавать РБП с использованием периодической задачи, необходимо создать и разнести накладные поставщиков.

    В следующей таблице описаны поля на странице **Создание РБП**.

    | Поле             | Описание                                                                       |
    |-------------------|-----------------------------------------------------------------------------------|
    | Начальная дата        | Дата начала периода расчета РБП.                                |
    | Дата завершения          | Дата окончания периода расчета РБП.                                  |
    | Последовательность          | Номер последовательности, указанный на странице **Нормативные расходы — последовательности**. |
    | Описание       | Имя последовательности.                                                                |
    | Канал           | Канал вывода РБП для выбранной последовательности.                            |
    | Ссылка на канал | Группа РБП, в которой вводятся рассчитанные результаты.                     |

    В следующей таблице описаны кнопки на панели операций страницы **Создание РБП**.

    | Кнопка           | Описание                                                                               |
    |------------------|-------------------------------------------------------------------------------------------|
    | Счетчики         | Откройте страницу **Настройка счетчика**, где можно настроить счетчики для последовательностей расчета. |
    | Рассчитать все    | Расчет всех последовательностей коэффициента списания РБП.                                   |
    | Рассчитать выделенные | Расчет выбранной последовательности коэффициента списания РБП.                               |

2. Для создания РБП с помощью периодических задач выполните следующие действия:

    1. Выберите строку, которая включает в себя настроенный счетчик, а затем на панели операций выберите **Рассчитать все** или **Рассчитать выделенные**.
    2. В полях **Дата начала** и **Дата окончания** введите диапазон дат для расчета периода РБП.
    3. Установите флажок **Перезаписать**, чтобы перезаписать любые существующие расходы будущих периодов за указанный период, которые не содержат ваучеров списания или выбытия.
    4. Установите флажок **Предварительный просмотр**, чтобы просмотреть или изменить расходы будущих периодов перед их созданием.

        При установке этого флажка перед созданием РБП появляется страница, отображая информацию о РБП. Таким образом, можно изменить параметры для создаваемых РБП. Если флажок снят, расходы будущих периодов автоматически создаются на основе параметров, введенных на странице **Создание РБП**.

    5. Установите флажок **Только по ваучерам ГК**, чтобы создать расходы будущих периодов только из документов главной книги. Все расходы будущих периодов, которые создаются на основе покупок, не будут учитываться.
    6. Перейдите к **Главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов** для просмотра создаваемых РБП. Для просмотра сведений о проводках на странице **Проводки по РБП**, на панели операций выберите **Модели РБП**, а затем выберите **Проводки**.

При создании РБП для накладных поставщика с помощью периодической задачи создаются ваучеры проводки РБП с типом проводки **Приход**.