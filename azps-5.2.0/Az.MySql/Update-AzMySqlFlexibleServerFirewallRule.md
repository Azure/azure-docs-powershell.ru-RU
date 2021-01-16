---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410892"
---
# <span data-ttu-id="97746-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="97746-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="97746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97746-102">SYNOPSIS</span></span>
<span data-ttu-id="97746-103">Обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="97746-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="97746-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97746-104">SYNTAX</span></span>

### <span data-ttu-id="97746-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97746-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97746-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="97746-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97746-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97746-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97746-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="97746-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="97746-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97746-109">DESCRIPTION</span></span>
<span data-ttu-id="97746-110">Обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="97746-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="97746-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97746-111">EXAMPLES</span></span>

### <span data-ttu-id="97746-112">Пример 1. Обновление правила брандмауэра MySql по имени</span><span class="sxs-lookup"><span data-stu-id="97746-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="97746-113">Этот cmdlet обновляет по имени правило брандмауэра MySql.</span><span class="sxs-lookup"><span data-stu-id="97746-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="97746-114">Пример 2. Обновление правила брандмауэра MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="97746-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="97746-115">Эти cmdlets обновляют правило брандмауэра MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="97746-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="97746-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97746-116">PARAMETERS</span></span>

### <span data-ttu-id="97746-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97746-117">-AsJob</span></span>
<span data-ttu-id="97746-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="97746-118">Run the command as a job</span></span>

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

### <span data-ttu-id="97746-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="97746-119">-ClientIPAddress</span></span>
<span data-ttu-id="97746-120">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="97746-121">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="97746-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="97746-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97746-122">-DefaultProfile</span></span>
<span data-ttu-id="97746-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97746-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97746-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="97746-124">-EndIPAddress</span></span>
<span data-ttu-id="97746-125">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="97746-126">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="97746-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="97746-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97746-127">-InputObject</span></span>
<span data-ttu-id="97746-128">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="97746-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97746-129">-Name</span><span class="sxs-lookup"><span data-stu-id="97746-129">-Name</span></span>
<span data-ttu-id="97746-130">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="97746-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="97746-131">-NoWait</span></span>
<span data-ttu-id="97746-132">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="97746-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="97746-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97746-133">-ResourceGroupName</span></span>
<span data-ttu-id="97746-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97746-134">The name of the resource group.</span></span>
<span data-ttu-id="97746-135">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="97746-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="97746-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97746-136">-ServerName</span></span>
<span data-ttu-id="97746-137">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-137">The name of the server.</span></span>

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

### <span data-ttu-id="97746-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="97746-138">-StartIPAddress</span></span>
<span data-ttu-id="97746-139">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="97746-140">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="97746-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="97746-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97746-141">-SubscriptionId</span></span>
<span data-ttu-id="97746-142">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="97746-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="97746-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97746-143">-Confirm</span></span>
<span data-ttu-id="97746-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97746-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97746-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97746-145">-WhatIf</span></span>
<span data-ttu-id="97746-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97746-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97746-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="97746-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97746-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97746-148">CommonParameters</span></span>
<span data-ttu-id="97746-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97746-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97746-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97746-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97746-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97746-151">INPUTS</span></span>

### <span data-ttu-id="97746-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="97746-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="97746-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97746-153">OUTPUTS</span></span>

### <span data-ttu-id="97746-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="97746-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="97746-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97746-155">NOTES</span></span>

<span data-ttu-id="97746-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97746-156">ALIASES</span></span>

<span data-ttu-id="97746-157">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="97746-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97746-158">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="97746-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97746-159">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97746-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97746-160">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="97746-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97746-161">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="97746-162">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="97746-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="97746-163">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="97746-164">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="97746-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97746-165">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="97746-166">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="97746-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="97746-167">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97746-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="97746-168">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="97746-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="97746-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="97746-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="97746-170">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="97746-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="97746-171">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="97746-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="97746-172">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="97746-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="97746-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97746-173">RELATED LINKS</span></span>
