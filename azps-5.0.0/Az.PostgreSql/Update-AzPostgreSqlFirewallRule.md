---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248067"
---
# <span data-ttu-id="76a43-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="76a43-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="76a43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76a43-102">SYNOPSIS</span></span>
<span data-ttu-id="76a43-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="76a43-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="76a43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76a43-104">SYNTAX</span></span>

### <span data-ttu-id="76a43-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76a43-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76a43-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="76a43-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76a43-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76a43-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76a43-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76a43-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="76a43-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a43-109">DESCRIPTION</span></span>
<span data-ttu-id="76a43-110">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="76a43-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="76a43-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76a43-111">EXAMPLES</span></span>

### <span data-ttu-id="76a43-112">Пример 1: обновление правила брандмауэра PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="76a43-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="76a43-113">Этот командлет обновляет PostgreSql правило брандмауэра по имени.</span><span class="sxs-lookup"><span data-stu-id="76a43-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="76a43-114">Пример 2: обновление правила брандмауэра PostgreSql по удостоверению.</span><span class="sxs-lookup"><span data-stu-id="76a43-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="76a43-115">Эти командлеты обновляют PostgreSql правило брандмауэра с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="76a43-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="76a43-116">Пример 3: обновление правила брандмауэра PostgreSql на ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="76a43-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="76a43-117">Эти командлеты обновляют PostgreSql правило брандмауэра на ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="76a43-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="76a43-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76a43-118">PARAMETERS</span></span>

### <span data-ttu-id="76a43-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76a43-119">-AsJob</span></span>
<span data-ttu-id="76a43-120">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="76a43-120">Run the command as a job</span></span>

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

### <span data-ttu-id="76a43-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="76a43-121">-ClientIPAddress</span></span>
<span data-ttu-id="76a43-122">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="76a43-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="76a43-123">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="76a43-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="76a43-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a43-124">-DefaultProfile</span></span>
<span data-ttu-id="76a43-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76a43-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a43-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="76a43-126">-EndIPAddress</span></span>
<span data-ttu-id="76a43-127">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="76a43-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="76a43-128">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="76a43-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="76a43-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76a43-129">-InputObject</span></span>
<span data-ttu-id="76a43-130">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="76a43-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76a43-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76a43-131">-Name</span></span>
<span data-ttu-id="76a43-132">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="76a43-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="76a43-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="76a43-133">-NoWait</span></span>
<span data-ttu-id="76a43-134">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="76a43-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76a43-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a43-135">-ResourceGroupName</span></span>
<span data-ttu-id="76a43-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76a43-136">The name of the resource group.</span></span>
<span data-ttu-id="76a43-137">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="76a43-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="76a43-138">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="76a43-138">-ServerName</span></span>
<span data-ttu-id="76a43-139">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="76a43-139">The name of the server.</span></span>

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

### <span data-ttu-id="76a43-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="76a43-140">-StartIPAddress</span></span>
<span data-ttu-id="76a43-141">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="76a43-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="76a43-142">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="76a43-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="76a43-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76a43-143">-SubscriptionId</span></span>
<span data-ttu-id="76a43-144">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="76a43-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="76a43-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76a43-145">-Confirm</span></span>
<span data-ttu-id="76a43-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76a43-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a43-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a43-147">-WhatIf</span></span>
<span data-ttu-id="76a43-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76a43-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a43-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76a43-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76a43-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a43-150">CommonParameters</span></span>
<span data-ttu-id="76a43-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76a43-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a43-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76a43-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a43-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76a43-153">INPUTS</span></span>

### <span data-ttu-id="76a43-154">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="76a43-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="76a43-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a43-155">OUTPUTS</span></span>

### <span data-ttu-id="76a43-156">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="76a43-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="76a43-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="76a43-157">NOTES</span></span>

<span data-ttu-id="76a43-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="76a43-158">ALIASES</span></span>

<span data-ttu-id="76a43-159">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="76a43-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76a43-160">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="76a43-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76a43-161">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76a43-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76a43-162">INPUTOBJECT <IPostgreSqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="76a43-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76a43-163">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="76a43-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="76a43-164">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="76a43-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="76a43-165">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="76a43-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="76a43-166">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="76a43-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76a43-167">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="76a43-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="76a43-168">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76a43-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="76a43-169">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="76a43-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="76a43-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="76a43-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="76a43-171">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="76a43-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="76a43-172">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="76a43-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="76a43-173">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="76a43-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="76a43-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76a43-174">RELATED LINKS</span></span>

