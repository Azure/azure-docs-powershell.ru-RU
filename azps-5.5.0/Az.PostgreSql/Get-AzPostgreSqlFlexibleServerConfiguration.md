---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0f65a007a37df559802a134ec5d6d8fc6fb33d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213228"
---
# <span data-ttu-id="df49f-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="df49f-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="df49f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df49f-102">SYNOPSIS</span></span>
<span data-ttu-id="df49f-103">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="df49f-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="df49f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="df49f-104">SYNTAX</span></span>

### <span data-ttu-id="df49f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df49f-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="df49f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="df49f-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="df49f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="df49f-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="df49f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df49f-108">DESCRIPTION</span></span>
<span data-ttu-id="df49f-109">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="df49f-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="df49f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="df49f-110">EXAMPLES</span></span>

### <span data-ttu-id="df49f-111">Пример 1. Получить указанную конфигурацию PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="df49f-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="df49f-112">Этот cmdlet получает заданную конфигурацию PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="df49f-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="df49f-113">Пример 2. Список всех конфигураций на указанном сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="df49f-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="df49f-114">Этот cmdlet lists all configurations in specified PostgreSql server.</span><span class="sxs-lookup"><span data-stu-id="df49f-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="df49f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df49f-115">PARAMETERS</span></span>

### <span data-ttu-id="df49f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df49f-116">-DefaultProfile</span></span>
<span data-ttu-id="df49f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df49f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df49f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df49f-118">-InputObject</span></span>
<span data-ttu-id="df49f-119">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="df49f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="df49f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="df49f-120">-Name</span></span>
<span data-ttu-id="df49f-121">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="df49f-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="df49f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df49f-122">-ResourceGroupName</span></span>
<span data-ttu-id="df49f-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df49f-123">The name of the resource group.</span></span>
<span data-ttu-id="df49f-124">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="df49f-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="df49f-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df49f-125">-ServerName</span></span>
<span data-ttu-id="df49f-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="df49f-126">The name of the server.</span></span>

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

### <span data-ttu-id="df49f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df49f-127">-SubscriptionId</span></span>
<span data-ttu-id="df49f-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="df49f-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="df49f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df49f-129">CommonParameters</span></span>
<span data-ttu-id="df49f-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df49f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df49f-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df49f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df49f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df49f-132">INPUTS</span></span>

### <span data-ttu-id="df49f-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="df49f-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="df49f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df49f-134">OUTPUTS</span></span>

### <span data-ttu-id="df49f-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="df49f-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="df49f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="df49f-136">NOTES</span></span>

<span data-ttu-id="df49f-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="df49f-137">ALIASES</span></span>

<span data-ttu-id="df49f-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="df49f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df49f-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="df49f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df49f-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df49f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df49f-141">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="df49f-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df49f-142">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="df49f-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="df49f-143">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="df49f-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="df49f-144">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="df49f-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="df49f-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="df49f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df49f-146">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="df49f-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="df49f-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df49f-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="df49f-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="df49f-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="df49f-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="df49f-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="df49f-150">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="df49f-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="df49f-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="df49f-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="df49f-152">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="df49f-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="df49f-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df49f-153">RELATED LINKS</span></span>

