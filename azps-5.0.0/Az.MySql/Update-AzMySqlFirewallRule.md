---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249388"
---
# <span data-ttu-id="d493b-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d493b-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="d493b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d493b-102">SYNOPSIS</span></span>
<span data-ttu-id="d493b-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d493b-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d493b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d493b-104">SYNTAX</span></span>

### <span data-ttu-id="d493b-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d493b-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d493b-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d493b-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d493b-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d493b-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d493b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d493b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d493b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d493b-109">DESCRIPTION</span></span>
<span data-ttu-id="d493b-110">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d493b-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d493b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d493b-111">EXAMPLES</span></span>

### <span data-ttu-id="d493b-112">Пример 1: обновление правила брандмауэра MySql по имени</span><span class="sxs-lookup"><span data-stu-id="d493b-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d493b-113">Этот командлет обновляет правило брандмауэра MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="d493b-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="d493b-114">Пример 2. Обновите правило брандмауэра MySql по удостоверению.</span><span class="sxs-lookup"><span data-stu-id="d493b-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d493b-115">Эти командлеты обновляют правило брандмауэра MySql по идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="d493b-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="d493b-116">Пример 3: обновление правила брандмауэра MySql по-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d493b-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="d493b-117">Эти командлеты обновляют правило брандмауэра MySql по-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d493b-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="d493b-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d493b-118">PARAMETERS</span></span>

### <span data-ttu-id="d493b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d493b-119">-AsJob</span></span>
<span data-ttu-id="d493b-120">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d493b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d493b-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d493b-121">-ClientIPAddress</span></span>
<span data-ttu-id="d493b-122">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d493b-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d493b-123">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="d493b-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d493b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d493b-124">-DefaultProfile</span></span>
<span data-ttu-id="d493b-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d493b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d493b-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="d493b-126">-EndIPAddress</span></span>
<span data-ttu-id="d493b-127">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d493b-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d493b-128">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="d493b-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d493b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d493b-129">-InputObject</span></span>
<span data-ttu-id="d493b-130">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d493b-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d493b-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d493b-131">-Name</span></span>
<span data-ttu-id="d493b-132">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d493b-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d493b-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="d493b-133">-NoWait</span></span>
<span data-ttu-id="d493b-134">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d493b-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d493b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d493b-135">-ResourceGroupName</span></span>
<span data-ttu-id="d493b-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d493b-136">The name of the resource group.</span></span>
<span data-ttu-id="d493b-137">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d493b-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d493b-138">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d493b-138">-ServerName</span></span>
<span data-ttu-id="d493b-139">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d493b-139">The name of the server.</span></span>

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

### <span data-ttu-id="d493b-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d493b-140">-StartIPAddress</span></span>
<span data-ttu-id="d493b-141">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d493b-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d493b-142">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="d493b-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d493b-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d493b-143">-SubscriptionId</span></span>
<span data-ttu-id="d493b-144">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d493b-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d493b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d493b-145">-Confirm</span></span>
<span data-ttu-id="d493b-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d493b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d493b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d493b-147">-WhatIf</span></span>
<span data-ttu-id="d493b-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d493b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d493b-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d493b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d493b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d493b-150">CommonParameters</span></span>
<span data-ttu-id="d493b-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d493b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d493b-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d493b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d493b-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d493b-153">INPUTS</span></span>

### <span data-ttu-id="d493b-154">Microsoft. Azure. PowerShell. командлеты. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d493b-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d493b-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d493b-155">OUTPUTS</span></span>

### <span data-ttu-id="d493b-156">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d493b-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d493b-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="d493b-157">NOTES</span></span>

<span data-ttu-id="d493b-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d493b-158">ALIASES</span></span>

<span data-ttu-id="d493b-159">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d493b-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d493b-160">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d493b-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d493b-161">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d493b-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d493b-162">INPUTOBJECT <IMySqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d493b-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d493b-163">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d493b-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d493b-164">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d493b-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d493b-165">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d493b-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d493b-166">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d493b-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d493b-167">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="d493b-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d493b-168">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d493b-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d493b-169">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d493b-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="d493b-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d493b-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d493b-171">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d493b-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d493b-172">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d493b-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d493b-173">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d493b-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d493b-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d493b-174">RELATED LINKS</span></span>

