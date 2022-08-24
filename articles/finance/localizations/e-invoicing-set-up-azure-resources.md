---
title: Настройка ресурсов Azure для электронного выставления накладных
description: В этой статье представлен обзор процесса настройки ресурсов Microsoft Azure для электронного выставления накладных.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f11e4eac831d54a6cac765a5adc4e4ffddbe0a22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283096"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Настройка ресурсов Azure для электронного выставления накладных

[!include [banner](../includes/banner.md)]

Процесс настройки ресурсов Microsoft Azure для электронного выставления накладных имеет три шага. Первые два шага, "Создание хранилища Azure Key Vault на портале Azure" и "Создание учетной записи хранения Azure на портале Azure", являются обязательными. Третий шаг, "Настройка подключения SharePoint", не является обязательным.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Создание Azure Key Vault на портале Azure

Создайте хранилище ключей в вашей подписке Azure. Рекомендуется создать отдельное хранилище ключей для электронного выставления накладных и не объединять секреты с другими приложениями. Создайте столько секретов и сертификатов, сколько требуется для сценариев в электронных документах. Необходимо создать хотя бы один секрет для сохранения маркера подписанного URL-адреса (SAS) учетной записи хранения Azure, которая будет создана на следующем шаге.

Сведения о том, как выполнить этот шаг, см. в разделе [Создание Azure Key Vault на портале Azure](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Создание учетной записи службы хранилища Azure на портале Azure

Вы владеете всеми электронными документами и файлами, которые создаются службой электронного выставления накладных или входят в службу. Эти документы и файлы хранятся в учетной записи хранения Azure, которая создается в вашей подписке Azure. Служба будет обращаться к учетной записи хранения, используя токен SAS, взятую из вашего секрета Key Vault.

Сведения о том, как выполнить этот шаг, см. в разделе [Создание учетной записи хранения Azure на портале Azure](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>Настройка подключения SharePoint

В некоторых сценариях может потребоваться сохранить электронные файлы в SharePoint и извлечь их из SharePoint. Чтобы служба электронного выставления накладных могла получать доступ к вашим папкам SharePoint, настройте доступ к SharePoint.

Сведения о том, как выполнить этот шаг, см. в разделе [Настройка подключения к SharePoint](e-invoicing-create-sharepoint-connection.md).
