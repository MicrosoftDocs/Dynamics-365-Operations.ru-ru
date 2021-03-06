---
title: Удаление экземпляра
description: В этой статье содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72a5b99150e5ccdf9a542b569c94c64cb95923fd
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053619"
---
# <a name="remove-an-instance"></a>Удаление экземпляра

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Удаление тестовой среды

Тестовые среды Human Resources подготавливаются с политикой срока действия 60 дней. Тем не менее владельцы тестовых сред могут прекратить пробную эксплуатацию раньше, выполнив следующие действия. 

1. Перейдите к [Центру администрирования Power Apps](https://admin.businessplatform.microsoft.com/).
2. Выберите **Среды**.
3. Выберите тестовую среду, имя которой построено по следующему шаблону: TestDrive - alias@domain
4. Выберите **Удалить** и подтвердите решение. 

Существующая тестовая среда будет удалена. При ее удалении вы можете зарегистрироваться на новую тестовую среду. 

## <a name="remove-a-production-environment"></a>Удаление производственной среды

В этой статье предполагается, что вы приобрели Human Resources в соответствии с соглашением поставщика облачных решений (CSP) или архитектуры предприятия (EA). 

Так как в одна среда Human Resources содержится в одной среде Power Apps, существуют две возможности. Первый вариант включает в себя удаление всей среды Power Apps; второй вариант включает в себя удаление только Human Resources. Первый вариант предпочтителен, если среда Power Apps была создана специально в целях подготовки Human Resources, и вы только начали реализацию или не имеете никаких установленных интеграций. Второй вариант подходит при наличии установившейся среды Power Apps, заполненной богатыми данными, которое используются в Power Apps и Power Automate.

> [!Important]
> Перед удалением среды Power Apps убедитесь, что она не используется для интеграции богатых данных вне Human Resources. Также обратите внимание, что удаление сред Power Apps по умолчанию невозможно. 

Чтобы удалить всю среду Power Apps, включая Human Resources и связанные приложения и потоки:

1. Перейдите к [Центру администрирования Power Apps](https://admin.businessplatform.microsoft.com/).
2. Выберите **Среды**.
3. Выберите среду для удаления.
4. Выберите **Удалить** и подтвердите решение. 
5. Дождитесь завершения удаления.
6. Выполните вход в [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) с помощью учетной записи, используемой для подписки на Human Resources. 
7. Выберите проект Human Resources, который содержит среду. 
8. В проекте LCS выберите плитку **Управление приложением Human Resources**. 
9. Выберите экземпляр для удаления. 
10. Выберите **Удалить экземпляр** и подтвердите этот выбор.  

Чтобы удалить среду Human Resources из существующей среды Power Apps, выполните следующие действия. Обратите внимание, что временно необходимо обращаться в службу поддержки и связываться с группой Human Resources DevOps, пока эта функция не будет включена непосредственно в LCS.

1. Обратитесь в службу поддержки, чтобы инициировать запрос на удаление.
2. Группа поддержки инициирует запрос на удаление в группе Human Resources DevOps. 
3. Продолжите после получения сообщения, что среда была удалена.
4. Выполните вход в LCS с помощью учетной записи, используемой для подписки на Human Resources. 
5. Выберите проект Human Resources, который содержит среду. 
6. В проекте LCS выберите плитку **Управление приложением Human Resources**. 
7. Выберите экземпляр, который вы хотите удалить, которой должен быть помечен статусом развертывания **Удалено**.
8. Выберите **Удалить экземпляр** и подтвердите этот выбор. 

## <a name="recover-a-soft-deleted-environment"></a>Восстановление среды с мягким удалением

При удалении среды Power Apps, к которой подключена среда Human Resources, статус среды Human Resources в Lifecycle Services будет **мягко удален**. В этом случае пользователи не смогут подключаться к Human Resources.

Чтобы восстановить среду:

1. Следуйте указаниям раздела [Восстановление среды Power Apps](/power-platform/admin/recover-environment.md).

2. Обратитесь в службу поддержки, чтобы восстановить среду Human Resources. Для получения дополнительных см. [Получение поддержки](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Среды Power Apps сохраняются только в течение семи дней после удаления. Среду следует восстанавливать в течение семи дней.


[!INCLUDE[footer-include](../includes/footer-banner.md)]