---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220705"
---
# <span data-ttu-id="ace83-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ace83-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="ace83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ace83-102">SYNOPSIS</span></span>
<span data-ttu-id="ace83-103">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="ace83-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="ace83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ace83-104">SYNTAX</span></span>

### <span data-ttu-id="ace83-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ace83-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ace83-106">Получить</span><span class="sxs-lookup"><span data-stu-id="ace83-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ace83-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ace83-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ace83-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ace83-108">DESCRIPTION</span></span>
<span data-ttu-id="ace83-109">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="ace83-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="ace83-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ace83-110">EXAMPLES</span></span>

### <span data-ttu-id="ace83-111">Пример 1. Список всех конфигураций на сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="ace83-111">Example 1: List all configurations in PostgreSql server</span></span>
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

<span data-ttu-id="ace83-112">Этот cmdlet lists all configurations in specified PostgreSql server.</span><span class="sxs-lookup"><span data-stu-id="ace83-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="ace83-113">Пример 2. Получить указанную конфигурацию PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="ace83-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="ace83-114">Этот cmdlet получает заданную конфигурацию PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="ace83-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="ace83-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ace83-115">PARAMETERS</span></span>

### <span data-ttu-id="ace83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace83-116">-DefaultProfile</span></span>
<span data-ttu-id="ace83-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ace83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ace83-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ace83-118">-InputObject</span></span>
<span data-ttu-id="ace83-119">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ace83-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ace83-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ace83-120">-Name</span></span>
<span data-ttu-id="ace83-121">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="ace83-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="ace83-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace83-122">-ResourceGroupName</span></span>
<span data-ttu-id="ace83-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ace83-123">The name of the resource group.</span></span>
<span data-ttu-id="ace83-124">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ace83-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ace83-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ace83-125">-ServerName</span></span>
<span data-ttu-id="ace83-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ace83-126">The name of the server.</span></span>

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

### <span data-ttu-id="ace83-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ace83-127">-SubscriptionId</span></span>
<span data-ttu-id="ace83-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ace83-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ace83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace83-129">CommonParameters</span></span>
<span data-ttu-id="ace83-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace83-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ace83-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace83-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ace83-132">INPUTS</span></span>

### <span data-ttu-id="ace83-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ace83-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="ace83-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ace83-134">OUTPUTS</span></span>

### <span data-ttu-id="ace83-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="ace83-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="ace83-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ace83-136">NOTES</span></span>

<span data-ttu-id="ace83-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ace83-137">ALIASES</span></span>

<span data-ttu-id="ace83-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ace83-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ace83-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ace83-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ace83-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ace83-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ace83-141">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ace83-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ace83-142">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="ace83-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ace83-143">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ace83-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ace83-144">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="ace83-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ace83-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ace83-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ace83-146">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="ace83-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ace83-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ace83-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ace83-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ace83-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="ace83-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ace83-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ace83-150">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ace83-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ace83-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ace83-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ace83-152">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="ace83-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ace83-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ace83-153">RELATED LINKS</span></span>

