---
title: Создание и связывание станции оборудования
description: Эта процедура содержит инструкции по созданию станции оборудования.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4402e8d1179499512034e7deb8b3eb78f12096f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798593"
---
# <a name="create-and-associate-a-hardware-station"></a>Создание и связывание станции оборудования

[!include [banner](../includes/banner.md)]

Эта процедура содержит инструкции по созданию станции оборудования. Новый профиль оборудования будет создан и будет использован для добавления новых станций оборудования в предварительно определенный магазин (канал). В этой процедуре используется компания с демонстрационными данными USRT.

1. Перейдите в раздел "Реквизиты Commerce" > "Каналы" > .. > .. > .. > "Профили станции оборудования".
2. Щелкните "Создать".
3. В поле "Код станции оборудования" введите "TestHWProfile".
4. В поле "Имя" введите значение.
5. В поле "Номер порта" введите число.
6. В поле "Профиль оборудования" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
7. Поиск и выбор требуемой записи в списке.
8. В списке перейдите по ссылке в выбранной строке.
9. В поле "Имя пакета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
10. В списке перейдите по ссылке в выбранной строке.
    * Это стандартный пакет, поставляемый с новой средой. Номер версии может отличаться.  
11. Нажмите кнопку Сохранить.
12. Закройте страницу.
13. Перейдите в раздел Retail и Commerce > Каналы > Все магазины.
14. В списке выберите строку 17.
    * При использовании компании демонстрационных данных USRT это будет магазин в Хьюстоне.  
15. В списке перейдите по ссылке в выбранной строке.
16. Переключите развертывание раздела "Станции оборудования".
17. Нажмите кнопку Добавить.
18. В списке пометьте выбранную строку.
19. В поле "Код профиля" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
20. В списке найдите и выберите требуемую запись.
    * Это должен быть новый профиль станции оборудования, созданных на предыдущих шагах.  
21. В списке перейдите по ссылке в выбранной строке.
22. В поле "Имя узла" введите значение.
23. В поле "Код терминала EFT" введите значение.
24. Нажмите кнопку "Сохранить".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]