---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 98e476b2a1732d2c984d200265d817c3ff6d71a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968787"
---
# <span data-ttu-id="ed1aa-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed1aa-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="ed1aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1aa-103">Обновляет сведения о конфигурации гибкого сервера MySQL.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="ed1aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed1aa-104">SYNTAX</span></span>

### <span data-ttu-id="ed1aa-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed1aa-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed1aa-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ed1aa-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed1aa-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-107">DESCRIPTION</span></span>
<span data-ttu-id="ed1aa-108">Обновляет сведения о конфигурации гибкого сервера MySQL.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="ed1aa-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-109">EXAMPLES</span></span>

### <span data-ttu-id="ed1aa-110">Пример 1. Обновление конфигурации MySql по имени</span><span class="sxs-lookup"><span data-stu-id="ed1aa-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="ed1aa-111">Этот cmdlet обновляет конфигурацию MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="ed1aa-112">Пример 2. Обновление конфигурации MySql с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="ed1aa-113">Эти cmdlets обновляют конфигурацию MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="ed1aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed1aa-114">PARAMETERS</span></span>

### <span data-ttu-id="ed1aa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed1aa-115">-AsJob</span></span>
<span data-ttu-id="ed1aa-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ed1aa-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ed1aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1aa-117">-DefaultProfile</span></span>
<span data-ttu-id="ed1aa-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed1aa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed1aa-119">-InputObject</span></span>
<span data-ttu-id="ed1aa-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed1aa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ed1aa-121">-Name</span></span>
<span data-ttu-id="ed1aa-122">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="ed1aa-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed1aa-123">-NoWait</span></span>
<span data-ttu-id="ed1aa-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ed1aa-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed1aa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed1aa-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed1aa-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-126">The name of the resource group.</span></span>
<span data-ttu-id="ed1aa-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ed1aa-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed1aa-128">-ServerName</span></span>
<span data-ttu-id="ed1aa-129">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-129">The name of the server.</span></span>

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

### <span data-ttu-id="ed1aa-130">-Source</span><span class="sxs-lookup"><span data-stu-id="ed1aa-130">-Source</span></span>
<span data-ttu-id="ed1aa-131">Источник обновляемого значения.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-131">The source of the updating value.</span></span>
<span data-ttu-id="ed1aa-132">Значение по умолчанию переопределяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-132">The default value is user-override</span></span>

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

### <span data-ttu-id="ed1aa-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed1aa-133">-SubscriptionId</span></span>
<span data-ttu-id="ed1aa-134">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ed1aa-135">-Value</span><span class="sxs-lookup"><span data-stu-id="ed1aa-135">-Value</span></span>
<span data-ttu-id="ed1aa-136">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="ed1aa-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed1aa-137">-Confirm</span></span>
<span data-ttu-id="ed1aa-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed1aa-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed1aa-139">-WhatIf</span></span>
<span data-ttu-id="ed1aa-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed1aa-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed1aa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1aa-142">CommonParameters</span></span>
<span data-ttu-id="ed1aa-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1aa-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed1aa-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1aa-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed1aa-145">INPUTS</span></span>

### <span data-ttu-id="ed1aa-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ed1aa-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ed1aa-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed1aa-147">OUTPUTS</span></span>

### <span data-ttu-id="ed1aa-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ed1aa-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="ed1aa-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-149">NOTES</span></span>

<span data-ttu-id="ed1aa-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ed1aa-150">ALIASES</span></span>

<span data-ttu-id="ed1aa-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed1aa-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed1aa-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed1aa-154">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ed1aa-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ed1aa-155">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ed1aa-156">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ed1aa-157">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ed1aa-158">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ed1aa-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ed1aa-159">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ed1aa-160">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ed1aa-161">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ed1aa-162">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="ed1aa-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ed1aa-164">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ed1aa-165">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ed1aa-166">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ed1aa-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-167">RELATED LINKS</span></span>

