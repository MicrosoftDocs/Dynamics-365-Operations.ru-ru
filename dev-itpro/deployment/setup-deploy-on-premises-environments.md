---
title: "Настройка и развертывание локальных сред"
description: "В этом разделе представлена информация о том, как запланировать, настроить и развернуть локальную среду."
author: sarvanisathish
manager: AnnBe
ms.date: 08/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Unified Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: ru-ru
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Настройка и развертывание локальных сред

В этом документе описывается, как запланировать развертывание, настроить инфраструктуру и выполнить развертывание Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise (локальный).

## <a name="finance-and-operations-components"></a>Компоненты Finance and Operations

Приложение Finance and Operations состоит из трех основных компонентов:

- Сервер Application Object Server (AOS)
- Бизнес-аналитика (BI)
- Финансовая отчетность/Management Reporter

Эти компоненты зависят от следующего программного обеспечения системы:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 с пакетом обновления 1 (SP1), который имеет следующие функции:

    - Включен поиск по полнотекстовому индексу.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > Приложение не будет работать, если не включен полнотекстовый поиск.

- SQL Server Management Studio
- Автономный кластер Microsoft Azure Service Fabric
- Windows PowerShell 5.0 или более поздней версии
- Active Directory Federation Services (AD FS) в Windows Server 2016

  Контроллером домена должен быть Windows Server 2012 R2 или более поздней версии с функциональным уровнем домена 2012 R2 или выше.

  Дополнительные сведения о функциональных уровнях домена см. в разделе: 
  - [Описание функциональных уровней Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Общие сведения о функциональных уровнях доменных служб Active Directory](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Компоненты Finance and Operations распределены во всех службах Microsoft Dynamics Lifecycle Services (LCS). Перед развертыванием необходимо приобрести лицензионные ключи через канал [Соглашение Enterprise Agreement](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) и настроить локальный проект в LCS. Развертывание может быть инициировано только через LCS. Дополнительные сведения о настройке локальных проектов в LCS см. в разделе [Создание локального проекта в Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Аутентификация

Локальное приложение работает со службами AD FS. Для взаимодействия с LCS необходимо также настроить Active Directory Azure (Azure AD).

## <a name="standalone-service-fabric"></a>Автономный кластер Service Fabric

Finance and Operations использует автономный кластер Service Fabric. Дополнительные сведения см. в [документации по Service Fabric](/azure/service-fabric/).

## <a name="infrastructure"></a>Инфраструктура

Приложение Finance and Operations предназначено для работы в гиперконвергированной архитектуре. Конфигурация оборудования включает следующие компоненты:

- Автономный кластер Service Fabric на основе виртуальных машин Windows Server 2016
- SQL Server (поддерживается кластеризованный SQL и Always-On)
- AD FS для проверки подлинности
- Файловый ресурс общего доступа Server Message Block (SMB) версии 3 для хранения
- Дополнительно: Microsoft Office Server 2017

Дополнительные сведения см. в разделе [Требования к системе](../get-started/system-requirements.md) и руководствах по определению размеров.

### <a name="hardware-layout"></a>Макет оборудования

Планируйте инфраструктуру и кластер Service Fabric на основании рекомендованных размеров в разделе [Определение параметров оборудования для локальных сред](../get-started/hardware-sizing-on-premises-environments.md). Дополнительные сведения о планировании кластера Service Fabric см. в разделе [Планирование и подготовка развертывания изолированного кластера Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

В следующей таблице показан пример макета оборудования. Этот пример используется во всем разделе для демонстрации настройки.

> [!NOTE]
> Первичный узел кластера Service Fabric должен иметь по крайней мере три узла. В этом примере **OrchestratorType** определяется как тип первичного узла.

| Назначение компьютера                                 | Имя компьютера    | IP-адрес    |
|-------------------------------------------------|-----------------|---------------|
| Контроллер домена                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Файл-сервер                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| Кластер SQL Always-On                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Клиент                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Кластер Service Fabric/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Кластер Service Fabric/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Кластер Service Fabric/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Кластер Service Fabric/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Кластер Service Fabric/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Кластер Service Fabric/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Кластер Service Fabric/узел Management Reporter | SQLAOSMR1       | 10.179.108.18 |
| Кластер Service Fabric/узел SSRS                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Настройка

### <a name="prerequisites"></a>Необходимые условия

Перед началом настройки должны быть выполнены следующие предварительные условия. Настройка этих необходимых условий не входит в этот документ.

- Службы Active Directory Domain Services (AD DS) установлены и настроены в вашей сети.
- Развернуты AD FS.
- Установлены SQL Server, SSRS и Management Studio.

### <a name="overview"></a>Обзор

Для настройки инфраструктуры для Finance and Operations необходимо выполнить следующие действия.

1. Планирование имени домена и зон DNS
2. Планирование и приобретение сертификатов
3. Планирование пользователей и учетных записей служб
4. Создание зон DNS и добавление записей A
5. Присоединение виртуальных машин к домену
6. Добавление необходимого программного обеспечения на виртуальные машины
7. Загрузка сценариев настройки из LCS
8. Описание конфигурации
9. Установка сертификатов
10. Настройка автономного кластера Service Fabric
11. Настройка подключения LCS для клиента
12. Настройка хранилища файлов
13. Настройка SQL Server
14. Настройка баз данных
15. Шифрование учетных данных
16. Настроить SSRS
17. Настройка AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>Планирование имени домена и зон DNS

Рекомендуется использовать публично зарегистрированное имя домена для производственной установки AOS. Таким образом доступ к нему можно получить вне сети, если необходим внешний доступ.

Например, если доменом компании является contoso.com, ваша зона для Finance and Operations (локальная версия) может быть d365ffo.onprem.contoso.com, и имена узлов могут быть следующими:

- ax.d365ffo.onprem.contoso.com для компьютеров AOS
- sf.d365ffo.onprem.contoso.com для кластера Service Fabric

### <a name="plan-and-acquire-your-certificates"></a>Планирование и приобретение сертификатов

Сертификаты Secure Sockets Layer (SSL) требуются для обеспечения безопасности кластера Service Fabric и всех развернутых приложений. Для производственной рабочей нагрузки и рабочей нагрузки в песочнице рекомендуется приобрести сертификаты в центре сертификации (CA), например [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) или [GlobalSign](https://www.globalsign.com/en/ssl/). Если домен настроен с использованием [служб сертификатов Active Directory](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), можно создавать сертификаты с помощью AD CS. Каждый сертификат должен содержать закрытый ключ, который был создан для обмена ключами и должен являться экспортируемым в файл Personal Information Exchange (PFX).

Самозаверяющие сертификаты можно использовать только в целях тестирования. Для удобства сценарии настройки включают сценарии, которые создают и экспортируют самозаверяющие сертификаты. Как было сказано ранее, эти сертификаты необходимо использовать только в целях тестирования.

| Цель                                      | Пояснение | Дополнительные требования |
|----------------------------------------------|-------------|-------------------------|
| Сертификат SSL SQL Server                   | Этот сертификат используется для шифрования данных, передаваемых по сети между экземпляром SQL Server и клиентским приложением. | <p>Имя домена сертификата должно совпадать с полностью определенным именем домена (FQDN) экземпляр SQL Server или слушателя.</p><p>Например, если слушатель SQL размещен на компьютере DAX7SQLAOSQLA, имя DNS сертификата — DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Сертификат сервера Service Fabric            | Этот сертификат используется для обеспечения безопасности связи узел–узел между узлами Service Fabric. Этот сертификат также используется в качестве сертификата сервера, представляемого клиенту, который подключается к кластеру. | <p>Имя домена сертификата должно соответствовать зоне DNS, в которой размещены AOS и Service Fabric.</p><p>Например, именем домена сертификата может быть \*.onprem.contoso.com или \*.contoso.com.</p><p>При использовании группового сертификата подстановочный знак применяется только к одному уровню. Поддомен, альтернативное имя субъекта (SAN), должен применяться к сертификату при наличии нескольких уровней, например \*.contoso.com в предыдущем примере.</p> |
| Сертификат клиента Service Fabric            | Этот сертификат используется клиентами для просмотра кластера Service Fabric и управления им. | |
| Сертификат шифрования                     | Этот сертификат используется для шифрования конфиденциальной информации, например пароля SQL Server и паролей учетных записей пользователей. | <p>Использование ключа сертификата должно включать шифрование данных (10) и не должно включать проверку подлинности сервера или клиента.</p><p>Дополнительные сведения см. в разделе [Управление секретами в приложениях Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| Сертификат SSL AOS                          | <p>Этот сертификат используется в качестве сертификата сервера, представляемого клиенту для веб-сайта AOS. Он также используется для включения сертификатов Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP).</p><p>Сертификат сервера Service Fabric можно использовать, если он является групповым.</p> | <p>Имя домена сертификата должно соответствовать зоне DNS, в которой размещены AOS и Service Fabric.</p><p>Например, именем домена сертификата может быть \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com или \*.contoso.com.</p><p>При использовании группового сертификата подстановочный знак применяется только к одному уровню. Поддомен (SAN) должен применяться к сертификату при наличии нескольких уровней, например \*.contoso.com в предыдущем примере.</p> |
| Сертификат проверки подлинности сессии           | Этот сертификат используется AOS для обеспечения безопасности сведений о сессии пользователя. | Это также сертификат **файлового ресурса общего доступа**, который будет использоваться во время развертывания из LCS. |
| Сертификат шифрования данных и сертификат подписи данных | Эти сертификаты используются AOS для шифрования конфиденциальной информации. | |
| Сертификат клиента финансовой отчетности       | Этот сертификат используется для обеспечения безопасности связи между службами Reporting Services и AOS. | |
| Сертификат отчетности                        | Этот сертификат используется для обеспечения безопасности связи между службами SSRS и AOS. | |
| Сертификат локального агента локальной версии           | <p>Этот сертификат используется для обеспечения безопасности связи между локальным агентом, размещенным локально, и LCS.</p><p>Этот сертификат позволяет локальному агенту действовать от имени вашего клиента Azure AD, а также обмениваться данными с LCS для организации и отслеживания развертываний.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Планирование пользователей и учетных записей служб

Необходимо создать несколько учетных записей пользователей или служб для того, чтобы приложение Finance and Operations (локальная версия) работало. Создайте комбинацию групповых управляемых учетных записей (gMSA), учетных записей доменов и учетных записей SQL. Следующая таблица показывает учетные записи пользователей, их назначение и примеры имен, которые будут использоваться в этом разделе.

| Учетная запись пользователя                                            | Вид           | Цель | Имя пользователя |
|---------------------------------------------------------|----------------|---------|-----------|
| Учетная запись службы приложения финансовой отчетности         | gMSA           |         | Contoso\\svc-FRAS$ |
| Учетная запись службы процесса финансовой отчетности             | gMSA           |         | Contoso\\svc-FRPS$ |
| Учетная запись службы конструктора ClickOnce финансовой отчетности | gMSA           |         | Contoso\\svc-FRCO$ |
| Учетная запись службы AOS                                     | gMSA           | Этот пользователь должен создаваться для проверки в будущем. Мы планируем включить AOS для работы с gMSA в будущих выпусках. Создав этого пользователя во время настройки, вы поможет обеспечить плавный переход на gMSA. | Contoso\\svc-AXSF$ |
| Учетная запись службы AOS                                     | Учетная запись домена | AOS использует этого пользователя в общедоступном выпуске. | Contoso\\AXServiceUser |
| Пользователь-администратор базы данных AOS SQL                                   | Пользователь SQL       | Finance and Operations использует этого пользователя для проверки подлинности с помощью SQL\*. Этот пользователь также будет заменен на пользователя gMSA в будущих выпусках. | AXDBAdmin |
| Учетная запись службы агента локального развертывания                  | gMSA           | Эта учетная запись используется локальным агентом для организации развертывания в различных узлах. | Contoso\\Svc-LocalAgent$ |

\* Имя пользователя и пароль SQL для проверки подлинности SQL защищены, поскольку они шифруются и хранятся в файловом ресурсе общего доступа.

### <a name="create-dns-zones-and-add-a-records"></a>Создание зон DNS и добавление записей A

DNS интегрирован с AD DS и позволяет организовывать и искать ресурсы в сети и управлять ими. Создайте зону прямого просмотра DNS и записи А для имени узла AOS и кластера Service Fabric. В этом примере настройки имя зоны DNS — d365ffo.onprem.contoso.com, а имена записей А/узла следующие:

- **ax**.d365ffo.onprem.contoso.com для компьютеров AOS
- **sf**.d365ffo.onprem.contoso.com для кластера Service Fabric

#### <a name="add-a-dns-zone"></a>Добавление зоны DNS

Используйте следующую процедуру для добавления зоны DNS.

1. Войдите на компьютер контроллера домена, нажмите кнопку **Начать** и запустите диспетчер DNS, введя **dnsmgmt.msc**.
2. Щелкните правой кнопкой мыши имя контроллера домена, а затем щелкните **Новая зона** \> **Далее**.
3. Выберите **Основная зона**.
4. Оставьте флажок **Хранить зону в Active Directory (доступно, только если сервер DNS является доступным для записи контроллером домена)** и нажмите кнопку **Далее**.
5. Выберите **Для всех серверов DNS, работающих в контроллерах домена в этом домене: Contoso.com** и нажмите кнопку **Далее**.
6. Выберите **Зона прямого просмотра**, а затем щелкните **Далее**.
7. Введите имя зоны для настройки и нажмите кнопку **Далее**. Например, введите **d365ffo.onprem.contoso.com**.
8. Выберите **Не разрешать динамические обновления** и нажмите кнопку **Далее**.

#### <a name="set-up-an-a-record-for-aos"></a>Настройка записи А для AOS

В новой зоне DNS создайте одну запись A, которая называется **ax.d365ffo.onprem.contoso.com** для **каждого** узла кластера Service Fabric типа **AOSNodeType**. Не создавайте записи А для других типов узлов.

1. Щелкните правой кнопкой мыши новую зону и выберите пункт **Новый узел**.
2. Введите имя и IP-адрес узла Service Fabric (например, 10.179.108.12) и нажмите кнопку **Добавить узел**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Настройка записи А для Orchestrator

В новой зоне DNS создайте запись A, которая называется **sf.d365ffo.onprem.contoso.com** для **каждого** узла кластера Service Fabric типа **OrchestratorType**. Не создавайте записи А для других типов узлов.

1. Щелкните правой кнопкой мыши новую зону и выберите пункт **Новый узел**.
2. Введите имя и IP-адрес узла Service Fabric (например, 10.179.108.15) и нажмите кнопку **Добавить узел**.

#### <a name="join-vms-to-the-domain"></a>Присоединение виртуальных машин к домену

Присоедините каждую из виртуальных машин к домену, выполнив действия, описанные в статье [Как включить Windows Server 2016 в домен Active Directory](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html). Либо используйте сценарий Windows PowerShell.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
После присоединения виртуальных машин к домену добавьте учетные записи служб AOS (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ) в группу локальных администраторов. Сведения о том, как это сделать см. в статье [Добавление участника в локальную группу](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx).

#### <a name="disable-user-access-control"></a>Отключение управления доступом пользователей 

Выполните следующий сценарий, чтобы отключить управление доступом пользователей в **каждом** узле Service Fabric.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> После успешного выполнения сценария необходимо перезагрузить узел.

#### <a name="add-prerequisite-software-to-vms"></a>Добавление необходимого программного обеспечения на виртуальные машины

В следующей таблице перечислено необходимое программное обеспечение, которое должно быть применено на компьютерах каждого типа узла.

> [!NOTE]
> Необходимо перезагрузить компьютер после установки компонентов.

| Тип узла | Компонент | Команда |
|-----------|-----------|---------|
| AOS       | SNAC – драйвер ODBC | См. раздел [Microsoft ODBC Driver 13.1 for SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Framework версии 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework версии 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Службы IIS (Internet Information Services) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Распространяемые пакеты Microsoft Visual C++ для Microsoft Visual Studio 2013 | См. раздел [Распространяемые пакеты Microsoft Visual C++ для Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Распространяемый пакет ядра СУБД Microsoft Access 2010 | См. раздел [Распространяемый пакет ядра СУБД Microsoft Access 2010](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI (бизнес-аналитика)        | .NET Framework версии 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI (бизнес-аналитика)        | .NET Framework версии 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI (бизнес-аналитика)        | Microsoft SQL Server 2016 с пакетом обновления 1 (SP1) | |
| BI (бизнес-аналитика)        | Management Studio 2016 | |
| BI (бизнес-аналитика)        | SQL Server Reporting Services 2016 в режиме **Собственный** | |
| MR        | .NET Framework версии 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework версии 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Распространяемые пакеты Microsoft Visual C++ для Visual Studio 2013 | См. раздел [Распространяемые пакеты Microsoft Visual C++ для Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Загрузка сценариев настройки из LCS

Мы предоставили несколько сценариев, которые помогут упростить процедуру настройки. Выполните следующие действия для загрузки сценариев настройки из LCS.

1. Войдите в LCS (<https://lcs.dynamics.com/v2>).
2. На панели мониторинга щелкните плитку **Общая библиотека активов**.
3. Перейдите на вкладку **Модель**.
4. В таблице выберите строку **Dynamics 365 for Operations — сценарии развертывания локальной версии**.
5. Щелкните **Версии** и загрузите последнюю версию сценариев.

### <a name="describe-your-configuration"></a>Описание конфигурации

В этом разделе представлена информация о сценариях, которые необходимо выполнить. Сценарии рассматриваются в порядке их выполнения. Для выполнения сценариев заполните файл шаблона в $(downloadPath)\\ConfigTemplate.xml. В файле ConfigTemplate.xml описываются кластеры Service Fabric, сертификаты, которые используются для их настройки, и учетные записи, которым должен быть предоставлен доступ к соответствующим сертификатам. В предоставленном примере значения заполняются для примера инфраструктуры, описанной в этой теме. Файл шаблона будет использоваться в следующем разделе.

#### <a name="create-the-domain-account-for-a-service-user"></a>Создание учетной записи домена для пользователя службы

Выполните следующую команду, чтобы создать учетную запись пользователя домена contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>Создание gMSA

1. Перейдите в каталог **$(DownloadPath)** и выполните следующую команду Windows PowerShell.

    > [!NOTE]
    > Этот сценарий не создает пользователей. Вместо этого будут напечатаны команды, которые должны выполняться вручную на компьютере контроллера домена.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Скопируйте результат выполнения команды в окно Windows PowerShell. Убедитесь в том, что разрывы строк удалены, и выполните строки на компьютере контроллера домена Active Directory с использованием повышенных привилегий (щелкните правой кнопкой мыши, а затем щелкните **Запуск от имени администратора**).
3. Запустите следующий сценарий на компьютере контроллера домена Active Directory, чтобы проверить, что учетные записи успешно созданы. Убедитесь, что сценарий выполняется после замены шаблона, который соответствует соглашению об именах учетных записей служб.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Запустите сценарий Export-AddGMSAsONVMScript.ps1 на клиентском компьютере. Этот сценарий создает сценарии, которые выполняются на каждой виртуальной машине Service Fabric, и добавляет их в папку, которая соответствует каждому имени виртуальной машины.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>Остановка IIS

Используйте протокол удаленного рабочего стола (RDP) для подключения к каждой виртуальной машине Service Fabric и завершите шаги вручную в разделе [Start or Stop the Web Server (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx). Либо используйте следующий сценарий Windows PowerShell с помощью RDP для подключения к каждой виртуальной машине Service Fabric.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_Функция IIS должна быть установлена, но отключена, поскольку существуют некоторые зависимости библиотек DLL служб IIS в продукте._

### <a name="install-certificates"></a>Установка сертификатов

1. Если вы приобрели сертификаты, которые были перечислены выше в этой теме, в допустимом центре сертификации, заполните имя PFX-файла и отпечаток для сертификатов в файле ConfigTemplate.xml. Задайте для атрибута **generateSelfSignedCert** значение **False**, а для атрибута **exportable** — значение **False**. Скопируйте PFX-файлы в папку $(DownloadPath)\\InfrastructureScripts\\Certs.
2. Если вы используете самозаверяющие сертификаты (только в целях тестирования), выполните следующий сценарий. Чтобы создать самозаверяющие сертификаты, в файле ConfigTemplate.xml убедитесь, что для **generateSelfSignedCert** задано значение **True** и для **exportable** задано значение **True**. Этот сценарий обновит XML для включения отпечатка для сертификатов.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Экспортируйте новые сертификаты с закрытым ключом (PFX-файл). Используйте следующий сценарий для создания и выполнения команд экспорта в Windows PowerShell. PFX-файлы будут помещены в папку Certs.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Сертификаты должны быть установлены и должны присутствовать в папке cert:\\CurrentUser\\My. Также сертификаты должны быть доступны для экспорта.

    Если вы используете самозаверяющие сертификаты, перейдите к следующему разделу. Вам не требуется выполнять эту процедуру.

4. После экспорта или копирования PFX-файлов в папку $(DownloadPath)\\InfrastructureScripts\\Certs выполните следующие команды для создания сценариев, которые будут помещены в папки, соответствующие виртуальным машинам.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Скопируйте сценарии в каждой папке на виртуальные машины, которые соответствуют имени папки.
6. На каждой виртуальной машине выполните следующие сценарии в порядке их появления.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Настройка автономного кластера Service Fabric

1. Выполните следующую команду, чтобы создать файл ClusterConfig.json.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Дополнительные сведения см. в разделах [Шаг 1Б. Создание кластера с несколькими компьютерами](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Защита автономного кластера под управлением Windows с помощью сертификатов X.509](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) и [Создание изолированного кластера под управлением Windows Server](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Загрузите [пакет установки автономного кластера Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) в один из узлов Service Fabric. После загрузки ZIP-файла разблокируйте его, щелкнув правой кнопкой мыши ZIP-файл, и выберите **Свойства**. В диалоговом окне установите флажок **Разблокировать** в правом нижнем углу.
3. Скопируйте ZIP-файл в один из узлов в кластере Service Fabric и распакуйте его.
4. Выполните следующие команды для создания правила брандмауэра для входящего трафика в портах 443 и 445 во всех узлах.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Выполните следующие команды для создания правила брандмауэра для входящего трафика в порте 80 только для узла SSRS.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Скопируйте файл ClusterConfig.json в место распакованной установки автономного кластера Service Fabric.
7. Перейдите в место распакованной установки в Windows PowerShell, используя повышенные привилегии, и выполните следующую команду для проверки ClusterConfig.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Если проверка прошла успешно, выполните следующую команду для развертывания кластера.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. После создания кластера откройте обозреватель Service Fabric на любом клиентском компьютере для проверки установки:

    1. Установите сертификат клиента Service Fabric в папку CurrentUser\\My, если он еще не установлен.
    2. Перейдите в раздел **Параметры IE** \> **Режим совместимости** и снимите флажок **Отображать сайты Intranet в режиме совместимости**.
    3. Перейдите в `https://sf.d365ffo.onprem.contoso.com:19080`, где sf.d365ffo.onprem.contoso.com — это имя узла кластера Service Fabric, указанного в зоне. Если не настроено разрешение имени DNS, используйте IP-адрес компьютера.
    4. Выберите сертификат клиента. Отобразится страница **Проводник Service Fabric**.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Настройка подключения LCS для клиента

Развертывание и обслуживание Finance and Operations выполняется через LCS с помощью локального агента локальной версии. Чтобы установить соединение между LCS и клиентом Finance and Operations, необходимо настроить сертификат, позволяющий локальному агенту действовать от имени ваших клиентов Azure AD (например, Contoso.Onmicrosoft.com).

Используйте сертификат агента локальной версии, который вы приобрели в центре сертификации, или самозаверяющий сертификат, созданный с помощью сценариев.

Только учетные записи пользователей, имеющие роль каталога "Глобальный администратор", могут добавлять сертификаты для авторизации LCS. По умолчанию тот, кто регистрируется в Microsoft Office 365 для вашей организации, будет глобальным администратором каталога.

> [!NOTE]
> Сертификат необходимо настроить один раз для каждого клиента. Все локальные среды могут использовать один и тот же сертификат для подключения к LCS.

1. Загрузите и установите последнюю версию Azure PowerShell на клиентском компьютере. Дополнительные сведения см. в разделе [Установка и настройка Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Выполните вход на [портал Azure клиента](https://portal.azure.com) для проверки наличия роли каталога "Глобальный администратор".
3. Запустите следующий сценарий из $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Настройка хранилища файлов

Необходимо настроить два высокодоступных файловых ресурсов общего доступа SMB 3.0. Сведения о включении SMB 3.0 см. в разделе [Улучшения безопасности SMB](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Согласование безопасности диалекта не может обнаружить или предотвратить возврат с SMB 2.0 или 3.0 к предыдущей версии SMB 1.0. По этой причине и для использования всех возможностей шифрования SMB настоятельно рекомендуется отключить сервер SMB 1.0.

> [!NOTE]
> Чтобы помочь обеспечить защиту данных, когда они не используются в вашей среде, необходимо включить шифрование диска BitLocker на каждом компьютере. Дополнительные сведения о том, как включить BitLocker, см. в разделе [BitLocker. Развертывание в Windows Server 2012 и более поздних версиях](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Файловый ресурс общего доступа, в котором хранятся документы пользователей, отправленные в AOS (например, \\\\DAX7SQLAOFILE1\\aos-storage).
- Файловый ресурс общего доступа, в котором хранятся последние файлы сборки и конфигурации для управления развертыванием (например, \\\\DAX7SQLAOFILE1\\agent).

    > [!NOTE]
    > Имя этого файлового ресурса общего доступа должно быть максимально коротким, чтобы избежать превышения максимальной длины пути в файлах, которые будут помещены в файловый ресурс общего доступа.

1. На компьютере файлового ресурса общего доступа выполните следующую команду.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Настройка файлового ресурса общего доступа \\\\DAX7SQLAOFILE1\\aos-storage

2. В диспетчере серверов выберите **Файловые службы и службы хранилища** \> **Общие ресурсы**.
3. Щелкните **Задачи** \> **Новый общий ресурс**, чтобы создать новый общий ресурс с именем **aos-storage**.
4. Предоставьте разрешения **Изменить** для каждого компьютера в кластере Service Fabric, кроме **OrchestratorNodeType**.
5. Предоставьте разрешения **Изменить** для пользователя домена AOS пользователя (contoso\\AXServiceUser) и пользователя gMSA (contoso\\svc-AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Настройка файлового ресурса общего доступа \\\\DAX7SQLAOFILE1\\agent

6. Вернитесь в диспетчер серверов и выберите **Файловые службы и службы хранилища** \> **Общие ресурсы**.
7. Щелкните **Задачи** \> **Новый общий ресурс**, чтобы создать новый общий ресурс с именем **agent**.
8. Предоставьте разрешения **Полное управление** пользователю gMSA для агента локального развертывания (contoso\\svc-LocalAgent$).

### <a name="set-up-sql-server"></a>Настройка SQL Server

1. Установите SQL Server 2016 с пакетом обновления 1 (SP1) с высокой доступностью как кластеры SQL, которые включают сеть хранения данных (SAN), или конфигурацию Always-On.  Убедитесь, что **ядро СУБД, службы Reporting Services, полнотекстовый поиск** и **Средства управления** установлены.
> [!NOTE]
> Убедитесь, что SQL Always On настроено согласно разделу [Выбор страницы синхронизации первоначальных данных (мастера групп доступности Always On)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards), и следуйте инструкциям в разделе [Подготовка вторичных баз данных вручную](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Запустите службу SQL как пользователь домена.
3. Получите сертификат SSL из центра сертификации для настройки Finance and Operations. В целях тестирования можно создать и использовать самозаверяющий сертификат.

**Самозаверяющий сертификат для кластеризованного экземпляра SQL**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Самозаверяющий сертификат для экземпляра SQL Always-On**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. С помощью сертификата выполните действия в разделе [Включение шифрования SSL для экземпляра SQL Server с помощью консоли управления MMC](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) для настройки SSL в SQL Server.
5. Для каждого узла кластера выполните следующие действия. Убедитесь в том, что внесены изменения в неактивном узле, и выполните отработку отказа на него после внесения изменений.

    1. Импортируйте сертификат в папку LocalMachine\\My.
    2. Предоставьте разрешения сертификата учетной записи службы, используемой для запуска службы SQL. В консоли управления (MMC) щелкните правой кнопкой мыши сертификат (certlm.msc) и щелкните **Задачи** \> **Управление закрытыми ключами**.
    3. Добавьте отпечаток сертификата в HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. В диспетчере конфигурации Microsoft SQL Server установите для параметра **ForceEncryption** значение **Да**.

6. Экспортируйте открытый ключ сертификат (CER-файл) и установите его в доверенный корень каждого узла Service Fabric.

### <a name="configure-the-orchestratordata-database"></a>Настройка базы данных OrchestratorData

1.  Создайте пустую базу данных и назовите ее **OrchestratorData**. Эта база данных используется локальным агентом локальной версии для управления развертываниями.
2.  Предоставьте gMSA локального агента (svc-LocalAgent$) разрешения **db\_owner** в базе данных:

    1. В дереве разверните имя сервера, разверните папку узел **Безопасность** \> **Имена входа**, затем щелкните правой кнопкой мыши и выберите **Создать имя входа**.

        ![Команда "Создать имя входа"](./media/OPSetup_01_NewLogin.png)


    2. Найдите учетную запись службы **svc-LocalAgent$**. Щелкните **Местоположения** и выберите **Весь каталог**, а затем нажмите кнопку **Типы объектов** и выберите **Учетная запись службы**.

        ![Диалоговое окно "Выбрать пользователя, учетную запись службы или группу"](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Задайте для параметра **Назначить ServerRole** значение **Общий**.
    4. Назначьте разрешение роли базы данных **db\_owner** базе данных OrchestratorData.

### <a name="configure-the-finance-and-operations-database"></a>Настройка базы данных Finance and Operations

1. Войдите в LCS (<https://lcs.dynamics.com/v2>).
2. На панели мониторинга щелкните плитку **Общая библиотека активов**.
3. Перейдите на вкладку **Модель**. 
4. В сетке щелкните строку **Dynamics 365 for Operations (локальная версия), выпуск Enterprise — демонстрационные данные**, чтобы загрузить ZIP-файл.
5. ZIP-файл содержит пустой BAK-файл и BAK-файл с демонстрационными данными. На основании своих потребностей выберите соответствующий BAK-файл. Например, если требуются демонстрационные данные, восстановите BAK-файл AxBootstrapDB_Demodata.bak. 
6. Восстановите базу данных AxBootstrapDB_DemoData.bak.
7. Переименуйте базу данных **AXDBRAIN**.
8. Выполните следующие запросы в восстановленной базе данных.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Обновите файлы базы данных:

    1. Щелкните правой кнопкой мыши базу данных и выберите пункт **Свойства**.
    2. Щелкните **Файлы** для изменения свойств файлов базы данных.
    3. В поле **Исходный размер (МБ)** введите значение больше 5 120.

        ![Диалоговое окно "Свойства базы данных"](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. Для параметра **AXDBBuild\_Data** задайте в поле **Авторасширение/Развернуть** значение **200** мегабайт (МБ).
    5. Для параметра **AXDBBuild\_Log** задайте в поле **Авторасширение/Развернуть** значение **500** МБ.

        ![Диалоговое окно "Изменение параметров автоувеличения"](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Создайте нового пользователя, для которого включена проверка подлинности SQL (axdbadmin).
6. Используйте сведения в следующей таблице, чтобы сопоставить пользователей и роли базы данных.

    | Пользователь             | Вид    | Роль базы данных |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Предоставьте пользователю svc-AXSF$ и пользователю axdbadmin SQL доступ к следующим ролям в базе данных tempdb:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. В Management Studio выполните следующие команды Transact SQL (T-SQL):

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Выполните следующую команду:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Настройка базы данных финансовой отчетности

1.  Создайте пустую базу данных и назовите ее **FinancialReporting**.
2.  Используйте сведения в следующей таблице, чтобы сопоставить пользователей и роли базы данных.

    | Пользователь             | Вид | Роль базы данных |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Шифрование учетных данных

1. На любом клиентском компьютере установите сертификат шифрования в папку LocalMachine\\My certificate store.
2. Предоставьте текущему пользователю доступ на чтение закрытого ключа этого сертификата.
3. Создайте файл Credentials.json, как показано ниже.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** — зашифрованный пароль пользователя домена для пользователя домена AOS (contoso\\axserviceuser).
    - **SqlUser** — зашифрованный пользователь SQL (axdbadmin), который имеет доступ к базе данных Finance and Operations (AXDBRAIN), а **SqlPassword** — зашифрованный пароль SQL.

4. Скопируйте JSON-файл в файловый ресурс общего доступа SMB \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Обновите файл Credentials.json с зашифрованными значениями.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. В Credentials.json замените **\<encryptedDomainUserPassword\>** на зашифрованный пароль домена.
    2. Замените **\<encryptedSqlUser\>** на зашифрованного пользователя SQL Finance and Operations.
    3. Замените **\<encryptedSqlPassword\>** на пароль SQL Finance and Operations.
    
### <a name="set-up-ssrs"></a>Настроить SSRS

1.  Прежде чем начать, убедитесь, что установлены все необходимые компоненты, перечисленные в начале этой темы.
2.  Выполните процедуру [Настройка служб SQL Server Reporting Services для локального развертывания](../analytics/configure-ssrs-on-premises.md).

### <a name="configure-ad-fs"></a>Настройка AD FS

Перед выполнением этой процедуры необходимо развернуть AD FS в Windows Server 2016. Дополнительные сведения о развертывании AD FS см. в разделе [Руководство по развертыванию Windows Server 2016 и 2012 R2 AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Finance and Operations требует дополнительной настройки помимо встроенной конфигурации AD FS по умолчанию. Для выполнения следующих шагов Windows PowerShell работает на компьютере, на котором установлена служба роли AD FS. Учетная запись пользователя должна иметь достаточно разрешений для администрирования AD FS. Например, пользователь должен иметь учетную запись администратора домена.

1. Настройте идентификатор AD FS, чтобы он соответствовал поставщику маркера AD FS.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Следует отключить встроенную проверку подлинности Windows (WIA) для подключений проверки подлинности интрасети, если вы не настроили AD FS для смешанных сред. Дополнительные сведения о настройке WIA для использования с AD FS см. в разделе [Configure browsers to use Windows Integrated Authentication (WIA) with AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Для входа в систему адрес электронной почты пользователя должен представлять собой допустимые входные данные проверки подлинности.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

Чтобы службы AD FS доверяли Finance and Operations для обмена проверкой подлинности, необходимо зарегистрировать различные записи приложения в AD FS в группе приложений AD FS. Чтобы ускорить процесс настройки и помочь уменьшить количество ошибок, можно использовать следующий сценарий для регистрации. Скопируйте сценарий Publish-ADFSApplicationGroup.ps1 и каталог D365FO-OP на компьютер, на котором установлена служба роли AD FS. Затем запустите сценарий с помощью учетной записи пользователя, например учетной записи администратора, которая имеет достаточно разрешений на администрирование AD FS. Дополнительные сведения о том, как использовать сценарий, см. в документации, указанной в сценарии. Запишите идентификаторы клиентов, которые указаны в выходных данных, поскольку они потребуются в LCS позже.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

Консоль управления AD FS должна напоминать рисунок ниже. Чтобы открыть диспетчер серверов, щелкните **Сервис** \> **Управление AD FS**, а затем в нижней части дерева слева щелкните **Группы приложений**. Дважды щелкните группу приложений для просмотра более подробной информации.

![Свойства группы приложений](./media/OPSetup_05_ApplicatioGroupProperties.png)

Наконец, для проверки готовности к работе убедитесь, что вы можете получить доступ к URL-адресу конфигурации OpenID AD FS в узле Service Fabric типа **AOSNodeType**, перейдя в `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` в веб-обозревателе. Если появится сообщение о том, что сайт не безопасен, сертификат SSL AD FS не был добавлен в хранилище "Доверенные корневые центры сертификации". Этот шаг описан в руководстве по развертыванию AD FS. Если вы успешно получили доступ к URL-адресу, возвращается файл JavaScript Object Notation (JSON), содержащий конфигурацию AD FS, и вы увидите, что URL-адрес AD FS является доверенным.

На этом настройка инфраструктуры завершена. В следующих разделах описывается, как перейти к [LCS](https://lcs.dynamics.com) для настройки соединителя и развернуть среду Dynamics 365 for Finance and Operations.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Настройка соединителя и установка локального агента локальной версии

1. Выполните вход в [LCS](https://lcs.dynamics.com/) и откройте проект локальной реализации.
2. В меню щелкните **Параметры проекта**.

    ![Команда "Параметры проекта"](./media/OPSetup_06_ProjectSettings.png)

3. Щелкните **Локальные соединители**.
4. Нажмите кнопку **Добавить**, чтобы создать новый соединитель.
5. На вкладке **Настройка инфраструктуры узла** загрузите установщик агента.

    ![Кнопка "Загрузить установщик агента" на вкладке "Настройка инфраструктуры узла"](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Убедитесь, что ZIP-файл разблокирован. Щелкните правой кнопкой мыши файл, щелкните **Свойства** и выберите пункт **Разблокировать**.
7. Распакуйте установщик агента в одном из узлов Service Fabric типа **OrchestratorType**.
8. На вкладке **Настройка агента** введите параметры конфигурации.
9. Сохраните конфигурацию, а затем щелкните **Загрузить конфигурации** для загрузки файла конфигурации localagent-config.json.

    ![Кнопка "Загрузить конфигурации" на вкладке "Настройка агента"](./media/OPSetup_08_DownloadConfigurations.png)

10. Скопируйте файл localagent-config.json на компьютер, на котором находится пакет установщика агента.
11. В окне командной строки выполните следующую команду, перейдя в папку, которая содержит установщик агента.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Пользователь, запустивший эту команду, должен иметь разрешения **db\_owner** в базе данных OrchestratorData.
    
12. После успешной установки локального агента вернитесь к локальному соединителю в LCS.
13. На вкладке **Проверка настройки** нажмите кнопку **Агент сообщений**. Будет запущена проверка подключения LCS к локальному агенту. При успешной установке подключения страница будет выглядеть, как на следующем рисунке.

     ![Проверка агента](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Развертывание среды Dynamics 365 for Finance and Operations (локальная версия)

1. Перейдите к локальному проекту в LCS, выберите раздел **Среды**, **Песочница** и щелкните **Настроить**.
2. Выберите **Топология среды** и перейдите в мастер для инициирования развертывания.
3. Локальный агент получит запрос на развертывание, запустит развертывание и свяжется с LCS, когда все будет готово.

