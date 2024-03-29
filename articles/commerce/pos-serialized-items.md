---
title: Работа с сериализованными номенклатурами в POS
description: В этой статье объясняется, как управлять сериализованными номенклатурами в приложении POS.
author: boycezhu
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 8a715a9d025f36656506daeb9e611bfacdafa102
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880037"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Работа с сериализованными номенклатурами в POS

[!include [banner](includes/banner.md)]

Многие розничные компании продают продукцию, требующую контроля серийного номера. Такие продукты называются *сериализованными номенклатурами*. У некоторых розничных продавцов может возникнуть необходимость в поддержке серийных номеров в магазине или складских запасах для целей отслеживания. Другие розничные предприятия могут получать серийные номера в процессе продаж (для целей обслуживания и гарантии). В этой статье объясняется, как управлять сериализованными номенклатурами в приложении Microsoft Dynamics 365 Commerce POS.

## <a name="serial-number-configurations"></a>Конфигурации серийных номеров

Номенклатура считается сериализованной, если ей назначается группа аналитик отслеживания, которая настроена на разрешение серийных номеров. В Commerce Headquarters на странице **Группы аналитик отслеживания** выберите параметр **Активно**, чтобы включить серийные номера для процесса запасов, или выберите параметр **Активно в процессе продаж**, чтобы включить серийные номера для процесса продаж.

На экспресс-вкладке **Аналитики отслеживания** включите параметр **Пропуск для приходов**, чтобы разрешить, чтобы серийный номер являлся необязательным вводимым значением в процессе приемки запасов сериализованных номенклатур. Если этот параметр отключен, необходимо обязательно вводить серийный номер. Аналогичным образом параметр **Пропуск для расходов** определяет, является ли обязательным серийный номер в процессе отгрузки запасов.

> [!NOTE]
> Чтобы использовать POS-операции **Входящие запасы** и **Исходящие запасы** для регистрации или подтверждения серийных номеров для сериализованной номенклатуры, необходимо настроить, чтобы этой номенклатуре была назначена группа аналитик отслеживания, которая настроена на разрешение серийных номеров для параметра **Активно**, а не для параметра **Активно в процессе продаж**.

## <a name="serial-number-management-page"></a>Страница управления серийными номерами

В POS-операциях **Входящие запасы** и **Исходящие запасы**, если выбранная, полученная или отгруженная номенклатура является сериализованной номенклатурой, область **Сведения** содержит параметр **Управление серийным номером**, который связывается со страницей **Управления серийными номерами**, на которой можно регистрировать или проверять серийные номера для номенклатуры. Кроме того, можно открыть страницу **Управление серийными номерами**, выбрав действие **Серийный номер** на панели приложения в представлении сведений о заказе или выбрав параметр **Управление серийным номером** в диалоговом окне, которое появляется в процессе приемки или отгрузки. 

На странице **Управление серийными номерами** перечислены все открытые строки серийных номеров, которые находятся в процессе регистрации или проверки. На этой странице могут быть две вкладки: одна для текущей номенклатуры и другая для всех сериализованных номенклатур в заказе.

В поле **Статус** на странице **Управление серийными номерами** представлены сведения о текущем этапе каждого серийного номера:

- **Не зарегистрировано** — серийный номер не был указан или зарегистрированный серийный номер еще не был проверен (в процессе приема).
- **Регистрация** — серийный номер был зарегистрирован и сохранен локально в базе данных канала магазина, либо предварительно зарегистрированный серийный номер был проверен. Только серийные номера со статусом " **Регистрация** будут отправлены в центральный офис Commerce после завершения приемки или выполнения.

## <a name="receive-serialized-items"></a>Получение сериализованных номенклатур

POS-операция **Входящие запасы** позволяет пользователям выполнять следующие задачи для сериализованных номенклатур:

- Регистрация серийных номеров для сериализованных номенклатур, которые поступают на склад по заказу на покупку.
- Проверкка предварительно зарегистрированных серийных номеров для сериализованных номенклатур, которые поступают на склад по заказу на покупку или заказу на перемещение.

