---
title: Создание исходного бюджета, а затем реверсирование предварительных записей бюджета для государственного сектора
description: В этой теме приводятся сведения о создании и сторнировании исходной записи бюджета с использованием модели бюджета и значений аналитик, которые имеют предварительные бюджетные суммы.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af037db40b0df3eeea163953d27c211e609cc02b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811247"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a>Создание исходного бюджета, а затем реверсирование предварительных записей бюджета для государственного сектора

[!include [banner](../../includes/banner.md)]

При создании записи исходного бюджета и использовании бюджетной модели и значений аналитики, которые содержат предварительные бюджетные суммы, предварительные бюджетные суммы можно реверсировать. Эта процедура была создана с использованием демонстрационных данных компании PSUS в разделе государственного сектора.

1. Перейдите в раздел "Бюджетирование" > "Записи бюджетного регистра".
2. Щелкните "Создать".
3. В поле "Бюджетная модель" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. Поиск и выбор требуемой записи в списке.
5. В поле "Код бюджета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
6. В списке щелкните "Исходный бюджет".
7. Нажмите кнопку Сохранить.
8. Щелкните "Добавить строку".
9. Необязательно. Если вы хотите изменить дату в одном из заголовков, введите новую дату. Эта дата определяет финансовый период, для которого будет записан бюджет.
10. В поле "Структура счета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
11. Поиск и выбор требуемой записи в списке.
12. В поле "Значения аналитик" укажите требуемые значения.
13. В поле "Сумма" введите число.
14. В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
15. В списке перейдите по ссылке в выбранной строке.
16. Нажмите кнопку "Сохранить".
17. Щелкните "Обновить сальдо бюджета".
    * Необязательно. Можно выбрать параметр реверсирования предварительного бюджета. Обратите внимание, что можно реверсировать как все записи предварительного бюджета, так и только те записи предварительного бюджета, которые имеют указанный код бюджета.  
    * Чтобы выбрать дополнительные параметры, щелкните значок "Разблокировать" в верхней части страницы.  
18. Щелкните Обновить.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]