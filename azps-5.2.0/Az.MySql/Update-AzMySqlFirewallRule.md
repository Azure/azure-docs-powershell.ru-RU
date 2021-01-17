---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: eb74b9530c9ce196b308a310d5a20642328719e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410919"
---
# <span data-ttu-id="d8942-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8942-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="d8942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8942-102">SYNOPSIS</span></span>
<span data-ttu-id="d8942-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d8942-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d8942-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8942-104">SYNTAX</span></span>

### <span data-ttu-id="d8942-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8942-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8942-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d8942-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8942-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8942-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8942-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d8942-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8942-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8942-109">DESCRIPTION</span></span>
<span data-ttu-id="d8942-110">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d8942-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d8942-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8942-111">EXAMPLES</span></span>

### <span data-ttu-id="d8942-112">Пример 1. Обновление правила брандмауэра MySql по имени</span><span class="sxs-lookup"><span data-stu-id="d8942-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d8942-113">Этот cmdlet обновляет по имени правило брандмауэра MySql.</span><span class="sxs-lookup"><span data-stu-id="d8942-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="d8942-114">Пример 2. Обновление правила брандмауэра MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="d8942-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d8942-115">Эти cmdlets обновляют правило брандмауэра MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="d8942-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="d8942-116">Пример 3. Обновление правила брандмауэра MySql с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d8942-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="d8942-117">Эти cmdlets обновляют правило брандмауэра MySql на clientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d8942-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="d8942-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8942-118">PARAMETERS</span></span>

### <span data-ttu-id="d8942-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8942-119">-AsJob</span></span>
<span data-ttu-id="d8942-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d8942-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d8942-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d8942-121">-ClientIPAddress</span></span>
<span data-ttu-id="d8942-122">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d8942-123">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="d8942-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d8942-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8942-124">-DefaultProfile</span></span>
<span data-ttu-id="d8942-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8942-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8942-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="d8942-126">-EndIPAddress</span></span>
<span data-ttu-id="d8942-127">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d8942-128">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="d8942-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d8942-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8942-129">-InputObject</span></span>
<span data-ttu-id="d8942-130">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d8942-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8942-131">-Name</span><span class="sxs-lookup"><span data-stu-id="d8942-131">-Name</span></span>
<span data-ttu-id="d8942-132">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d8942-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d8942-133">-NoWait</span></span>
<span data-ttu-id="d8942-134">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d8942-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d8942-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8942-135">-ResourceGroupName</span></span>
<span data-ttu-id="d8942-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8942-136">The name of the resource group.</span></span>
<span data-ttu-id="d8942-137">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d8942-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d8942-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8942-138">-ServerName</span></span>
<span data-ttu-id="d8942-139">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-139">The name of the server.</span></span>

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

### <span data-ttu-id="d8942-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d8942-140">-StartIPAddress</span></span>
<span data-ttu-id="d8942-141">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d8942-142">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="d8942-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d8942-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8942-143">-SubscriptionId</span></span>
<span data-ttu-id="d8942-144">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d8942-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d8942-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8942-145">-Confirm</span></span>
<span data-ttu-id="d8942-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8942-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8942-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8942-147">-WhatIf</span></span>
<span data-ttu-id="d8942-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8942-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8942-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d8942-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8942-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8942-150">CommonParameters</span></span>
<span data-ttu-id="d8942-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8942-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8942-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8942-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8942-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8942-153">INPUTS</span></span>

### <span data-ttu-id="d8942-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d8942-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d8942-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8942-155">OUTPUTS</span></span>

### <span data-ttu-id="d8942-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8942-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d8942-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8942-157">NOTES</span></span>

<span data-ttu-id="d8942-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d8942-158">ALIASES</span></span>

<span data-ttu-id="d8942-159">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d8942-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8942-160">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d8942-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8942-161">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8942-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8942-162">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d8942-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8942-163">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d8942-164">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d8942-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d8942-165">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d8942-166">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d8942-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8942-167">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-167">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d8942-168">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="d8942-168">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d8942-169">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8942-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d8942-170">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d8942-170">The name is case insensitive.</span></span>
  - <span data-ttu-id="d8942-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d8942-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d8942-172">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d8942-172">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d8942-173">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d8942-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d8942-174">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="d8942-174">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d8942-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8942-175">RELATED LINKS</span></span>

