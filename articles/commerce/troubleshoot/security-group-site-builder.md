---
title: Во время начального развертывания невозможно настроить группу безопасности для конструктора сайтов Commerce
description: В этом разделе приведены инструкции по устранению неполадок, которые могут помочь, когда группа безопасности Microsoft Azure Active Directory (Azure AD) для конструктора сайтов Commerce не отображается в качестве параметра при создании компонентов электронной коммерции в Microsoft Dynamics Lifecycle Services (LCS) в ходе начального развертывания нового клиента электронной коммерции.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: aa00e9331693600ced2f4ead399a0c005b77ad08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801515"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Во время начального развертывания невозможно настроить группу безопасности для конструктора сайтов Commerce

[!include [banner](../../includes/banner.md)]

В этом разделе приведены инструкции по устранению неполадок, которые могут помочь, когда группа безопасности Microsoft Azure Active Directory (Azure AD) для конструктора сайтов Commerce не отображается в качестве параметра при создании компонентов электронной коммерции в Microsoft Dynamics Lifecycle Services (LCS) в ходе начального развертывания нового клиента электронной коммерции.

## <a name="description"></a>описание

При создании компонентов электронной коммерции в рамках процесса развертывания нового клиента электронной коммерции, который содержит компонент конструктора сайтов Commerce, группа безопасности Azure AD не отображается в диалоговом окне в качестве параметра.

## <a name="resolution"></a>Приказ

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Предоставьте сайту электронной коммерции пользователя в надлежащем клиенте

1. Перейдите в раздел [порталу Azure](https://portal.azure.com/).
1. В рамках клиента, для которого был предоставлен проект LCS для вашего сайта электронной коммерции, следуйте указаниям в разделе [Создание базовой группы и добавление участников с помощью Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Перейдите в раздел [LCS](https://lcs.dynamics.com/) и выполните вход, используя учетную запись, которая использует тот же клиент, что и только что созданная группа безопасности Azure AD. Учетная запись должна иметь доступ для просмотра группы безопасности Azure AD.
1. Выполните шаги настройки для настройки сайта электронной коммерции. При подготовке компонентов электронной коммерции в диалоговом окне теперь группа безопасности должна отображаться как параметр.

> [!NOTE]
> Чтобы поле в диалоговом окне было заполнено списком групп безопасности, необходимо выбрать **Ввод** после ввода имени созданной группы безопасности Azure AD. В результатах поиска будут перечислены все группы безопасности Azure AD, которые начинаются с текста поиска, и к которым пользователь имеет доступ. Можно использовать более короткое условие поиска, чтобы иметь возможность расширить результаты поиска.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Создание базовой группы и добавление участников с помощью Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Развертывание нового арендатора электронной коммерции](../deploy-ecommerce-site.md)
