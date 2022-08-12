---
title: Устранение проблем с расширением Store Commerce
description: В этой статье объясняется, как устранять проблемы с расширением в приложении Microsoft Dynamics 365 Commerce Store Commerce.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b440183e255e05c4f93a4f11106be2967163ff74
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169026"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Устранение проблем с расширением Store Commerce

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как устранять проблемы с расширением в приложении Microsoft Dynamics 365 Commerce Store Commerce.

## <a name="extensions-packages-arent-loaded"></a>Пакеты расширений не загружены

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Пакеты расширений не отображаются на странице POS \> Параметры

Триггеры Commerce Runtime (CRT) могли быть не обновлены для включения пакета расширения, или они не развернуты. Дополнительные сведения см. в разделе [Расширяемость и триггеры среды Commerce Runtime (CRT)](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Пакеты расширений отображаются на странице POS \> Параметры, но манифест не загружен

Убедитесь, что пакеты расширений существуют в папке **C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions**. Если пакеты существуют, должна быть папка **POS**, содержащая манифест.

Если папка **POS** отсутствует, убедитесь, что проект Store Commerce правильно ссылается на проект расширения POS. Проверьте путь ссылки на проект и убедитесь, что он существует. 

В следующем примере проект установщика испытывает проблемы с проектом расширения, на который указывает ссылка.

![Ссылка на проект установщика Store Commerce недействительна.](media/ReferenceNotValid.png)

Если ссылка для проекта расширения добавлена правильно, в проекте установщика не будет никаких предупреждений или проблем зависимостей, как показано в следующем примере.

![Ссылка на проект установщика Store Commerce действительна.](media/ReferenceValid.png)
