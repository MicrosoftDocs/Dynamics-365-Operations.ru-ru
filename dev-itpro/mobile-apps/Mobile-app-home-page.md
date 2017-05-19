---
title: "Домашняя страница мобильного приложения Dynamics 365 for Operations"
description: "В этом разделе описывается мобильное приложение Microsoft Dynamics 365 for Operations и предоставляются ссылки на ресурсы, которые помогут вам реализовать его в вашей организации."
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e1a9e0eeb45f011ccb2aa091e68aff92782e1ae7
ms.contentlocale: ru-ru
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Домашняя страница мобильного приложения Dynamics 365 for Operations

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]


В этом разделе описывается мобильное приложение Microsoft Dynamics 365 for Operations и предоставляются ссылки на ресурсы, которые помогут вам реализовать его в вашей организации.

<a name="overview"></a>Обзор
--------

Мобильное приложение Microsoft Dynamics 365 for Operations позволяет вашей организации сделать свои бизнес-процессы доступными для мобильных устройств. После того как ваш ИТ-администратор включит функцию мобильных рабочих областей для вашей организации, пользователи могут войти в приложение и немедленно приступить к выполнению бизнес-процессов со своих мобильных устройств. Мобильное приложение Dynamics 365 for Operations включает в себя следующие функции, которые могут помочь повысить производительность:

-   Пользователи могут просматривать и редактировать бизнес-данные, а также действовать на их основе, даже если они имеют непостоянное подключение к сети или их мобильные устройства полностью отключены от сети. Когда устройство восстанавливает подключение к сети, операций с данными в автономном режиме автоматически синхронизируются с Dynamics 365 for Operations.
-   Администраторы ИТ или разработчики могут создавать и публиковать мобильные рабочие области, которые были адаптированы для их организации. Приложение использует существующие ресурсы кода. Таким образом, не нужно повторно реализовать ваши процедуры проверки, бизнес-логику или конфигурацию безопасности.
-   Администраторы ИТ или разработчики могут легко разрабатывать мобильные рабочие области с помощью конструктора рабочих областей типа "указать и нажать", который входит в состав веб-клиента Dynamics 365 for Operations.
-   Администраторы ИТ или разработчики при необходимости могут оптимизировать возможности автономной работы рабочих областей с помощью платформы расширения бизнес-логики. Поскольку данные по-прежнему будет обрабатываться, пока устройство является автономным, мобильные сценарии остаются содержательными и гибкими, даже если у устройства нет постоянного сетевого подключения.

## <a name="elements-of-the-mobile-app"></a>Элементы мобильного приложения
Навигация в мобильном приложении состоит из четырех простых концепций: панель мониторинга, рабочие области, страницы и действия. 

[![Концепции навигации в мобильном приложении](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   При запуске приложения можно перейти к **панель мониторинга**.
-   На панели мониторинга можно просмотреть список **рабочих областей**, опубликованных в вашей среде Dynamics 365 for Operations.
-   В каждой рабочей области можно просмотреть список **страниц**, доступных для этой рабочей области.
-   На странице можно просмотреть данные, собранные с одной или нескольких страниц в Dynamics 365 for Operations.
-   Со страницы можно переходить на другие страницы для соответствующих данных, например сведения о записи или строках.
-   На странице можно также просмотреть список **действий**, которые доступны для этой страницы.
-   Действия позволяют создавать или редактировать существующие данные.

## <a name="implementation-process"></a>Процесс внедрения
На следующем рисунке показана процесс внедрения мобильного приложения Dynamics 365 for Operations в вашей организации. 

[![](./media/mobile-implementation-process_4.png)](./media/mobile-implementation-process_4.png) 

В следующей таблице приведены ссылки на ресурсы, которые могут помочь внедрить мобильное приложение Dynamics 365 for Operations в вашей организации. Цифры в первом столбце соответствуют пронумерованным шагам на предыдущем рисунке.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Шаг</th>
<th>Роль</th>
<th>Действие</th>
<th>Ресурсы, помогающие выполнить действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Системный администратор</td>
<td>Реализуйте Dynamics 365 for Operations в организации.</td>
<td>Если система Dynamics 365 for Operations еще не развернута в вашей организации, см. раздел <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Развертывание демонстрационной среды Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Системный администратор</td>
<td>Загрузите и установите KB, обеспечивающие использование мобильных рабочих областей, которые предоставляются корпорацией Microsoft.</td>
<td>См. раздел &quot;Необходимые условия&quot; в разделе о мобильной рабочей области, которую ваша организация хочет использовать:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Мобильные рабочие области управления затратами</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Мобильная рабочая область запасов в наличии</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Мобильные рабочие области заказов на продажу</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Мобильная рабочая область совместной работы с поставщиками</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Мобильная рабочая область регистрации времени по проекту</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Системный администратор</td>
<td>Опубликуйте мобильные рабочие области, поставляемые корпорацией Microsoft.</td>
<td>См. раздел &quot;Необходимые условия&quot; в разделе о мобильной рабочей области, которую ваша организация хочет использовать:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Мобильные рабочие области управления затратами</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Мобильная рабочая область запасов в наличии</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Мобильные рабочие области заказов на продажу</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Мобильная рабочая область совместной работы с поставщиками</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Мобильная рабочая область регистрации времени по проекту</a></li>
</ul></td>
</tr>
<tr class="even">
<td>4</td>
<td>Разработчик или независимый поставщик программного обеспечения (ISV)</td>
<td>Используйте мобильную платформу Dynamics 365 for Operations для создания настраиваемых мобильных рабочих областей.</td>
<td><ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Мобильная платформа Dynamics 365 for Operations</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Интерфейсы API X++ рабочей области Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Создайте пакет развертывания, содержащий настраиваемые мобильные рабочие области, и отправьте пакет в службы Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Создание пакета развертывания</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Системный администратор</td>
<td>Примените пакет развертывания, содержащий настраиваемые рабочие области, предоставленные независимым производителем программного обеспечения.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Применение пакета развертывания в системе Microsoft Dynamics 365 for Operations</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Системный администратор</td>
<td>Опубликуйте настраиваемые мобильные рабочие области, поставляемые независимым разработчиком программного обеспечения.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/publish-mobile-workspace">Публикация мобильной рабочей области</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Пользователь</td>
<td>Загрузите и установите мобильное приложение Dynamics 365 for Operations.</td>
<td><ul>
<li>Для Android: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations в магазине Google Play</a></li>
<li>Для iPhone: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations в магазине приложений iTunes</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Пользователь</td>
<td>Выполните вход и используйте мобильное приложение Dynamics 365 for Operations. Приложение включает в себя мобильные рабочие области, которые были опубликованы.</td>
<td>Корпорация Microsoft предоставляет следующие мобильные рабочие области:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Мобильные рабочие области управления затратами</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Мобильная рабочая область запасов в наличии</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Мобильные рабочие области заказов на продажу</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Мобильная рабочая область совместной работы с поставщиками</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Мобильная рабочая область регистрации времени по проекту</a></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>См. также
--------

[Мобильные рабочие области, недавно выпущенные для мобильного приложения Dynamics 365 for Operations](mobile-workspaces-released.md)





