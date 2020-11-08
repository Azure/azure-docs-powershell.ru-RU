---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247929"
---
# <span data-ttu-id="d1b6b-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1b6b-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="d1b6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b6b-103">Получает сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="d1b6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1b6b-104">SYNTAX</span></span>

### <span data-ttu-id="d1b6b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1b6b-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1b6b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d1b6b-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1b6b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1b6b-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1b6b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1b6b-108">DESCRIPTION</span></span>
<span data-ttu-id="d1b6b-109">Получает сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="d1b6b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1b6b-110">EXAMPLES</span></span>

### <span data-ttu-id="d1b6b-111">Пример 1: список всех конфигураций на сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="d1b6b-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="d1b6b-112">Этот командлет выводит список всех конфигураций на указанном сервере PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="d1b6b-113">Пример 2: получение указанной конфигурации PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="d1b6b-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="d1b6b-114">Этот командлет получает определенную конфигурацию PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="d1b6b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1b6b-115">PARAMETERS</span></span>

### <span data-ttu-id="d1b6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b6b-116">-DefaultProfile</span></span>
<span data-ttu-id="d1b6b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b6b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1b6b-118">-InputObject</span></span>
<span data-ttu-id="d1b6b-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1b6b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1b6b-120">-Name</span></span>
<span data-ttu-id="d1b6b-121">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b6b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1b6b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d1b6b-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-123">The name of the resource group.</span></span>
<span data-ttu-id="d1b6b-124">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-124">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b6b-125">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d1b6b-125">-ServerName</span></span>
<span data-ttu-id="d1b6b-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b6b-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1b6b-127">-SubscriptionId</span></span>
<span data-ttu-id="d1b6b-128">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b6b-129">CommonParameters</span></span>
<span data-ttu-id="d1b6b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b6b-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1b6b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b6b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1b6b-132">INPUTS</span></span>

### <span data-ttu-id="d1b6b-133">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d1b6b-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d1b6b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1b6b-134">OUTPUTS</span></span>

### <span data-ttu-id="d1b6b-135">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1b6b-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="d1b6b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1b6b-136">NOTES</span></span>

<span data-ttu-id="d1b6b-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d1b6b-137">ALIASES</span></span>

<span data-ttu-id="d1b6b-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d1b6b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1b6b-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1b6b-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1b6b-141">INPUTOBJECT <IPostgreSqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d1b6b-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1b6b-142">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d1b6b-143">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d1b6b-144">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d1b6b-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d1b6b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1b6b-146">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d1b6b-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d1b6b-148">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="d1b6b-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d1b6b-150">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d1b6b-151">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d1b6b-152">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d1b6b-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d1b6b-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1b6b-153">RELATED LINKS</span></span>

