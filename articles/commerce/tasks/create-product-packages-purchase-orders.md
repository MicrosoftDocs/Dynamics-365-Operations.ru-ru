---
title: Создание пакетов продуктов для заказов на покупку
description: Эта процедура содержит инструкции по созданию пакета продуктов и его использованию в заказе на покупку.
author: josaw1
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb10164be8d7a0828169cf3865f884afaa2e8408472edebe4cb0c7d4db059d8c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723245"
---
# <a name="create-product-packages-for-purchase-orders"></a>Создание пакетов продуктов для заказов на покупку

[!include [banner](../includes/banner.md)]

Эта процедура содержит инструкции по созданию пакета продуктов и его использованию в заказе на покупку. Заказ на покупку будет использоваться для создания заказа на заранее определенный набор продуктов. В этой процедуре используется компания с демонстрационными данными USRT.


## <a name="create-a-product-package"></a>Создание пакета продуктов
1. Перейдите в раздел "Retail и Commerce" > "Управление запасами" > "Пополнение" > "Пакеты продуктов".
2. Щелкните "Создать".
3. В поле "Номер пакета" введите значение.
4. В поле "Описание" введите значение.
5. В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
6. В списке перейдите по ссылке в выбранной строке.
7. Нажмите кнопку Добавить.
8. В поле "Код номенклатуры" введите "0160".
9. В поле "Размер" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
10. В списке перейдите по ссылке в выбранной строке.
11. В поле "Количество" введите число.
12. Нажмите кнопку Добавить.
13. В поле "Код номенклатуры" введите "0160".
14. В поле "Номер варианта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
15. В списке перейдите по ссылке в выбранной строке.
16. В поле "Количество" введите число.
17. Нажмите кнопку Добавить.
18. В поле "Код номенклатуры" введите "0175".
19. В поле "Количество" введите число.
20. Нажмите кнопку "Сохранить".
21. Закройте страницу.

## <a name="add-package-to-purchase-order"></a>Добавление пакета в заказ на покупку
1. Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".
2. Щелкните "Создать".
3. В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. В списке выберите поставщика, для которого ранее был создан пакет продуктов, если поставщик был выбран.
5. Переключите развертывание раздела "Общее".
6. В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
7. В списке перейдите по ссылке в выбранной строке.
8. В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
9. В списке перейдите по ссылке в выбранной строке.
10. Нажмите кнопку OK.
11. Переключите развертывание раздела "Сведения о строке".
12. Откройте вкладку "Пакеты продуктов".
13. Щелкните "Строка заказа на покупку".
14. Щелкните "Создать строки из пакета".
15. В списке найдите и выберите пакет продуктов, созданный в предыдущем шаге.
16. В поле "Количество" введите число.
17. Щелкните "Создать".
18. Нажмите кнопку "Сохранить".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]