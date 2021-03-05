---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 31f99de8a0afaf77345fbdc20782bdd725cb660b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970467"
---
# <span data-ttu-id="41a02-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="41a02-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="41a02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41a02-102">SYNOPSIS</span></span>
<span data-ttu-id="41a02-103">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="41a02-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="41a02-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41a02-104">SYNTAX</span></span>

### <span data-ttu-id="41a02-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41a02-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41a02-106">Получить</span><span class="sxs-lookup"><span data-stu-id="41a02-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41a02-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41a02-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="41a02-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41a02-108">DESCRIPTION</span></span>
<span data-ttu-id="41a02-109">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="41a02-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="41a02-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41a02-110">EXAMPLES</span></span>

### <span data-ttu-id="41a02-111">Пример 1. Получить указанную конфигурацию PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="41a02-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="41a02-112">Этот cmdlet получает заданную конфигурацию PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="41a02-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="41a02-113">Пример 2. Список всех конфигураций на указанном сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="41a02-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="41a02-114">Этот cmdlet lists all configurations in specified PostgreSql server.</span><span class="sxs-lookup"><span data-stu-id="41a02-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="41a02-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41a02-115">PARAMETERS</span></span>

### <span data-ttu-id="41a02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a02-116">-DefaultProfile</span></span>
<span data-ttu-id="41a02-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41a02-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41a02-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41a02-118">-InputObject</span></span>
<span data-ttu-id="41a02-119">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="41a02-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="41a02-120">-Name</span><span class="sxs-lookup"><span data-stu-id="41a02-120">-Name</span></span>
<span data-ttu-id="41a02-121">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="41a02-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="41a02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a02-122">-ResourceGroupName</span></span>
<span data-ttu-id="41a02-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41a02-123">The name of the resource group.</span></span>
<span data-ttu-id="41a02-124">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="41a02-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="41a02-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="41a02-125">-ServerName</span></span>
<span data-ttu-id="41a02-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="41a02-126">The name of the server.</span></span>

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

### <span data-ttu-id="41a02-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41a02-127">-SubscriptionId</span></span>
<span data-ttu-id="41a02-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="41a02-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="41a02-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a02-129">CommonParameters</span></span>
<span data-ttu-id="41a02-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a02-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a02-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41a02-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a02-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41a02-132">INPUTS</span></span>

### <span data-ttu-id="41a02-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="41a02-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="41a02-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41a02-134">OUTPUTS</span></span>

### <span data-ttu-id="41a02-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="41a02-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="41a02-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41a02-136">NOTES</span></span>

<span data-ttu-id="41a02-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="41a02-137">ALIASES</span></span>

<span data-ttu-id="41a02-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="41a02-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41a02-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="41a02-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41a02-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41a02-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41a02-141">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="41a02-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41a02-142">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="41a02-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="41a02-143">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="41a02-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="41a02-144">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="41a02-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="41a02-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="41a02-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41a02-146">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="41a02-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="41a02-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41a02-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="41a02-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="41a02-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="41a02-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="41a02-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="41a02-150">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="41a02-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="41a02-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="41a02-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="41a02-152">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="41a02-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="41a02-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41a02-153">RELATED LINKS</span></span>

