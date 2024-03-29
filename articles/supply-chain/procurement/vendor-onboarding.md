---
title: Адаптация поставщиков
description: В этой статье описан процесс адаптации новых поставщиков. В нем описываются действия, которые требуются для различных ролей во время этого процесса.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, SysUserRequestListPage, VendRequestListPage, VendRequestCompanyProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8b3660e1c7a0e236456d1a16c628fd5d538f045f
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111376"
---
# <a name="onboard-vendors"></a>Адаптация поставщиков

[!include [banner](../includes/banner.md)]

---

Новые поставщики могут быть адаптированы и зарегистрированы в Microsoft Dynamics 365 Supply Chain Management на основе сведений, полученных от человека, который представляет поставщика.

Этот процесс состоит из следующих этапов, где различные роли выполняют действия в системе.

1. **Управление данными OData** — Импорт объекта — Начальным запросом будет запрос регистрации потенциального поставщика. Как правило этот запрос поступает из источника, например с размещенного у клиента веб-сайта, который разрешает анонимный доступ. Поставщики могут зарегистрироваться, предоставляя базовые сведения, такие как имя поставщика, обоснование, номер организации и имя и адрес электронной почты контактного лица. Запросы импортируются через интерфейс управления данными.
2. **Страница списка запросов регистрации потенциальных поставщиков** — на основе сведений, входящем в запрос регистрации потенциального поставщика, специалист по закупкам решает, следует ли зарегистрировать поставщика. Специалист по закупкам просматривает входящие запросы на странице списка **Запросы регистрации потенциальных поставщиков**.
3. **Workflow-процесс подготовки пользователей** — когда специалист по закупкам проверил информацию из входящего запроса и принял решение продолжить процесс регистрации, workflow-процесс запроса пользователя подготавливает нового пользователя и отправляет электронное приглашение, чтобы принять контактное лицо в качестве проверенного пользователя Microsoft Dynamics 365.
4. **Мастер регистрации поставщика** — контактное лицо поставщика производит вход с использованием новой учетной записи пользователя. Он выполняет мастер регистрации поставщика для предоставления сведений, таких как адреса, бизнес-информация, категории закупаемой продукции и ответы на анкету.
5. **Workflow-процесс утверждения** — создается запрос поставщика, который включает сведения о регистрации. Этот запрос поставщика направляется в workflow-процесс и передается на проверку и утверждение.
6. **Создание шаблона поставщика и изменение роли пользователя** — когда запрос поставщика утвержден, создается запись поставщика. Учетная запись пользователя контактного лица поставщика получает разрешение на совместную работу с поставщиком или отключается.

Следующая таблица показывает действия и роли, которые участвуют в процессе.

| Роль и "процесс"       | Управление данными OData — импорт объектов | Страница списка запросов на регистрацию потенциальных поставщиков | Workflow-процесс подготовки пользователя | Мастер регистрации поставщика | Утверждение документооборота | Создание шаблона поставщика и изменение роли пользователя |
|--------------------------|---|---|---|---|---|---|
| System                   | Запрос на нового поставщика импортируется. | | | | | После принятия запроса поставщика создается запись поставщика. |
| Специалист по закупкам | | Запускает процесс адаптации. | | | Просмотр и либо принятие, либо отклонение запроса поставщика. | |
| Администратор            | | | Создайте пользователя в Supply Chain Management и в Microsoft Azure. | | | |
| Контактное лицо поставщика    | | | Отправка электронной почты контактному лицу. | Регистрация сведений о поставщике. | | |

