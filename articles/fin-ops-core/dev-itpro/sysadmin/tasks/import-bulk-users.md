---
title: Импорт пользователей в пакетном режиме
description: Эта процедура используется системными администраторами для импорта большого числа пользователей из Azure Active Directory.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d8b55895c9dfaf1c69cd319697f1e0da5990daf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144095"
---
# <a name="import-users-in-bulk"></a>Импорт пользователей в пакетном режиме

[!include [banner](../../includes/banner.md)]

Эта процедура используется системными администраторами для импорта большого числа пользователей из Azure Active Directory.


## <a name="run-as-a-batch-job"></a>Выполнить пакетное задание
1. Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".
2. Щелкните "Пакетный импорт".
3. Разверните раздел "Выполнять в фоновом режиме".
4. Выберите значение "Да" в поле "Пакетная обработка".
5. В поле "Описание задачи" введите значение.
6. В поле "Группа партий" введите или выберите значение.
    * Это необязательный шаг.  
7. Выберите "Да" в поле "Частный".
    * Это необязательный шаг.  
8. Выберите "Да" в поле "Критическое задание".
    * Это необязательный шаг.  
9. В поле "Категория мониторинга" выберите один из вариантов.
10. Нажмите кнопку "OК".

## <a name="run-in-a-sandbox-environment"></a>Запуск в песочнице
1. Щелкните "Пакетный импорт".
2. Нажмите кнопку "OК".

