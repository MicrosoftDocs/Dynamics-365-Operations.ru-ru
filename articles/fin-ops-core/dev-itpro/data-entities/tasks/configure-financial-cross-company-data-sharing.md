---
title: Настройка совместного использования финансовых данных компаниями
description: В этой процедуре описывается, как настроить, включить, проверить и разрешить конфликты при обмене данными между компаниями.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35ec8fc809841c0830224646fb57b0e4e4d40ef4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752300"
---
# <a name="configure-financial-cross-company-data-sharing"></a>Настройка совместного использования финансовых данных компаниями

[!include [banner](../../includes/banner.md)]

В этой процедуре описывается, как настроить, включить, проверить и разрешить конфликты при обмене данными между компаниями. В ней используется компания с демонстрационными данными USMF и шаблон публикации финансовых данных.

Для выполнения этого руководства по задаче требуется платформа Dynamics AX 7.1 или более поздней версии.

1. Перейдите в раздел **Область переходов > Модули > Администрирование системы > Рабочие области > Управление данными**.
2. Нажмите кнопку **Импорт**.
3. В поле **Имя** введите значение.
4. В поле **Формат исходных данных** выберите "Тип упаковки". Щелкните **Загрузить**. Перейдите к расположению файла пакета шаблона публикации финансовых данных и выберите этот файл.
5. Нажмите кнопку **Сохранить**.
6. В списке пометьте выбранную строку. Выберите только что созданную политику обмена данными.  
7. Нажмите кнопку **Импорт**.
8. Нажмите кнопку **Закрыть**.
9. Обновите страницу.
10. Закройте страницу.
11. Закройте страницу.
12. Закройте страницу.
13. Перейдите в раздел **Область переходов > Модули > Администрирование системы > Настройка > Настройка совместного использования данных компаниями**.
14. В списке найдите и выберите **Платежные дни**.
15. Нажмите кнопку **Добавить**.
16. В списке пометьте выбранную строку.
17. В поле **Компания** введите "USSI".
18. Нажмите кнопку **Добавить**.
19. В поле **Компания** введите "USMF".
20. Нажмите кнопку **Сохранить**.
21. Щелкните **Включить**.
22. Нажмите кнопку **Да**.
23. Щелкните **Поиск проблем совместного использования**.
24. Нажмите кнопку **Да**.
25. Щелкните **Обновить значение поля**.
26. Щелкните **Использовать значение из компании 1**.
27. Обновите страницу.
28. Закройте страницу.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]