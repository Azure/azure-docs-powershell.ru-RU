---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250091"
---
# <span data-ttu-id="d153c-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d153c-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="d153c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d153c-102">SYNOPSIS</span></span>
<span data-ttu-id="d153c-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d153c-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d153c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d153c-104">SYNTAX</span></span>

### <span data-ttu-id="d153c-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d153c-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d153c-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d153c-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d153c-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d153c-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d153c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d153c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d153c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d153c-109">DESCRIPTION</span></span>
<span data-ttu-id="d153c-110">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d153c-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d153c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d153c-111">EXAMPLES</span></span>

### <span data-ttu-id="d153c-112">Пример 1: обновление правила брандмауэра MariaDB</span><span class="sxs-lookup"><span data-stu-id="d153c-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="d153c-113">Эта команда обновляет правило брандмауэра MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d153c-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="d153c-114">Пример 2: обновление правила брандмауэра MariaDB по удостоверению.</span><span class="sxs-lookup"><span data-stu-id="d153c-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d153c-115">Командлет обновляет MariaDB правило межсетевого экрана с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="d153c-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="d153c-116">Пример 3: обновление правила брандмауэра MariaDB на ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d153c-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="d153c-117">Командлет обновляет MariaDB правило брандмауэра на ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d153c-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="d153c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d153c-118">PARAMETERS</span></span>

### <span data-ttu-id="d153c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d153c-119">-AsJob</span></span>
<span data-ttu-id="d153c-120">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d153c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d153c-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d153c-121">-ClientIPAddress</span></span>
<span data-ttu-id="d153c-122">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d153c-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d153c-123">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="d153c-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d153c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d153c-124">-DefaultProfile</span></span>
<span data-ttu-id="d153c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d153c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d153c-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="d153c-126">-EndIPAddress</span></span>
<span data-ttu-id="d153c-127">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d153c-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d153c-128">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="d153c-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d153c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d153c-129">-InputObject</span></span>
<span data-ttu-id="d153c-130">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d153c-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d153c-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d153c-131">-Name</span></span>
<span data-ttu-id="d153c-132">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d153c-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d153c-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="d153c-133">-NoWait</span></span>
<span data-ttu-id="d153c-134">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d153c-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d153c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d153c-135">-ResourceGroupName</span></span>
<span data-ttu-id="d153c-136">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="d153c-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d153c-137">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d153c-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d153c-138">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d153c-138">-ServerName</span></span>
<span data-ttu-id="d153c-139">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d153c-139">The name of the server.</span></span>

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

### <span data-ttu-id="d153c-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d153c-140">-StartIPAddress</span></span>
<span data-ttu-id="d153c-141">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d153c-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d153c-142">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="d153c-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d153c-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d153c-143">-SubscriptionId</span></span>
<span data-ttu-id="d153c-144">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="d153c-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d153c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d153c-145">-Confirm</span></span>
<span data-ttu-id="d153c-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d153c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d153c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d153c-147">-WhatIf</span></span>
<span data-ttu-id="d153c-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d153c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d153c-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d153c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d153c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d153c-150">CommonParameters</span></span>
<span data-ttu-id="d153c-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d153c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d153c-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d153c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d153c-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d153c-153">INPUTS</span></span>

### <span data-ttu-id="d153c-154">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d153c-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d153c-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d153c-155">OUTPUTS</span></span>

### <span data-ttu-id="d153c-156">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d153c-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="d153c-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="d153c-157">NOTES</span></span>

<span data-ttu-id="d153c-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d153c-158">ALIASES</span></span>

<span data-ttu-id="d153c-159">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d153c-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d153c-160">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d153c-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d153c-161">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d153c-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d153c-162">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d153c-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d153c-163">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d153c-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d153c-164">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d153c-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d153c-165">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d153c-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d153c-166">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d153c-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d153c-167">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="d153c-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d153c-168">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="d153c-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d153c-169">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d153c-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d153c-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d153c-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d153c-171">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d153c-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d153c-172">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="d153c-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d153c-173">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d153c-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d153c-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d153c-174">RELATED LINKS</span></span>

