---
title: Что нового и что изменилось в Dynamics 365 Supply Chain Management 10.0.6 (ноябрь 2019 г.)
description: В этой теме описываются новые и измененные компоненты Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 83798af9c39ae8845125026903741882356d8845
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909337"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Что нового и что изменилось в Dynamics 365 Supply Chain Management 10.0.6 (ноябрь 2019 г.)

[!include [banner](../includes/banner.md)]

В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Supply Chain Management 10.0.6. Эта версия имеет номер сборки 10.0.234. Хотя общая дата доступности находится в ноябре, новые функции доступны для раннего выпуска в октябре. Дополнительные сведения о версии 10.0.6 см. в разделе [Дополнительные ресурсы](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>Информационный объект моделей конфигурации продукта версии 2

Вторая версии для информационного объекта "модели конфигурации продукта" выпускается (называется "модели конфигурации продуктов версии 2"). Шаблон по умолчанию "418 — модели конфигурации продукта" также должен быть, так как он использует новый информационный объект "модели конфигурации продукта версии 2" в шаблонах структуры импорта/экспорта. Шаблон не будет автоматически обновляться, так что потребуется загрузить шаблон по умолчанию вручную. Объект версии 2 экспортирует одну строку как отдельный файл во вложение, а не в виде встроенного файла, что устраняет ограничения размера у объекта версии 1. 
 
Что необходимо сделать, чтобы принять это изменение?
-    Поскольку сущность версии 1 устарела, следует начать переход с версии 1 на версию 2. При использовании шаблона "418 — модели конфигурации продукта" можно нажать кнопку "загрузить шаблоны по умолчанию" и перезагрузить шаблон "418 — модели конфигурации продукта"
-    Если необходимо обеспечить совместимость с существующими системами, можно сейчас продолжить работу с существующим шаблоном и (устаревшим) объектом версии 1 до переноса интеграций в новый шаблон. 

## <a name="feature-management-enhancements"></a>Улучшения управления функциями
Теперь управление функциями позволяет включить все новые возможности по умолчанию, требовать подтверждения включения функции и включить все функции, которые еще не были включены. 


## <a name="purchase-agreement-responsible-party"></a>Ответственный субъект договора покупки
Теперь имеется возможность определить основных и дополнительных ответственных лиц в форме классификации договоров покупки и полученных в результате договорах покупки.  Это предоставляет пользователю доступ к тем, кто контролирует договора.

## <a name="rfq-link-on-the-purchase-order-line"></a>Скидка запроса предложения в строке заказа на покупку
Можно добавить справочную ссылку из строк заказа на покупку назад в соответствующие строки запроса предложения, из которых они созданы, что позволяет пользователю легко получить доступ к соответствующему документу запроса предложения.

## <a name="additional-resources"></a>Дополнительные ресурсы

### <a name="bug-fixes"></a>Исправления ошибок
Для получения сведений об исправлениях ошибок, включенных в каждое из обновлений, которые являются частью 10.0.6, войдите в службы Lifecycle Services (LCS) и просмотрите [статью базы знаний](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Обновление платформы update 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 включает обновление платформы Platform update 30. Дополнительные сведения об обновлении платформы Platform update 30 см. в разделе [Что нового и что изменилось в обновлении платформы Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: план выпуска волны 2 за 2019 год
Интересуетесь предстоящими и недавно выпущенными возможностями наших бизнес-приложений и платформ?

Ознакомьтесь с разделом [Dynamics 365: план выпуска волны 2 за 2019 год](/dynamics365-release-plan/2019wave2/). Мы собрали в одном документе все сведения, чтобы вы могли использовать их для планирования.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Удаленные и устаревшие функции Supply Chain Management

В теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) описываются функции, которые запланированы к удалению или которые планируется удалить или объявить устаревшими для Supply Chain Management.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Перед удалением каких-либо функций из продукта уведомление об устаревании будет объявлено в теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) за 12 месяцев до удаления.

Для критических изменений, которые влияют только на время компиляции, но являются двоично совместимыми с песочницей и производственными средами, время устаревания будет меньше 12 месяцев. Обычно это функциональные обновления, которые должны быть выполнены для компилятора.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]