### <a name="register-serial-numbers-against-serialized-items"></a>Регистрация серийных номеров для сериализованных номенклатур

Для заказа на покупку вам будет открыто диалоговое окно с параметром **Управление серийным номером** в процессе приемки сериализованной номенклатуры. Можно выбрать этот параметр, чтобы открыть страницу **Управление серийным номером** и начать регистрацию серийных номеров. Можно также пропустить этот шаг в процессе приемки и ввести номер позже, до разноски прихода.

По умолчанию отображается вкладка для текущей номенклатуры. Все строки серийных номеров имеют пустое значение серийного номера и статус **Не зарегистрировано**. Можно просканировать штрихкоды серийных номеров или выбрать **Серийный номер** на панели приложений, чтобы сразу ввести серийные номера. Введенные серийные номера появятся в списке, и из статус изменится на **Регистрация**. Максимальное число серийных номеров, которое можно зарегистрировать в списке, равно принимаемому количеству. Если допущена ошибка, можно выбрать **Изменить** или **Очистить** в **Сведения** для внесения изменений в введенные серийные номера.

Серийные номера можно также регистрировать на вкладке **Все сериализованные номенклатуры** на странице **Управление серийными номерами**. В списке выберите номенклатуру, для которой необходимо зарегистрировать серийные номера.

### <a name="validate-serial-numbers-on-serialized-items"></a>Проверка серийных номеров в сериализованных номенклатурах

Для заказа на перемещение исходящая сторона должна выполнить предварительную регистрацию серийных номеров для сериализованных номенклатур в процессе отгрузки. Для заказа на покупку поставщик может предоставлять информацию о серийном номере через уведомление о предварительной отгрузке (ASN), и можно предварительно зарегистрировать номера номенклатур, которые будут отгружены. В обоих случаях серийные номера известны до получения товара. Поэтому на принимающей стороне необходимо только подтвердить получение того, что вы предполагали получать.

Чтобы выполнить проверку серийных номеров, можно открыть страницу **Управление серийными номерами** во время приемки или в любое время до разноски прихода. Для каждой сериализованной номенклатуры с предварительно зарегистрированными серийными номерами все серийные номера автоматически устанавливаются в начальный статус **Не зарегистрировано** на этой странице. Для проверки серийных номеров их можно отсканировать или ввести. При вводе серийного номера приложение проверяет, соответствуют ли они предварительно зарегистрированным серийным номерам. Если они совпадают, статус изменится на **Регистрация**. В противном случае вы получаете сообщение об ошибке. Альтернативно можно непосредственно выбрать серийный номер, затем выберите параметр **Проверить серийный номер** в области **Сведения**, чтобы быстро пометить этот серийный номер как проверенный. Максимальное число серийных номеров, которое можно проверить в списке, равно принимаемому количеству.

Серийные номера можно также проверять на вкладке **Все сериализованные номенклатуры** на странице **Управление серийными номерами**. В списке выберите номенклатуру, для которой необходимо проверить серийные номера.

## <a name="ship-serialized-items"></a>Отгрузка серийных номенклатур

Можно использовать POS-операцию **Исходящие запасы** для регистрации серийных номеров по сериализованным номенклатурам при отгрузке их из текущего магазина с помощью заказа на перемещение.

### <a name="register-serial-numbers-against-serialized-items"></a>Регистрация серийных номеров для сериализованных номенклатур

Для заказа на перемещение вам будет открыто диалоговое окно с параметром **Управление серийным номером** в процессе отгрузки сериализованной номенклатуры. Можно выбрать параметр, чтобы открыть страницу **Управление серийным номером** и начать регистрацию серийных номеров. Можно также пропустить этот шаг в процессе отгрузки и ввести номер позже, до разноски отгрузки.

