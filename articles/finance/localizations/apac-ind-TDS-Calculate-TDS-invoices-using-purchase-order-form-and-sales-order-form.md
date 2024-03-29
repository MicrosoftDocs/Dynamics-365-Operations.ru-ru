---
title: Расчет накладных TDS с использованием формы заказа на покупку и формы заказа на продажу
description: В этой статье перечислены шаги для расчета налога, удерживаемого у источника (TDS), по различным типам накладных.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 72883741ee7eed6b0296736c80dd648c882ae53e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853295"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Расчет накладных TDS с использованием формы заказа на покупку и формы заказа на продажу

[!include [banner](../includes/banner.md)]

В этой статье перечисляются шаги для расчета налога, удерживаемого у источника (TDS), по различным типам накладных с помощью страниц **Заказ на покупку**, **Журнал покупок**, **Контракт** и **Заказ на продажу**.

1. Создайте заказ на покупку, журнал покупок, контракт на покупку или заказ на продажу, используя указанную страницу. Введите требуемую информацию.

2. Перейдите на вкладку **Настройка**, чтобы просмотреть суть налогоплательщика поставщика или клиента. Эта информация перечислена в поле **Суть налогоплательщика** в группе полей **Группа подоходного налога**.

3. В поле **Группа TDS** просмотрите или измените группу TDS по умолчанию, определенную для поставщика или клиента.

   > [!NOTE]
   > Поле **Группа TCS** недоступно, если в поле **Группа TDS** выбрана группа TDS. TDS вычисляется только в том случае, если установлен флажок **Рассчитать подоходный налог** для поставщика или клиента на странице **Все поставщики** или **Все клиенты**.  

4. Создайте строки номенклатур на вкладке **Строки** и введите требуемые сведения.

5. Перейдите на вкладку **Настройка** (уровень строки), чтобы просмотреть или изменить группу TDS, определенную на уровне заголовка. Группа TDS отображается в поле **Группа TDS**, которое находится в группе полей **Группа подоходного налога**.

6. Перейдите на вкладку **Информация по налогам** и выберите альтернативные адреса, которые настроены для названия компании, которое отображается в этом поле. Название компании отображается в поле **Имя**, которое находится в группе полей **Данные о компании**. 

   TAN для выбранного названия компании отображается в поле **Номера счета налога** (**TAN**) в группе полей **Подоходный налог**. 

7. Выберите **Подоходный налог**, чтобы открыть страницу **Временные проводки по подоходному налогу**. Просмотрите следующие поля в верхней области страницы **Временные проводки по подоходному налогу**.

   - **Итоговая** **сумма** **подоходного** **налога** **—** итог TDS, рассчитанный для проводки для группы TDS.

   - **Значение** — итоговое процентное значение, используемое для расчета TDS для проводки. Итоговое процентное значение основано на формуле, которая определена для кодов налогов TDS, прикрепленных к группе TDS.

   - **Скорректированная итоговая сумма подоходного налога** — итоговая скорректированная сумма TDS для всех налоговых кодов в группе TDS.

   - **TDS** — если выбрано, группа TDS присоединена к проводке.

В полях на вкладках **Обзор**, **Общее** и **Корректировка** на странице **Временные проводки по подоходному налогу** отображается рассчитанная сумма TDS и скорректированная сумма TDS для каждого налогового кода TDS, связанного с группой TDS.

8. Выберите **Порог**, чтобы открыть страницу **Порог**. Просмотр лимита порога, определенного для компонента налогов TDS, присоединенных к конкретному налоговому коду TDS на данной странице.

9. Выберите **Конструктор формул**, чтобы открыть форму страницу **Конструктор формул**. Просмотр формулы, которая определена для конкретного налогового кода TDS на данной странице. 

10. Разноска накладной. Сумма TDS, рассчитанная в накладных по покупке, разносится на счет расчетов с поставщиками, а сумма TDS, рассчитанная в накладных на продажу, разносится на счет, который определен для каждого налогового кода TDS в группе TDS. Счета расчетов с поставщиками или счета дебиторской задолженности для налоговых кодов TDS определяются на странице **Коды подоходного налога**.

11. Нажмите кнопку **Запрос** **> Накладная > Разнесенный подоходный налог**, чтобы открыть страницу **Проводки подоходного налога**. Общее процентное значение, используемое для расчета TDS для проводки, можно просмотреть в поле **Значение**.

В полях на вкладках **Обзор**, **Общее** и **Сумма** на странице **Проводки по подоходному налогу** содержат сведения о TDS, рассчитанном для проводки. Просмотрите информацию о расчете TDS для каждого налогового кода TDS, связанного с группой TDS.
