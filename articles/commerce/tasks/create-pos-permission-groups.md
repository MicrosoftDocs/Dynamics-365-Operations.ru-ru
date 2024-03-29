---
title: Создание групп разрешений POS
description: В этой статье объясняется, как создать группу разрешений POS.
author: josaw1
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailPosPermissionGroup, HcmJob
ms.openlocfilehash: 0aa394e5dc6685954c31cdddae7cdc042b80af29
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277969"
---
# <a name="create-pos-permission-groups"></a>Создание групп разрешений POS

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как создать группу разрешений POS. В качестве компании с демонстрационными данными для создания этой задачи используется USRT. Эта задача предназначена для роли директора-распорядителя в Commerce.

1. В области переходов выберите **Модули > Retail и Commerce > Сотрудники > Группы разрешений**.
2. Выберите **Создать**.
3. В поле **ИД группы POS-разрешений** введите значение.
4. В поле **Описание** введите значение.
5. Выберите **Да** в поле **Просмотр записей часов**. Теперь можно активировать или деактивировать различные разрешения для группы разрешений POS. Для некоторых разрешений можно установить значение, которое будет использоваться для проверки того, может ли пользователь терминала выполнять определенное действие. В этом руководстве по задачам включено несколько разрешение, которые можно предоставить кассиру.  
6. Выберите **Да** в поле **Разрешить создание заказа**.
7. Выберите **Да** в поле **Разрешить изменение заказа**.
8. Выберите **Да** в поле **Разрешить получение заказа**.
9. Выберите **Да** в поле **Разрешить изменение пароля**.
10. Выберите **Да** в поле **Разрешить закрытие "вслепую"**.
11. Нажмите **Сохранить**. После сохранения изменений необходимо запустить график распределения персонала, чтобы передать изменения в Commerce. 
12. В области перехода выберите **Модули > Управление персоналом > Должности > Должности**.
13. Теперь мы назначим группы разрешения POS заданию. В списке найдите и выберите требуемую запись.
14. Выберите **Правка**.
15. Разверните раздел **Классификация задний**.
16. В поле "Группа POS-разрешений" введите или выберите значение. Все работники на должностях для этого задания будут использовать настройки этой группы разрешений POS, если разрешения POS работника не были переопределены на уровне должности.  
17. Нажмите **Сохранить**. После сохранения изменений необходимо запустить график распределения персонала, чтобы передать изменения в каналы.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
