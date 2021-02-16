---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 82945caa08fb102c0ef5a05e95586f9c66d3d4a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218057"
---
# <span data-ttu-id="6a964-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a964-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="6a964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a964-102">SYNOPSIS</span></span>
<span data-ttu-id="6a964-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="6a964-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="6a964-104">Используйте Update-AzPostgreSqlFlexibleServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="6a964-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6a964-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a964-105">SYNTAX</span></span>

### <span data-ttu-id="6a964-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a964-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a964-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a964-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a964-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a964-108">DESCRIPTION</span></span>
<span data-ttu-id="6a964-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="6a964-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="6a964-110">Используйте Update-AzPostgreSqlFlexibleServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="6a964-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6a964-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a964-111">EXAMPLES</span></span>

### <span data-ttu-id="6a964-112">Пример 1. Updatae указанной конфигурации PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="6a964-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="6a964-113">Этот cmdlet обновляет конфигурацию PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="6a964-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="6a964-114">Пример 1. Updatae, заданная конфигурацией PostgreSql по удостоверению</span><span class="sxs-lookup"><span data-stu-id="6a964-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="6a964-115">Этот cmdlet обновляет конфигурацию PostgreSql по удостоверению.</span><span class="sxs-lookup"><span data-stu-id="6a964-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="6a964-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a964-116">PARAMETERS</span></span>

### <span data-ttu-id="6a964-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a964-117">-AsJob</span></span>
<span data-ttu-id="6a964-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="6a964-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a964-119">-DefaultProfile</span></span>
<span data-ttu-id="6a964-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a964-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a964-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a964-121">-InputObject</span></span>
<span data-ttu-id="6a964-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="6a964-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6a964-123">-Name</span></span>
<span data-ttu-id="6a964-124">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="6a964-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6a964-125">-NoWait</span></span>
<span data-ttu-id="6a964-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="6a964-126">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a964-127">-ResourceGroupName</span></span>
<span data-ttu-id="6a964-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a964-128">The name of the resource group.</span></span>
<span data-ttu-id="6a964-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="6a964-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6a964-130">-ServerName</span></span>
<span data-ttu-id="6a964-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6a964-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-132">-Source</span><span class="sxs-lookup"><span data-stu-id="6a964-132">-Source</span></span>
<span data-ttu-id="6a964-133">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6a964-133">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a964-134">-SubscriptionId</span></span>
<span data-ttu-id="6a964-135">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6a964-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-136">-Значение</span><span class="sxs-lookup"><span data-stu-id="6a964-136">-Value</span></span>
<span data-ttu-id="6a964-137">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6a964-137">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a964-138">-Confirm</span></span>
<span data-ttu-id="6a964-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6a964-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a964-140">-WhatIf</span></span>
<span data-ttu-id="6a964-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a964-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a964-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6a964-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a964-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a964-143">CommonParameters</span></span>
<span data-ttu-id="6a964-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a964-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a964-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a964-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a964-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a964-146">INPUTS</span></span>

### <span data-ttu-id="6a964-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6a964-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6a964-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a964-148">OUTPUTS</span></span>

### <span data-ttu-id="6a964-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="6a964-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="6a964-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a964-150">NOTES</span></span>

<span data-ttu-id="6a964-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6a964-151">ALIASES</span></span>

<span data-ttu-id="6a964-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6a964-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a964-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="6a964-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a964-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a964-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a964-155">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="6a964-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a964-156">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="6a964-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6a964-157">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6a964-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6a964-158">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="6a964-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6a964-159">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="6a964-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a964-160">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="6a964-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6a964-161">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a964-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6a964-162">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="6a964-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="6a964-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6a964-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6a964-164">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6a964-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6a964-165">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6a964-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6a964-166">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="6a964-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6a964-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a964-167">RELATED LINKS</span></span>

