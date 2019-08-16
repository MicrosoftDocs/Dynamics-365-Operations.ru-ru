---
title: Доступ к метаданным приложения с помощью подключенных приложений
description: В этом разделе описывается, как пользователь службы Regulatory Configuration Service (RCS) может создать новое сопоставление модели электронной отчетности (ER) с помощью метаданных в Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d3581f6ae2d91b9648da3ba69e6b1d36cd08196
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727060"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Доступ к метаданным приложения с помощью подключенных приложений

[!include [task guide banner](../../includes/task-guide-banner.md)]

В следующих шагах поясняется, как пользователь службы Regulatory Configuration Service (RCS) с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новое сопоставление модели электронной отчетности с помощью метаданных в Dynamics 365 for Finance and Operations. Доступ к метаданным приложения производится в сети с помощью подключенного приложения RCS. Образец сопоставления модели ER будет настроен для доступа к проводкам внешней торговли. Для выполнения этих шагов в RCS необходимо сначала выполнить шаги в теме [Создание поставщика конфигурации и установка его в качестве активного](er-configuration-provider-mark-it-active-2016-11.md). Если вы не выполнили шаги в теме [Доступ к метаданным приложения с помощью конфигурации электронной отчетности](access-application-metadata-er-configuration.md), перейдите на [страницу примеров электронной отчетности](https://go.microsoft.com/fwlink/?linkid=862266), чтобы загрузить и сохранить следующие конфигурации электронной отчетности: Метаданные внешней торговли.xml; Модель внешней торговли.xml; Сопоставление внешней торговли.xml, а затем выполните шаги из процедуры.

## <a name="prerequisites"></a>Необходимые условия
1. Перейдите в раздел **Все рабочие области** > **Электронная отчетность**. 
2. Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**. Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщика конфигурации и пометка его как активного](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="get-required-er-configurations"></a>Получение необходимых конфигураций электронной отчетности
1. Щелкните **Конфигурации отчетности**. 
2. Если вы уже выполнили шаги из процедуры [(RCS) Доступ к метаданным приложения с помощью конфигурации электронной отчетности](access-application-metadata-er-configuration.md), у вас уже имеются все необходимые конфигурации ER (конфигурации метаданных, моделей и сопоставлений внешней торговли) в текущем экземпляре RCS. Все остальные шаги в этой подзадаче можно пропустить. 
3. Щелкните **Обменять**. 
4. Щелкните **Загрузить из XML-файла**. 
5. Щелкните **Обзор** и выберите файл **Метаданные внешней торговли.xml**. 
6. Щелкните **OK**. 
7. Щелкните **Обменять**. 
8. Щелкните **Загрузить из XML-файла**. 
9. Щелкните **Обзор** и выберите файл **Модель внешней торговли.xml**. 
10. Щелкните **OK**. 
11. Щелкните **Обменять**. 
12. Щелкните **Загрузить из XML-файла**. 
13. Щелкните **Обзор** и выберите файл **Сопоставление внешней торговли.xml**. 
14. Щелкните **OK**. 

## <a name="register-connected-dynamics-365-for-finance-and-operations-application"></a>Регистрация подключенного приложения Dynamics 365 for Finance and Operations
1. Закройте страницу. 
2. Закройте страницу. 
3. Перейдите в раздел **Все рабочие области** > **Электронная отчетность**. 
4. Щелкните **Подключенные приложения**. 
5. Убедитесь, что настроенное приложение основано на Azura, и что оно доступно для текущего пользователя RCS. Также необходимо, чтобы текущий пользователь RCS имел доступ к выбранному приложению и был зарегистрирован в качестве пользователя данного приложения в роли, которая дает ему право доступа к метаданным приложения. 
6. Нажмите кнопку **Создать**. 
7. В поле **Имя** введите "MyConnectedApp". 
8. В поле **Приложение** введите "https://mycompany.operations.dynamics.com'. 
9. В поле **Клиент** введите "mycompany.onmicrosoft.com". 
10. Нажмите кнопку **Сохранить**. 
11. При проверке подключения к настроенному приложению на странице **Подключение к удаленному приложению** щелкните **Щелкните здесь, чтобы подключиться к выбранному удаленному приложению**. 
12. Щелкните **Проверить подключение**. 
13. Нажмите кнопку **Закрыть**. 
14. После успешной проверки подключения сведения о версии и клиенте будут обновлены для настроенного приложения в текущей сетке. 

## <a name="review-existing-model-mapping-configuration"></a>Проверка существующей конфигурации сопоставлений модели
1. Закройте страницу. 
2. Щелкните **Конфигурации отчетности**. 
3. В дереве разверните узел **Модель внешней торговли**. 
4. В дереве выберите **Модель внешней торговли\Сопоставление внешней торговли**. 
5. Разверните раздел **Необходимые условия**. 

> [!NOTE]
> В настоящее время это сопоставление ссылается на конфигурацию метаданных. Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей. 

6. Выберите **Конструктор**. 
7. Выберите **Конструктор**. 
8. В дереве выберите узел **Dynamics 365 for Operations\Записи таблиц**. 
9. Щелкните **Добавить корень**. 
10. В поле **Таблица** введите или выберите значение. 

> [!NOTE]
> В настоящее время это сопоставление ссылается на конфигурацию метаданных. Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей. 

11. Щелкните **Отмена**. 
12. Закройте страницу. 
13. Закройте страницу. 

## <a name="assign-connected-application-to-model-mapping"></a>Назначение подключенного приложения сопоставлению модели 
1. Выберите **Изменить**. 
2. Выберите приложение **MyConnectedApp**. 

> [!NOTE]
> В настоящее время это сопоставление ссылается на метаданные выбранного подключенного приложения. Если это же сопоставление ссылается одновременно на конфигурацию метаданных и подключенное приложение, будут использоваться метаданные подключенного приложения. 

3. Выберите **Конструктор**. 
4. Выберите **Конструктор**. 
5. В дереве выберите узел **Dynamics 365 for Operations\Записи таблиц**. 
6. Щелкните **Добавить корень**. 
7. В поле **Таблица** введите или выберите значение. 

> [!NOTE]
> Теперь предлагается более двух таблиц приложений, поскольку в этом сопоставлении используются все метаданные подключенного приложения, которое было назначено для него. 

8. Щелкните **Отмена**. 
9. Щелкните **Проверить**. 

> [!NOTE]
> Мы успешно привязали элементы модели данных к элементам источников данных, которые описаны с помощью подробных сведений метаданных подключенного приложения, которое было назначено для этого сопоставления. 

10. Закройте страницу. 
11. Закройте страницу. 

Когда необходимо оценить сопоставление модели с помощью метаданных другой версии приложения, зарегистрируйте другое подключенное приложение, назначьте его этому сопоставлению модели и проверьте его по новым метаданным.