Для быстрой демонстрации процесса адаптации поставщика просмотрите это короткое видео на YouTube о том, [Как адаптировать нового поставщика в приложениях для управления финансами и операциями](https://www.youtube.com/watch?v=0KUc3AGaTKk).

## <a name="importing-the-prospective-vendor-registration-request"></a>Импорт запроса на регистрацию потенциального поставщика

Запрос регистрации потенциального поставщика является объектом в Supply Chain Management. Можно настроить систему для импорта данных через этот объект. 

В следующей таблице показаны сведения, которые содержит этот объект, и которые могут быть импортированы.

| Поле                        | описание |
|------------------------------|-------------|
| Наименование Поставщика                  | Название поставщика. |
| Деловое обоснование       | Причина или причины запроса поставщика. |
| Номер организации          | Официально известный регистрационный номер. |
| Отрасль             | Отрасль, в которой работает поставщик. |
| Имя контактного лица  | Имя лица, которому будет предложено зарегистрировать сведения о поставщике. |
| Отчество контактного лица | Отчество лица, которому будет предложено зарегистрировать сведения о поставщике. |
| Фамилия контактного лица   | Фамилия лица, которому будет предложено зарегистрировать сведения о поставщике. |
| Адрес электронной почты контактного лица       | Адрес электронной почты, который будет использоваться для создания нового пользователя в Supply Chain Management, и который будет регистрироваться в учетной записи клиента Azure Active Directory (Azure AD). |
| Дата отправки               | Дата создания запроса во внешней системе. |
| Информация о компании                 | Юридическое лицо, для которого поставщик хочет стать поставщиком. Это значение должно быть кодом юридического лица, который был зарегистрирован в Supply Chain Management. Если значение не было получено в процессе импорта, применяется значение из параметров закупки и источников. |
| Вид поставщика                  | Поставщик может быть либо организацией, либо физическим лицом. Тип поставщика определяет конечный способ создания поставщика. |

После импорта запрос регистрации потенциального поставщика он появляется на странице списка **Запрос регистрации потенциального поставщика**. С этой страницы списка специалист по закупкам может пригласить пользователя. Запрос пользователя для подготовки пользователя отправляется в workflow-процесс.

## <a name="submitting-a-prospective-vendor-user-request"></a>Отправка запроса пользователя потенциального поставщика

Цель запроса пользователя потенциального поставщика — подготовка человека, который отправил начальный запрос, чтобы он мог войти в Supply Chain Management с использованием учетной записи электронной почты, представленной в запросе регистрации потенциального поставщика.

Запроса пользователя потенциального поставщика обрабатывается workflow-процессом запроса пользователя. Этот workflow-процесс обменивается данными через сотрудничество Azure AD B2B. Он создает пользователя в Supply Chain Management, который имеет соответствующие параметры безопасности.

Новые пользователи, которые настраиваются, имеют следующие роли безопасности:

- Внешний пользователь системы
- Потенциальный поставщик (внешний)

Новый пользователь будет получать сообщения электронной почты, которые создаются workflow-процессом запроса пользователя. Это сообщение электронной почты приглашает пользователя для входа в систему.

Дополнительные сведения о конфигурации электронной почты и workflow-процессе в целом см. в описании workflow-процесса запроса пользователя в разделе [Настройка и ведение сотрудничества с поставщиками](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Регистрация поставщика

Пользователь потенциального поставщика, который выполнит вход в Supply Chain Management, увидит первую страницу мастера регистрации поставщика, на которой он может ввести сведения о поставщике.

Мастер отражает конфигурацию запроса поставщика. Страна или регион, где работает поставщик, определяет, какая информация запрашивается в мастере и какая информация является обязательной.

Дополнительные сведения о конфигурации запроса поставщика см. в разделе [Настройка и ведение сотрудничества с поставщиками](set-up-maintain-vendor-collaboration.md). В следующей таблице содержится обзор страниц мастера и назначение каждой страницы.

| Страница                       | описание |
|----------------------------|-------------|
| Страна/регион             | Страна или регион определяют конфигурацию запроса поставщика, которая применяется на оставшихся страницах мастера. Они также определяют значения в поле подстановки **Состояние налога**. |
| Условия       | Эта страница может быть доступна в зависимости от конфигурации запроса поставщика. Если она доступна, пользователь должен принять условия для продолжения. |
| Информация о поставщике         | Эта страница содержит название поставщика, которое вводится автоматически из исходного запроса регистрации потенциального поставщика. Она также содержит номер организации, телефонный номер поставщика, номер факса и адрес электронной почты, а также адреса поставщика для различных целей. |
| Информация о контактном лице | Эта страница содержит имя контактного лица, которое вводится автоматически из исходного запроса регистрации потенциального поставщика. Она также содержит номер телефона и адрес электронной почты контактного лица, а также адреса контактного лица для различных целей. |
| Бизнес-информация       | На этой странице содержатся налоговые регистрационные номера (для различных стран или регионов) и количества сотрудников. Она также указывает, принадлежит ли бизнес представителям меньшинств. |
| Категории закупаемой продукции     | Эта страница содержит категории закупаемой продукции, на которые запросил утверждение поставщик. Пользователь может выбирать категории в иерархии категорий закупаемой продукции. Можно настроить число уровней, отображаемых в иерархии, в пункте **Параметры модуля "Закупки и источники"** &gt; **Совместная работа с поставщиками** раздела **Закупки и источники** &gt; **Настройка**. |
| Анкеты             | Мастер может включать набор анкет для поставщика. Анкеты, которые отображаются в мастере, настраиваются либо для запроса поставщика, либо по категориям закупаемой продукции. Если анкеты настраиваются по категории закупаемой продукции, категории закупаемой продукции, для которых поставщик запросил утверждение, определяют анкеты, которые отображаются в мастере. На странице **Категории закупаемой продукции** можно добавить анкету для соответствующей категории и задать тип действия **Адаптация поставщика**. |

Когда пользователь потенциального поставщика завершает заполнение мастера регистрации поставщика, создается запрос поставщика.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Отправка запроса поставщика вручную или автоматически

Запрос поставщика может быть создан как черновик и вручную отправлен в workflow-процесс. Кроме того, запрос поставщика может быть автоматически отправлен в workflow-процесс после завершения работы мастера регистрации поставщика. Запрос можно отправить вручную, если, например, специалист по закупкам хочет оценить, требуется ли отправить запрос в процесс утверждения до его отправки в workflow-процесс.

- Выберите **Параметры модуля "Закупки и источники"** &gt; **Совместная работа с поставщиками**, затем выберите **Автоматическая отправка регистрации потенциального поставщика в workflow-процесс** для настройки запроса поставщика таким образом, чтобы он отправлялся автоматически в workflow-процесс после завершения мастера регистрации поставщика.

## <a name="vendor-requests"></a>Запросы поставщиков

Запросы поставщиков доступны на странице **Запросы пользователей совместной работы с поставщиками**.

Запрос поставщика содержит сведения, введенные пользователем потенциального поставщика в мастере регистрации поставщика.

Этот запрос позволяет просмотреть сведения о поставщике и решить, должен ли поставщик стать зарегистрированным поставщиком.

Запрос поставщика должен быть отправлен в workflow-процесс, и он должен быть перенаправлен соответствующим проверяющим и утверждающим. Базовые сведения о настройке workflow-процессов см. в разделе [Workflow-процессы модуля "Закупки и источники"](procurement-sourcing-workflows.md).

В следующей таблице показаны статусы, которые запросы поставщиков могут иметь.

| Состояние                     | описание |
|----------------------------|-------------|
| Черновой                      | Запрос поставщика еще не был отправлен. |
| Запрос отправлен          | Запрос поставщика отправлен, и обрабатывается первый шаг в workflow-процессе. |
| Ожидает рассмотрения             | Если имеются несколько проверяющих в задаче workflow-процесса, проверяющий может принять задачу проверки запроса поставщика, а затем завершить проверку. Если имеется только один проверяющий, этот участник может завершить проверку, выбрав **Завершено** в действии workflow-процесса. Им не требуется сначала принять рабочий элемент. |
| Запрос ожидает утверждения   | Запрос поставщика был направлен участникам для утверждения, и имеется возможность запросить дополнительные сведения. Запрос для получения дополнительных сведений приводит к тому, что рабочий элемент будет направлен назад отправителю. Запрос поставщика может также быть утвержден или отклонен, когда он находится в этом состоянии. |
| Запрос изменения заявления | Дополнительные сведения были запрошены утверждающим лицом, и запрос поставщика был направлен пользователю, который отправил запрос поставщика. Отправитель может добавить необходимые сведения, а затем заново отправить запрос поставщика. Если запрос поставщика направляется повторно, статус изменяется обратно на **Запрос ожидает утверждения**. |
| Запрос утвержден           | Это состояние является окончательным. |
| Запрос отклонен           | Это состояние является окончательным. |

## <a name="approving-a-vendor-request"></a>Утверждение запроса поставщика

Если запрос поставщика утвержден, создается учетная запись поставщика и статус **Утвержден** отображается как в первоначальном запросе регистрации потенциального поставщика, так и в запросе поставщика.

Прежде чем утвердить запрос поставщика, на странице **Новый поставщик** на экспресс-вкладке **Общие сведения** выберите пункт **Группа поставщиков** для выбора группы поставщиков.

Если пользователь потенциального поставщика должен иметь доступ к Supply Chain Management как пользователь совместной работы с поставщиками, который представляет поставщика, задайте для разрешения доступа к совместной работе с поставщиками значение **Да**. Чтобы отключить учетную запись пользователя, которую потенциальный поставщик использовал для регистрации, присвойте этому разрешению значение **Нет**.

Если разрешение на доступ к совместной работе с поставщиками имеет значение **Да**, когда запрос поставщика утверждается, запрос отправляется для изменения ролей пользователя так, чтобы пользователь имел роли, которые определены для типа **Поставщик** в **Внешние роли**. Если это разрешение имеет значение **Нет**, когда запрос поставщика утверждается, запрос отправляется для отключения пользователя. В этом случае должен быть настроен workflow-процесс, чтобы деактивировать запрос пользователя.

Для создания учетной записи поставщика при утверждении запроса поставщика для номерной серии для создания поставщиков из запросов поставщиков должно быть задано значение **Авто**.

Обзор разрешений на доступ пользователя совместной работы с поставщиками см. в разделе [Настройка и ведение сотрудничества с поставщиками](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Отклонение запроса поставщика

Если запрос поставщика отклонен, причина отклонения должна быть выбрана в запросе поставщика.

При отклонении запроса поставщика отправляется запрос на отключение пользователя. В этом случае должен быть настроен workflow-процесс, чтобы деактивировать запрос пользователя. Дополнительные сведения см. в разделе [Настройка и ведение сотрудничества с поставщиками](set-up-maintain-vendor-collaboration.md).

Если запрос поставщика отклонен, статус **Отклонен** отображается как в первоначальном запросе регистрации потенциального поставщика, так и в запросе поставщика.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Удаление запроса регистрации потенциального поставщика в различных статусах

Различные статусы запроса регистрации потенциального поставщика дают общее представление о состоянии запроса.

С помощью действия **Удалить** для запроса регистрации потенциального поставщика можно очистить и удалить цепочку записей, которые были созданы, и можно отключить учетную запись пользователя. Результат действия **Удалить** зависит от статуса запроса на регистрацию потенциального поставщика, как показано в следующей таблице.


|          Состояние          |                                                                                     Описание статуса                                                                                      |                                                                                                                                                            Результат выполнения действия удаления                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Новое            |                                                                         Никакие действия не были сделаны с запросом.                                                                          |                                                                                                                                              Запрос на регистрацию потенциального поставщика удален.                                                                                                                                               |
|      Запрошенный пользователь      | При выборе <strong>Пригласить пользователя</strong> статус изменяется на <strong>Запрошенный пользователь</strong>, и запрос потенциального пользователя создается и отправляется в workflow-процесс запроса пользователя. |                                                                                                          Невозможно удалить запрос регистрации потенциального поставщика с этим статусом, поскольку workflow-процесс запроса пользователя еще не завершен.                                                                                                          |
|       Приглашенный пользователь       |                                                               Workflow-процесс запроса пользователя утвержден, и пользователь создан.                                                               |                                                                                                                      Создается запрос на деактивацию пользователя, и запрос регистрации потенциального поставщика удаляется.                                                                                                                      |
| Выполняется регистрация |                                                         Новый пользователь выполнил вход и запустил мастер регистрации поставщика.                                                          |                                                                                     Создается запрос на деактивацию пользователя, и запрос регистрации потенциального поставщика и данные, которые были введены в мастере регистрации поставщика, удаляются.                                                                                      |
|  Запрос поставщика создан  |                                                                     Мастер регистрации поставщика была выполнен.                                                                      | Создается запрос на деактивацию пользователя, и удаляются запрос регистрации потенциального поставщика, данные, которые были введены в мастере регистрации поставщика, и запрос поставщика.<blockquote>[!NOTE]<br>Нельзя использовать действие <strong>Удалить</strong>, когда запрос поставщика находится в процессе рассмотрения в workflow-процессе.</blockquote> |
|         Одобрено         |                                                                               Запрос поставщика утвержден.                                                                               |                                                                                                   Запрос регистрации потенциального поставщика, данные, которые были введены в мастере регистрации поставщика, и запрос поставщика удаляются.                                                                                                    |
|         Отклонено         |                                                                               Запрос поставщика отклонен.                                                                               |                                                                                                   Запрос регистрации потенциального поставщика, данные, которые были введены в мастере регистрации поставщика, и запрос поставщика удаляются.                                                                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
