---
title: Устранение неполадок при настройке и установке Store Commerce
description: В этой статье объясняется, как устранять проблемы при настройке и установке в приложении Microsoft Dynamics 365 Commerce Store Commerce.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 92d4a9d78485b681b4e802f695d54f44ecd7c5de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870474"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Устранение неполадок при настройке и установке Store Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

В этой статье объясняется, как устранять проблемы при настройке и установке в приложении Microsoft Dynamics 365 Commerce Store Commerce.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Невозможно активировать приложение, и выдается сообщение об ошибке подключения

После ввода допустимого URL-адреса CPOS может появиться сообщение об ошибке подключения, которое напоминает следующий пример:

> Произошла ошибка подключения, и устройство не может подключиться к CPOS. Введенный URL-адрес CPOS может иметь несколько ошибок.

В этом случае проверьте URL-адрес на наличие типографических ошибок или проверьте, не является ли CPOS недоступным, так как он отключен.

Кроме того, проверьте, что Cloud Scale Unit (CSU) имеет версию 10.0.25 (9.35.\*.\*) или более позднюю. Для использования приложения Store Commerce требуется версия CPOS 10.0.25 или более поздняя.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Не удается установить приложение, так как уже установлено приложение Modern POS

Во время установки может появиться сообщение об ошибке, аналогичное показанному в следующем примере:

> Версия (9.\*.\*.\*) этого продукта (Modern POS) была ранее установлена через устаревший установщик.

Чтобы исправить ошибку, необходимо удалить приложение MPOS для всех пользователей на компьютере и повторить попытку. Можно проверить, что приложение MPOS было удалено для всех пользователей, запустив следующую команду PowerShell.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Не удается активировать приложение из-за недопустимого URL-адреса или состояния ошибки

Если введенный URL-адрес CPOS является недопустимым и его нужно изменить, или если во время активации приложение Store Commerce находится в состоянии ошибки, можно перезапустить процесс, сбросив приложение. Приложение Store Commerce сохранит только допустимый URL-адрес CPOS.

Чтобы сбросить приложение Store Commerce, выполните следующие действия.

1. В меню **Пуск** Windows выберите и удерживайте (или щелкните правой кнопкой мыши) приложения, затем выберите **Дополнительно \> Параметры приложения**.
2. Прокрутите вниз страницу параметров приложения, пока не найдете кнопку **Сброс**.
3. Выберите **Сброс**. Затем при появлении запроса подтвердите, что хотите выполнить сброс приложения.
