---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: fe6ef1a5193119c4778d18c39a7ecff98354cf89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240312"
---
# <span data-ttu-id="ef048-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ef048-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="ef048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef048-102">SYNOPSIS</span></span>
<span data-ttu-id="ef048-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ef048-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="ef048-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef048-104">SYNTAX</span></span>

### <span data-ttu-id="ef048-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef048-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ef048-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ef048-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ef048-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ef048-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ef048-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ef048-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ef048-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef048-109">DESCRIPTION</span></span>
<span data-ttu-id="ef048-110">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ef048-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="ef048-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef048-111">EXAMPLES</span></span>

### <span data-ttu-id="ef048-112">Пример 1. Обновление правила брандмауэра PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="ef048-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="ef048-113">Этот cmdlet обновляет по имени правило брандмауэра PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="ef048-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="ef048-114">Пример 2. Обновление правила брандмауэра PostgreSql с помощью удостоверений.</span><span class="sxs-lookup"><span data-stu-id="ef048-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="ef048-115">Эти cmdlets обновляют правило брандмауэра PostgreSql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="ef048-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="ef048-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef048-116">PARAMETERS</span></span>

### <span data-ttu-id="ef048-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef048-117">-AsJob</span></span>
<span data-ttu-id="ef048-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ef048-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ef048-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ef048-119">-ClientIPAddress</span></span>
<span data-ttu-id="ef048-120">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="ef048-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="ef048-121">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="ef048-121">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef048-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef048-122">-DefaultProfile</span></span>
<span data-ttu-id="ef048-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef048-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef048-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="ef048-124">-EndIPAddress</span></span>
<span data-ttu-id="ef048-125">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="ef048-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="ef048-126">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="ef048-126">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef048-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef048-127">-InputObject</span></span>
<span data-ttu-id="ef048-128">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ef048-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef048-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ef048-129">-Name</span></span>
<span data-ttu-id="ef048-130">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="ef048-130">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef048-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ef048-131">-NoWait</span></span>
<span data-ttu-id="ef048-132">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ef048-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ef048-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef048-133">-ResourceGroupName</span></span>
<span data-ttu-id="ef048-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef048-134">The name of the resource group.</span></span>
<span data-ttu-id="ef048-135">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ef048-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef048-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ef048-136">-ServerName</span></span>
<span data-ttu-id="ef048-137">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ef048-137">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef048-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="ef048-138">-StartIPAddress</span></span>
<span data-ttu-id="ef048-139">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="ef048-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="ef048-140">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="ef048-140">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef048-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef048-141">-SubscriptionId</span></span>
<span data-ttu-id="ef048-142">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ef048-142">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef048-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef048-143">-Confirm</span></span>
<span data-ttu-id="ef048-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ef048-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef048-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef048-145">-WhatIf</span></span>
<span data-ttu-id="ef048-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef048-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef048-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ef048-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef048-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef048-148">CommonParameters</span></span>
<span data-ttu-id="ef048-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef048-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef048-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef048-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef048-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef048-151">INPUTS</span></span>

### <span data-ttu-id="ef048-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ef048-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="ef048-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef048-153">OUTPUTS</span></span>

### <span data-ttu-id="ef048-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ef048-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="ef048-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef048-155">NOTES</span></span>

<span data-ttu-id="ef048-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ef048-156">ALIASES</span></span>

<span data-ttu-id="ef048-157">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ef048-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef048-158">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ef048-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef048-159">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef048-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef048-160">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ef048-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef048-161">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="ef048-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ef048-162">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ef048-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ef048-163">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="ef048-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ef048-164">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ef048-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef048-165">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="ef048-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ef048-166">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef048-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ef048-167">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ef048-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="ef048-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ef048-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ef048-169">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ef048-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ef048-170">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ef048-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ef048-171">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="ef048-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ef048-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef048-172">RELATED LINKS</span></span>

