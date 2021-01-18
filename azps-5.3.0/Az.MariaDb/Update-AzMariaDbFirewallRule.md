---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507121"
---
# <span data-ttu-id="3671a-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3671a-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="3671a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3671a-102">SYNOPSIS</span></span>
<span data-ttu-id="3671a-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3671a-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3671a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3671a-104">SYNTAX</span></span>

### <span data-ttu-id="3671a-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3671a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3671a-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3671a-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3671a-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3671a-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3671a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3671a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3671a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3671a-109">DESCRIPTION</span></span>
<span data-ttu-id="3671a-110">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3671a-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3671a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3671a-111">EXAMPLES</span></span>

### <span data-ttu-id="3671a-112">Пример 1. Обновление правила брандмауэра MariaDB</span><span class="sxs-lookup"><span data-stu-id="3671a-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="3671a-113">Эта команда обновляет правило брандмауэра MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3671a-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="3671a-114">Пример 2. Обновление правила брандмауэра MariaDB по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="3671a-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="3671a-115">Этот cmdlet обновляет правило брандмауэра MariaDB по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="3671a-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="3671a-116">Пример 3. Обновление правила брандмауэра MariaDB на clientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="3671a-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="3671a-117">Этот cmdlet обновляет правило брандмауэра MariaDB от -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="3671a-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="3671a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3671a-118">PARAMETERS</span></span>

### <span data-ttu-id="3671a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3671a-119">-AsJob</span></span>
<span data-ttu-id="3671a-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3671a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3671a-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3671a-121">-ClientIPAddress</span></span>
<span data-ttu-id="3671a-122">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3671a-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="3671a-123">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="3671a-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3671a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3671a-124">-DefaultProfile</span></span>
<span data-ttu-id="3671a-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3671a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3671a-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="3671a-126">-EndIPAddress</span></span>
<span data-ttu-id="3671a-127">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3671a-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="3671a-128">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="3671a-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3671a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3671a-129">-InputObject</span></span>
<span data-ttu-id="3671a-130">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3671a-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3671a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3671a-131">-Name</span></span>
<span data-ttu-id="3671a-132">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3671a-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="3671a-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3671a-133">-NoWait</span></span>
<span data-ttu-id="3671a-134">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="3671a-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3671a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3671a-135">-ResourceGroupName</span></span>
<span data-ttu-id="3671a-136">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="3671a-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3671a-137">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="3671a-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3671a-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3671a-138">-ServerName</span></span>
<span data-ttu-id="3671a-139">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3671a-139">The name of the server.</span></span>

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

### <span data-ttu-id="3671a-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="3671a-140">-StartIPAddress</span></span>
<span data-ttu-id="3671a-141">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3671a-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="3671a-142">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="3671a-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3671a-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3671a-143">-SubscriptionId</span></span>
<span data-ttu-id="3671a-144">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="3671a-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3671a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3671a-145">-Confirm</span></span>
<span data-ttu-id="3671a-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3671a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3671a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3671a-147">-WhatIf</span></span>
<span data-ttu-id="3671a-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3671a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3671a-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3671a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3671a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3671a-150">CommonParameters</span></span>
<span data-ttu-id="3671a-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3671a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3671a-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3671a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3671a-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3671a-153">INPUTS</span></span>

### <span data-ttu-id="3671a-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="3671a-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="3671a-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3671a-155">OUTPUTS</span></span>

### <span data-ttu-id="3671a-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3671a-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="3671a-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3671a-157">NOTES</span></span>

<span data-ttu-id="3671a-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3671a-158">ALIASES</span></span>

<span data-ttu-id="3671a-159">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3671a-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3671a-160">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3671a-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3671a-161">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3671a-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3671a-162">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="3671a-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3671a-163">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="3671a-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3671a-164">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="3671a-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3671a-165">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3671a-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3671a-166">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="3671a-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3671a-167">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="3671a-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3671a-168">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="3671a-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3671a-169">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="3671a-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3671a-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="3671a-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3671a-171">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3671a-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3671a-172">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="3671a-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="3671a-173">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="3671a-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3671a-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3671a-174">RELATED LINKS</span></span>

