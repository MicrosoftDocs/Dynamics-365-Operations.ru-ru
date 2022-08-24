---
title: Установка темы Adventure Works
description: В этой статье описывается, как установить тему Adventure Works в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274295"
---
# <a name="install-the-adventure-works-theme"></a>Установка темы Adventure Works

[!include [banner](includes/banner.md)]

В этой статье описывается, как установить тему Adventure Works в Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Тема Adventure Works и модули доступны в выпуске Dynamics 365 Commerce версии 10.0.20. Они доступны из Microsoft AppSource.

## <a name="prerequisites"></a>Необходимые условия

Перед установкой темы Adventure Works необходимо иметь среду Dynamics 365 Commerce (Commerce версии 10.0.20 или более поздней версии), которая включает Retail Cloud Scale Unit (RCSU), пакет средств разработки программного обеспечения для Commerce Online (SDK) и библиотеку модуля Commerce. Сведения об установке пакета SDK и библиотеки модулей Commerce см. в разделе [Настройка среды разработки](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>Этапы установки

### <a name="install-the-adventure-works-theme-in-your-application"></a>Установка темы Adventure Works в приложение

Пакет темы Adventure Works доступен на канале **dynamics365-commerce** как **@msdyn365-commerce-theme/adventureworks-theme-kit**. Однако хотя пакет темы Adventure Works является частью этого канала, он находится под своим пространством имен. Таким образом, для добавления записей реестра для пространства имен необходимо выполнить следующие действия.

1. Обновите файл **.npmrc** таким образом, чтобы он включал следующую запись реестра (если эта запись еще не включена):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Обновите файл **.yarnrc** таким образом, чтобы он включал следующую запись реестра (если эта запись еще не включена):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Чтобы установить пакет в локальной среде, выполните команду `yarn add THEME_PACKAGE@VERSION` из командной строки, где **THEME_PACKAGE** является пакетом тем (@msdyn365-commerce-theme/adventureworks-theme-kit) и **VERSION** — это номер версии используемой библиотеки модулей. Важно, чтобы версии пакета тем и библиотеки модулей совпадали. Чтобы найти правильный номер версии библиотеки модулей для использования, откройте файл package.json и найдите значение **starter-pack** в разделе **dependencies**. В следующем примере файл package.json использует версию 9.32 библиотеки модулей, которая сопоставляется с выпуском Dynamics 365 Commerce версии 10.0.22.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

В следующем примере показано, как выполнить команду `yarn add` для добавления версии 9.32 темы Adventure Works. Команда автоматически обновляет файл package.json, чтобы он включал в себя зависимость.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

Дополнительные сведения об обновлении версии библиотеки модулей см. в разделе [Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md). 

> [!IMPORTANT]
> - Версия темы должна соответствовать версии библиотеки модулей, чтобы гарантировать, что все функции работают так, как ожидалось. 
> - Минимальная версия для библиотеки модуля Commerce и SDK должна быть 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Добавление файлов шрифтов для темы Adventure Works

После установки темы Adventure Works в приложение необходимо добавить необходимые для нее файлы шрифтов. Чтобы выполнить этот шаг, скопируйте все файлы шрифтов из папки **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** в путь к общедоступному каталогу партнерских приложений **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Настройка ресурсов для темы Adventure Works

Следующим шагом является обновление необходимого для темы ресурса по умолчанию. Чтобы выполнить этот шаг, скопируйте содержимое из файла global.json в папке **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** в файл global.json партнерского приложения по пути **\src\resources\modules**. Если каталог назначения **\src\resources** не существует, его можно полностью скопировать из исходного каталога **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** в целевой каталог **\src**.

### <a name="pull-updates-and-validate-the-theme"></a>Извлечение обновлений и проверка темы

Сведения о том, как извлечь последнюю версию пакета SDK, библиотеки модулей и других обновлений зависимостей, см. в разделе "Извлечение обновлений" из [обновлений пакета SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#pull-updates).

После извлечения последних зависимостей можно выполнить команду **yarn start**, чтобы запустить сервер узла в среде разработки и протестировать новую тему Adventure Works. Просмотрите локально приложение, используя параметр строки запроса `?theme=adventureworks` (например, `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Тема Adventure Works](adventure-works-theme.md)

[Обзор библиотеки модулей](starter-kit-overview.md)

[Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