По умолчанию отображается вкладка для текущей номенклатуры. Все строки серийных номеров имеют пустое значение серийного номера и статус **Не зарегистрировано**. Можно просканировать штрихкоды серийных номеров или выбрать **Серийный номер** на панели приложений, чтобы сразу ввести серийные номера. Введенные серийные номера появятся в списке, и из статус изменится на **Регистрация**. Максимальное число серийных номеров, которое можно зарегистрировать в списке, равно отгружаемому количеству. Если допущена ошибка, можно выбрать **Изменить** или **Очистить** в **Сведения** для внесения изменений в введенные серийные номера.

Серийные номера можно также регистрировать на вкладке **Все сериализованные номенклатуры** на странице **Управление серийными номерами**. В списке выберите номенклатуру, для которой необходимо зарегистрировать серийные номера.

Можно также включить проверку наличия серийного номера во время регистрации серийного номера для исходящего заказа на перемещение. При такой проверке при попытке отгрузки серийного номера, недоступного в запасах магазина отгрузки, вы получите сообщение об ошибке у потребуется ввести другой номер.

Чтобы включить такую проверку, необходимо предварительно запланировать следующие задания для запуска на повторяющейся основе:

- **Retail и Commerce** > **ИТ Retail и Commerce** > **Продукты и запасы** > **Доступность продукта**
- **Retail и Commerce** > **Графики распределения** > **1130** (**Доступность продукта**)

## <a name="sell-serialized-items-in-pos"></a>Продажа сериализованных номенклатур в POS

В то время как приложение торгового терминала POS всегда поддерживает продажу сериализованных номенклатур в Commerce версии 10.0.17 и более поздних, организации могут включить функции, улучшающие бизнес-логику, которая запускается при продаже продуктов, настроенных для отслеживания серийных номеров.

Когда функция **Улучшенная проверка серийных номеров в модуле запись и выполнения заказов на POS-терминале** включена, при продаже продуктов с серийными номерами в POS оцениваются следующие конфигурации продуктов:

- Настройка **Серийный тип** для продукта (**активна** или **активна при продаже**).
- Параметры **Допускается пустой выпуск** для продукта.
- Параметры **Физический отрицательный запас** для продукта и/или склада продажи.

### <a name="active-serial-configurations"></a>Активные серийные конфигурации

При продаже номенклатуры в POS-терминале, настроенном с использованием аналитики отслеживания серийных номеров **Активно**, POS-терминал выполняет логику проверки, которая не позволяет пользователям завершить продажу сериализованной номенклатуры с серийным номером, который не может быть найден в текущих запасах склада продаж. Имеется два исключения из этого правила проверки:

- Если для номенклатуры также задано **Допускается пустой выпуск**, пользователи могут пропустить ввод серийного номера и продать номенклатуру без указания серийного номера.
- Если номенклатура и/или склад продажи настроен с включенным параметром **Физический отрицательный запас**, приложение принимает и продает серийный номер, который не может быть подтвержден в запасах на складе, с которого выполняется продажа. Эта конфигурация позволяет получить отрицательный запас складской проводки для данной номенклатуры или серийного номера, поэтому система будет разрешать продажи неизвестных серийных номеров.

> [!IMPORTANT]
> Чтобы приложение POS-терминала могло правильно проверять, находятся ли продаваемые серийные номера для номенклатуры серийного типа **Активно** в запасах на складе продажи, необходимо, чтобы организации часто выполняли задание **Доступность продукта с аналитикой отслеживания** в Commerce headquarters и сопутствующую задачу распределения наличия продукта **1130** в Commerce headquarters. По мере того как новые сериализованные запасы поступают на склады продаж, для того чтобы POS-терминал проверял доступность продаваемых серийных номеров в запасах, шаблон запасов должен часто обновлять базу данных канала с самыми последними данными о доступности запасов. Задание **Доступность продуктов с аналитикой отслеживания** делает текущий снимок основных запасов, включая серийные номера, для всех складов компании. Задание по распределению **1130** делает моментальный снимок запасов и использует его совместно со всеми настроенными базами данных каналов.

### <a name="active-in-sales-process-serial-configurations"></a>Активно в конфигурациях с серийными номерами в процессе продаж

