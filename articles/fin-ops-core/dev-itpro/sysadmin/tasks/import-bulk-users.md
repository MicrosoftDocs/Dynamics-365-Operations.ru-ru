---
title: Импорт пользователей из Azure Active Directory
description: Эта процедура используется системными администраторами для импорта вручную выбранных пользователей или для импорта большого числа пользователей из Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce8c98add0c6d5fb07b3ba5338037d9a12b1d8e50a2d2039b0231d3d305c9ebe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748296"
---
# <a name="import-users-from-azure-active-directory"></a>Импорт пользователей из Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Импорт выбранных пользователей

Эта процедура используется системными администраторами для импорта выбранных пользователей из Azure Active Directory (Azure AD).

1. Пользователь будет импортирован с компанией текущего сеанса в качестве компании по умолчанию. Измените текущую компанию, если это применимо, прежде чем импортировать пользователей.
2. Перейдите в раздел **Администрирование системы > Пользователи > Пользователи**.
3. Щелкните **Импорт пользователей**.
4. Выберите пользователей, которых необходимо импортировать, и выберите **Импорт пользователей**.

После завершения импорта потребуется назначить роли пользователям.

## <a name="import-users-in-bulk"></a>Импорт пользователей в пакетном режиме

Эта процедура используется системными администраторами для импорта большого числа пользователей из Azure Active Directory.
Обратите внимание, что при использовании параметра пакетного импорта выбирать пользователей невозможно.

## <a name="run-the-import-as-a-batch-job"></a>Запуск импорта в качестве пакетной задачи
1. Пользователь будет импортирован с компанией текущего сеанса в качестве компании по умолчанию. Измените текущую компанию, если это применимо, прежде чем импортировать пользователей.
2. Перейдите в раздел **Администрирование системы > Пользователи > Пользователи**.
3. Выберите **Пакетный импорт**.
4. Разверните раздел **Выполнять в фоновом режиме**.
4. Выберите значение **Да** в поле **Пакетная обработка**.
6. В поле **Группа пакетной обработке** введите или выберите значение. Это необязательный шаг.  
7. Выберите **Да** в поле **Частный**. Это необязательный шаг.  
8. Выберите **Да** в поле **Критическое задание**. Это необязательный шаг.  
9. В поле **Категория мониторинга** выберите один из вариантов.
10. Щелкните **OK**.

После завершения импорта потребуется назначить роли пользователям.

## <a name="run-in-a-sandbox-environment"></a>Запуск в песочнице
1. Выберите **Пакетный импорт**.
2. Нажмите **ОК**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]