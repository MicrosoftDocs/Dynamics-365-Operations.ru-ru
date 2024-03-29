---
title: Диагностика безопасности для записей задач
description: В этой статье содержатся сведения о том, как анализировать требования к разрешениям безопасности и управлять ими на основе записи задачи.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.search.form: ''
ms.openlocfilehash: e564a0499cb1a5dc00fc027c20a027f9b454600c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272531"
---
# <a name="security-diagnostics-for-task-recordings"></a>Диагностика безопасности для записей задач

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Перед началом

В этой статье содержатся сведения о том, как анализировать требования к разрешениям безопасности и управлять ими на основе записи задачи. Перед выполнением шагов, описанных в этой статье, необходимо провести запись задачи бизнес-процесса, который требуется проанализировать. Для записи бизнес-процесса см. раздел [Ресурсы регистратора задач](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Управление безопасностью записи задач

1. Выберите **Администрирование системы** > **Безопасность** > **Диагностика безопасности для записи задач**.
2. Откройте запись задачи из нужного местоположения. Выберите **Открыть с этого компьютера** или **Открыть из Lifecycle Services**, а затем нажмите кнопку **Закрыть**.
3. Откроется страница **Сведения о пункте меню Безопасность**, на которой перечислены необходимые для процесса объекты безопасности.

 > [!NOTE]
 > Пункты меню **Действие** и **Вывод** не включаются в список.

4. В поле **ИД пользователя** выберите пользователя. Если у пользователя отсутствуют разрешения на доступ к некоторым пунктам меню, поле **Отсутствующие разрешения** будет обновлено на **Да**.
  
  ![Страница сведения о пункте меню "Безопасность".](../media/Security-Menu-Item-Details.png)

5. Выберите **Добавить ссылку**, чтобы просмотреть список объектов безопасности, включая роли, обязанности и привилегии, которые предоставляют отсутствующее разрешение.
6. Выберите объект безопасности из списка.

    - Если выбрана **Роль**, выберите **Добавить роль для пользователя**. Откроется страница **Назначить пользователей ролям**. Дополнительные сведения см. в разделе [Назначение пользователей для ролей безопасности](assign-users-security-roles.md).
    - Если выбрано **Полномочие**, выберите **Добавить полномочие для роли**, выберите роли, к которым следует добавить полномочие, а затем нажмите кнопку **ОК**.
    - Если выбрана **Привилегия**, выберите **Добавить привилегию для полномочий**, выберите роли, к которым следует добавить полномочие, а затем нажмите кнопку **ОК**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