Номенклатуры, для которых настроена аналитика серийных номера как **Активная в процессе продаж**, не проходят через какую-либо логику проверки запасов, поскольку в этой конфигурации предполагается, что серийные номера запасов предварительно не зарегистрированы в запасах, а серийные номера фиксируются только во время продажи.  

Если таже настроен параметр **Допускается пустой выпуск** для номенклатуры, для которой настроено **Активная в процессе продаж**, запись серийного номера может быть пропущена. Если параметр **Допускается пустой выпуск** не настроен, приложение требует, чтобы пользователь ввел серийный номер, даже если он не будет проверяться на наличие доступных запасов.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Применение серийных номеров в процессе создания проводок POS-терминала

Приложение POS-терминала сразу запрашивает у пользователей сбор серийных номеров при продаже сериализованной номенклатуры, но приложение позволяет пользователям пропускать ввод серийных номеров до определенного момента процесса продажи. Когда пользователь начинает запись платежа, приложение принудительно требует ввода серийного номера для всех номенклатур, которые не настроены для выполнения через будущие отгрузки или получения. Все сериализованные номенклатуры, настроенные для кассовых проводок или выполнения на вынос, требуют от пользователя фиксации серийного номера (или согласиться оставлять его пустым, если в конфигурации номенклатуры это разрешено) перед завершением продажи.

Для номенклатур с серийными номерами, проданных для будущего получения или отгрузки, пользователи POS-терминалов могут пропускать ввод серийного номера изначально и тем самым завершать создание заказа клиентом.   

> [!NOTE]
> При продаже или выполнении продажи продуктов с серийными номерами через приложение POS-терминала для номенклатур с серийными номерами в проводке по продажам применяется количество "1". Это результат того, как отслеживается информация о серийном номере в строке продаж. При продаже или выполнении проводки для нескольких номенклатур с серийными номерами через POS-терминал каждая строка продажи должна быть настроена только с количеством "1". 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Применение серийных номеров в процессе выполнения или получения заказа клиента

При выполнении строк заказа клиента для продуктов с серийными номерами с использованием операции **Выполнение заказа** в POS-терминале POS-терминал обеспечивает запись серийного номера до окончательного выполнения. Следовательно, если серийный номер не был введен во время первоначальной регистрации заказа, он должен быть записан во время процесса комплектации, упаковки или отгрузки в POS-терминале. Проверка выполняется на каждом шаге, и пользователь получит запрос данных серийного номера только в том случае, если они отсутствуют или недействительны. Например, если пользователь пропускает этапы комплектации или упаковки и сразу же инициировал отгрузку, а серийный номер не был зарегистрирован для данной строки, POS-терминал потребует ввода серийного номера перед завершением окончательного шага выставления накладной. При принудительной записи серийного номера во время выполнения операций выполнения заказа в POS-терминале все правила, упомянутые ранее в этой статье, действуют по-прежнему. Только сериализованные номенклатуры, настроенные как **Активные**, проходят проверку запасов по серийному номеру. Номенклатуры, настроенные как **Активные в процессе продаж**, не проверяются. Если разрешены **Физические отрицательные запасы** для продуктов со значением **Активно**, все серийные номера будут приниматься, независимо от наличия запасов. Для номенклатур **Активно** и **Активно в процессе продаж**, если настроен параметр **Разрешены пустые выпуски**, пользователь может оставлять серийные номера пустыми, если это необходимо на этапе комплектации, упаковки и отгрузки.

Проверки серийных номеров также будут выполняться, когда пользователь выполняет операции получения заказов клиентов в POS-терминале. Приложение POS-терминала не допускает завершения получения по продукту с серийным номером, если он не прошел проверки, как упоминалось ранее. Проверки всегда основываются на аналитике отслеживания продукта и конфигурациях склада продажи. 

## <a name="additional-resources"></a>Дополнительные ресурсы

[Входящая операция запасов в POS](./pos-inbound-inventory-operation.md)

[Исходящая операция запасов в POS](./pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]