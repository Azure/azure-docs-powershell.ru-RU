---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 26f6da2cdbf7d12e4d4927fd14ffc6b58b539bef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974648"
---
# <span data-ttu-id="f91d0-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f91d0-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="f91d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f91d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f91d0-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f91d0-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f91d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f91d0-104">SYNTAX</span></span>

### <span data-ttu-id="f91d0-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f91d0-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f91d0-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f91d0-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f91d0-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f91d0-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f91d0-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f91d0-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f91d0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f91d0-109">DESCRIPTION</span></span>
<span data-ttu-id="f91d0-110">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f91d0-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f91d0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f91d0-111">EXAMPLES</span></span>

### <span data-ttu-id="f91d0-112">Пример 1. Обновление правила брандмауэра PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="f91d0-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="f91d0-113">Этот cmdlet обновляет по имени правило брандмауэра PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="f91d0-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="f91d0-114">Пример 2. Обновление правила брандмауэра PostgreSql с помощью удостоверений.</span><span class="sxs-lookup"><span data-stu-id="f91d0-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="f91d0-115">Эти cmdlets обновляют правило брандмауэра PostgreSql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="f91d0-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="f91d0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f91d0-116">PARAMETERS</span></span>

### <span data-ttu-id="f91d0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f91d0-117">-AsJob</span></span>
<span data-ttu-id="f91d0-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f91d0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="f91d0-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f91d0-119">-ClientIPAddress</span></span>
<span data-ttu-id="f91d0-120">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f91d0-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="f91d0-121">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="f91d0-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f91d0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91d0-122">-DefaultProfile</span></span>
<span data-ttu-id="f91d0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f91d0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f91d0-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="f91d0-124">-EndIPAddress</span></span>
<span data-ttu-id="f91d0-125">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f91d0-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="f91d0-126">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="f91d0-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f91d0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f91d0-127">-InputObject</span></span>
<span data-ttu-id="f91d0-128">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f91d0-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f91d0-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f91d0-129">-Name</span></span>
<span data-ttu-id="f91d0-130">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f91d0-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="f91d0-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f91d0-131">-NoWait</span></span>
<span data-ttu-id="f91d0-132">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="f91d0-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f91d0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91d0-133">-ResourceGroupName</span></span>
<span data-ttu-id="f91d0-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f91d0-134">The name of the resource group.</span></span>
<span data-ttu-id="f91d0-135">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="f91d0-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f91d0-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f91d0-136">-ServerName</span></span>
<span data-ttu-id="f91d0-137">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f91d0-137">The name of the server.</span></span>

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

### <span data-ttu-id="f91d0-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="f91d0-138">-StartIPAddress</span></span>
<span data-ttu-id="f91d0-139">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f91d0-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="f91d0-140">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="f91d0-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f91d0-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f91d0-141">-SubscriptionId</span></span>
<span data-ttu-id="f91d0-142">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="f91d0-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f91d0-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f91d0-143">-Confirm</span></span>
<span data-ttu-id="f91d0-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f91d0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f91d0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f91d0-145">-WhatIf</span></span>
<span data-ttu-id="f91d0-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f91d0-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f91d0-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f91d0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f91d0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91d0-148">CommonParameters</span></span>
<span data-ttu-id="f91d0-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f91d0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91d0-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f91d0-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91d0-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f91d0-151">INPUTS</span></span>

### <span data-ttu-id="f91d0-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f91d0-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f91d0-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f91d0-153">OUTPUTS</span></span>

### <span data-ttu-id="f91d0-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f91d0-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="f91d0-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f91d0-155">NOTES</span></span>

<span data-ttu-id="f91d0-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f91d0-156">ALIASES</span></span>

<span data-ttu-id="f91d0-157">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f91d0-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f91d0-158">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f91d0-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f91d0-159">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f91d0-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f91d0-160">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="f91d0-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f91d0-161">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="f91d0-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f91d0-162">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f91d0-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f91d0-163">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f91d0-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f91d0-164">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="f91d0-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f91d0-165">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="f91d0-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f91d0-166">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f91d0-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f91d0-167">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="f91d0-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="f91d0-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="f91d0-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f91d0-169">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f91d0-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f91d0-170">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="f91d0-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f91d0-171">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="f91d0-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f91d0-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f91d0-172">RELATED LINKS</span></span>

