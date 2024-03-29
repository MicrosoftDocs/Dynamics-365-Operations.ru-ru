---
title: Хранилище отчетов о распределении запасов по срокам
description: В этой статье описываются функции, позволяющие выполнить отчет о распределении запасов по срокам и сделать выходные данные доступными в виде формы и диаграммы.
author: JennySong-SH
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d810ec90c85f2f7758ec01ef4b24611e026cc80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875578"
---
# <a name="inventory-aging-report-storage"></a>Хранилище отчетов о распределении запасов по срокам

[!include [banner](../includes/banner.md)]

В Microsoft Dynamics 365 Supply Chain Management можно выполнить отчет **Хранилище отчетов о распределении запасов по срокам** и сделать выходные данные доступными в виде формы и диаграммы. В форме столбцы и агрегированные балансы динамически корректируются в зависимости от настроенного макета. Диаграмма дает визуальное представление, поддерживающий фильтрацию, и позволяет детально просмотреть подробные сведения. Кроме того, информационный объект с именем **Отчет о распределении запасов по срокам** позволяет экспортировать результаты отчета **Хранилище отчетов о распределении запасов по срокам** в формат, такой как Microsoft Excel-файл или PDF-файл.

Этот метод выполнения отчета **Хранилище отчетов о распределении запасов по срокам** полезен в тех случаях, когда выходные данные содержат много строк. Например, на выходе будет содержаться множество строк, если имеется 50 000 номенклатур и 300 магазинов, созданных как склады, и вы запрашиваете распределение запасов по срокам для номенклатуры, месту и складу.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Включение функции отчета о стоимости запасов по складам

Прежде чем использовать эту функцию, необходимо включить ее в системе. Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса компонента и включения их при необходимости. В этой статье функция указана следующим образом:

- **Модуль** — Управление затратами
- **Имя функции** — хранилище отчетов о распределении запасов по срокам

## <a name="run-an-inventory-aging-report-storage"></a>Запуск хранилища отчетов о распределении запасов по срокам

1. Перейдите **Управление затратами \> Запросы и отчеты \> Хранение отчета о распределении запасов по срокам**.
1. Выберите **Создать**.
1. В поле **Код процесса — Имя** введите уникальное имя для отчета.
1. Выберите отчет **Идентификация — код** и отфильтруйте его, как требуется.

    Выполнение отчета всегда выполняется в пакетном задании.

1. После завершения пакетного задания результаты отображаются на странице **Хранение отчета о распределении запасов по срокам**.
1. Для просмотра выходных данных в виде формы с традиционной табличной структурой выберите **Показать подробности**. Для просмотра выходных данных в виде агрегированной диаграммы выберите **Показать диаграмму**.

    > [!NOTE]
    > В форме не будут включены промежуточные итоги, определенные в макете отчета.

Информационный объект **Отчет о распределении запасов по срокам** позволяет экспортировать выходные данные отчета **Хранилище отчетов о распределении запасов по срокам**, применив фильтр к полю **Код процесса — имя** в любой формат, поддерживаемый системой управления данными.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]