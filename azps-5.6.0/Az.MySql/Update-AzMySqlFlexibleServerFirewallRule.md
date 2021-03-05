---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 2147921826c6f50882345bc68603b0dae8cb26ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968760"
---
# <span data-ttu-id="4e04a-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4e04a-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="4e04a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e04a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e04a-103">Обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4e04a-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="4e04a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e04a-104">SYNTAX</span></span>

### <span data-ttu-id="4e04a-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e04a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e04a-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="4e04a-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e04a-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e04a-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e04a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4e04a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4e04a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e04a-109">DESCRIPTION</span></span>
<span data-ttu-id="4e04a-110">Обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4e04a-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="4e04a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e04a-111">EXAMPLES</span></span>

### <span data-ttu-id="4e04a-112">Пример 1. Обновление правила брандмауэра MySql по имени</span><span class="sxs-lookup"><span data-stu-id="4e04a-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="4e04a-113">Этот cmdlet обновляет по имени правило брандмауэра MySql.</span><span class="sxs-lookup"><span data-stu-id="4e04a-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="4e04a-114">Пример 2. Обновление правила брандмауэра MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="4e04a-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="4e04a-115">Эти cmdlets обновляют правило брандмауэра MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="4e04a-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="4e04a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e04a-116">PARAMETERS</span></span>

### <span data-ttu-id="4e04a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e04a-117">-AsJob</span></span>
<span data-ttu-id="4e04a-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4e04a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="4e04a-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="4e04a-119">-ClientIPAddress</span></span>
<span data-ttu-id="4e04a-120">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="4e04a-121">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="4e04a-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4e04a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e04a-122">-DefaultProfile</span></span>
<span data-ttu-id="4e04a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e04a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e04a-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="4e04a-124">-EndIPAddress</span></span>
<span data-ttu-id="4e04a-125">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="4e04a-126">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="4e04a-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4e04a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e04a-127">-InputObject</span></span>
<span data-ttu-id="4e04a-128">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="4e04a-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e04a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4e04a-129">-Name</span></span>
<span data-ttu-id="4e04a-130">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="4e04a-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4e04a-131">-NoWait</span></span>
<span data-ttu-id="4e04a-132">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="4e04a-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e04a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e04a-133">-ResourceGroupName</span></span>
<span data-ttu-id="4e04a-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e04a-134">The name of the resource group.</span></span>
<span data-ttu-id="4e04a-135">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="4e04a-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4e04a-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e04a-136">-ServerName</span></span>
<span data-ttu-id="4e04a-137">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-137">The name of the server.</span></span>

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

### <span data-ttu-id="4e04a-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="4e04a-138">-StartIPAddress</span></span>
<span data-ttu-id="4e04a-139">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="4e04a-140">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="4e04a-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4e04a-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e04a-141">-SubscriptionId</span></span>
<span data-ttu-id="4e04a-142">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="4e04a-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4e04a-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e04a-143">-Confirm</span></span>
<span data-ttu-id="4e04a-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4e04a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e04a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e04a-145">-WhatIf</span></span>
<span data-ttu-id="4e04a-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e04a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e04a-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e04a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e04a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e04a-148">CommonParameters</span></span>
<span data-ttu-id="4e04a-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e04a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e04a-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e04a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e04a-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e04a-151">INPUTS</span></span>

### <span data-ttu-id="4e04a-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4e04a-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4e04a-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e04a-153">OUTPUTS</span></span>

### <span data-ttu-id="4e04a-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4e04a-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="4e04a-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e04a-155">NOTES</span></span>

<span data-ttu-id="4e04a-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4e04a-156">ALIASES</span></span>

<span data-ttu-id="4e04a-157">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4e04a-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e04a-158">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4e04a-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e04a-159">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e04a-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e04a-160">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="4e04a-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e04a-161">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4e04a-162">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e04a-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4e04a-163">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4e04a-164">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="4e04a-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e04a-165">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="4e04a-166">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="4e04a-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4e04a-167">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e04a-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4e04a-168">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="4e04a-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="4e04a-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="4e04a-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4e04a-170">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4e04a-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4e04a-171">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="4e04a-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4e04a-172">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="4e04a-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4e04a-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e04a-173">RELATED LINKS</span></span>

