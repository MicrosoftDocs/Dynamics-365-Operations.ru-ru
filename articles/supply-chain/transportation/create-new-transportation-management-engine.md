---
title: Создание нового механизма управления транспортировкой
description: В этой статье описывается, как создать новый механизм управления транспортировкой в Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 627972ef6afb7551bb57821ded24183f8f335e9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857267"
---
# <a name="create-a-new-transportation-management-engine"></a>Создание нового механизма управления транспортировкой

[!include [banner](../includes/banner.md)]

В этой статье описывается, как создать новый механизм управления транспортировкой в Dynamics 365 Supply Chain Management. 

Механизмы управления транспортировкой (TMS) определяют логику, которая используется для создания и обработки ставок транспортировки в модуле "Управление транспортировкой". Supply Chain Management содержит несколько различных типов механизмов, которые рассчитывают различные параметры, такие как ставки, время транспортировки и число зон, которые будут пересечены при транспортировке. В этой статье объясняется, как использовать среду разработки Microsoft Visual Studio вместе со средствами разработки Supply Chain Management для создания и развертывания нового механизма TMS, а затем для настройки механизма в Operations. Дополнительные сведения об этих механизмах см. в разделе [Механизмы управления транспортировкой](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Создание механизма TMS

В этом разделе объясняется, как создать библиотеку классов, в которой реализована система TMS, и как ссылаться на нее из модели Supply Chain Management.

1. Для развертывания новых механизмов необходима модель, которая будет содержать механизмы. В меню **Dynamics 365** &gt; **Управление моделями** нажмите **Создать модель** для создания новой модели. На первой странице мастера **Создать модель** назовите модель **TMSEngines**. 

   [![Создание модели.](./media/012.png)](./media/012.png)

2. На следующей странице выберите **Создать новый пакет**. 

   [![Создание нового пакета.](./media/021.png)](./media/021.png)

3. На следующей странице выберите модель **ApplicationSuite** для ссылки. (Предварительно выбрана модель **ApplicationPlatform**.) 

   [![Выбор модели для ссылки.](./media/032.png)](./media/032.png)

4. На следующей странице нажмите **Готово**, чтобы подтвердить создание новой модели. 

   [![Завершение создания модели.](./media/042.png)](./media/042.png)

5. В новом решении создайте новый проект Supply Chain Management и назовите его **TMSThirdParty**. В свойствах проекта задайте для модели проекта значение **TMSEngines**.
6. Добавьте новую библиотеку классов C\# в решение и назовите ее **ThirdPartyTMSEngines**.
7. В проекте ThirdPartyTMSEngines добавьте ссылки на сборки для Supply Chain Management:
   -   Сборки приложений, которые позволяют ссылаться на типы X++. Эти сборки можно найти в следующих местоположениях. \[Корень пакетов\] — это путь к местоположению, в котором размещаются все развернутые сборки, например, C:\\Packages.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Сборки структуры, которые позволяют осуществлять доступ к данным, LINQ и вспомогательным функциям. Все эти сборки можно найти в \[Корень пакетов\]\\bin.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   Основная сборка системы TMS (которая содержит механизмы) и базовая сборка TMS (которая содержит помощники, константы, определения классов для перемещения данных и т. д.). Эти сборки можно найти в следующих местоположениях.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Переименуйте класс C\#, который автоматически создается в проекте ThirdPartyTMSEngines на **SampleRatingEngine**.
9. Реализуйте механизм. Поскольку в этом примере создается механизм ставок, мы наследуем из базового класса для механизмов ставок. Базовый класс реализует основную часть интерфейса механизма ставок (**TMSFwkIRateEngine**). Нам просто нужно реализовать метод ставок. Чтобы этот пример был простым, мы сделаем так, чтобы этот метод регистрировал жестко запрограммированную ставку 100. Можно создавать механизмы, которые реализуют любые интерфейсы механизмов, такие как **TMSFwkIAccessorialEngine**. Все интерфейсы механизмов определены в X++.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Постройте решение.
11. Добавьте новую ссылку в проект TMSThirdParty. Ссылка должна указывать на проект ThirdPartyTMSEngines. По завершении работы решение должно выглядеть следующим образом. 

    [![Решение, содержащее ссылку на проект TMSThirdParty.](./media/052.png)](./media/052.png)

12. Постройте решение. Убедитесь, что новая библиотека отображается в узле **Ссылки** в обозревателе приложений. 

    [![Новая библиотека в узле ссылок в обозревателе приложений.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Развертывание механизмы TMS в качестве пакета

Одним из способов развертывания механизмов TMS сторонних производителей является пакет развертывания. Этот подход рекомендуется в рабочей среде. В среде разработки можно вручную копировать сборки, как описано в следующем разделе, "Настройка механизма TMS в Supply Chain Management". Чтобы развернуть модуль в качестве пакета, выполните следующие действия.

1. В меню **Dynamics 365** &gt; **Развертывание** щелкните <strong>Создать пакет развертывания</strong>.
2. В диалоговом окне **Создание пакета развертывания** выберите механизм TMSEngines и введите путь, по которому необходимо сохранить файлы пакета. 

   [![Выбор модели TMSEngines.](./media/071.png)](./media/071.png)

3. Теперь пакет можно развернуть в целевой среде. Cм. руководство в разделе [Установка готового к развертыванию пакета](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Настройка механизма TMS в Supply Chain Management

В этом разделе объясняется, как настроить Supply Chain Management для использования механизма TMS, и показано, как новый созданный вами механизм используется в подборе ставок. В примере в этом разделе используется компания с в демонстрационными данными USMF.

1. Создайте новый механизм, как описано в разделе "Создание нового механизма TMS".
2. Постройте решение.
3. Скопируйте полученную сборку в расположение двоичных объектов сервера Supply Chain Management, \[AOSWebRoot\]bin. **Примечание.** Этот шаг относится только к среде разработки. В рабочей среде следует развернуть с помощью пакета развертывания. Инструкции см. в предыдущем разделе, "Развертывание механизма TMS в качестве пакета".
4. В Supply Chain Management на странице **Механизмы ставок** создайте новый механизм ставок. Механизм должен указывать на сборку механизма, созданную при построении библиотеки классов механизма и реализуемого класса механизма. 

   [![Создание нового механизма ставок на странице механизмов ставок.](./media/081.png)](./media/081.png)

5. Создайте перевозчика, использующего механизм ставок из примера. Поскольку наш механизм не использует никаких данных, нет необходимости назначать справочник ставок. 

   [![Создание нового перевозчика.](./media/092.png)](./media/092.png)

6. На странице **Рабочее место маршрута ставки** щелкните **Магазин ставок**. Вы увидите ставку 100,00 от SampleCarrier, как показано на следующем снимке экрана. В этом примере мы подбираем ставки для маршрута со склада 24 до клиента US-004. Однако, поскольку ставка жестко запрограммирована, всегда будет отображаться ставка 100,00.

   [![Рабочее место маршрута ставки.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Советы и рекомендации

- Если вы используете средства разработки для Supply Chain Management, полезно добавить в решение новый проект. Если этот проект настроен как проект на запуске и начнете сеанс отладки, можно выполнить отладку X++ и кода C\# в одном и том же сеансе отладки.
- Каждый раз при изменении и повторной компиляции проекта ThirdPartyTMSEngines необходимо вручную скопировать результирующую сборку в папку двоичных объектов или развернуть ее с помощью пакета развертывания. В противном случае вы можете работать, используя устаревшую сборку.
- После выполнения операций TMS в Supply Chain Management рабочий процесс Internet Information Services (IIS) может заблокировать сборку ThirdPartyTMSEngines, чтобы обновление сборки было невозможно. В этом случае перезапустите процесс w3svc.

### <a name="whitepaper"></a>Технический документ

Для получения дополнительных сведений загрузите следующий технический документ (написан для поддержки AX2012, но по-прежнему применим к Dynamics 365 Supply Chain Management)

- [Внедрение и развертывание механизмов управления транспортировкой](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]