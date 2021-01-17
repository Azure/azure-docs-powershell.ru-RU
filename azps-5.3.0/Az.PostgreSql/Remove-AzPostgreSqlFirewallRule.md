---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421284"
---
# <span data-ttu-id="7a8e2-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a8e2-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="7a8e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8e2-103">Удаляет правило брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="7a8e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a8e2-104">SYNTAX</span></span>

### <span data-ttu-id="7a8e2-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a8e2-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7a8e2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7a8e2-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a8e2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a8e2-107">DESCRIPTION</span></span>
<span data-ttu-id="7a8e2-108">Удаляет правило брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="7a8e2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a8e2-109">EXAMPLES</span></span>

### <span data-ttu-id="7a8e2-110">Пример 1. Удаление правила брандмауэра PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="7a8e2-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="7a8e2-111">Этот cmdlet удаляет правило брандмауэра PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="7a8e2-112">Пример 2. Удаление правила брандмауэра PostgreSql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="7a8e2-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="7a8e2-113">Эти cmdlets remove PostgreSql Firewall Rule by identity.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="7a8e2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a8e2-114">PARAMETERS</span></span>

### <span data-ttu-id="7a8e2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a8e2-115">-AsJob</span></span>
<span data-ttu-id="7a8e2-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="7a8e2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7a8e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8e2-117">-DefaultProfile</span></span>
<span data-ttu-id="7a8e2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a8e2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a8e2-119">-InputObject</span></span>
<span data-ttu-id="7a8e2-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8e2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7a8e2-121">-Name</span></span>
<span data-ttu-id="7a8e2-122">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8e2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7a8e2-123">-NoWait</span></span>
<span data-ttu-id="7a8e2-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="7a8e2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7a8e2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a8e2-125">-PassThru</span></span>
<span data-ttu-id="7a8e2-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7a8e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a8e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a8e2-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-128">The name of the resource group.</span></span>
<span data-ttu-id="7a8e2-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8e2-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a8e2-130">-ServerName</span></span>
<span data-ttu-id="7a8e2-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8e2-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a8e2-132">-SubscriptionId</span></span>
<span data-ttu-id="7a8e2-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8e2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a8e2-134">-Confirm</span></span>
<span data-ttu-id="7a8e2-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a8e2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a8e2-136">-WhatIf</span></span>
<span data-ttu-id="7a8e2-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a8e2-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a8e2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8e2-139">CommonParameters</span></span>
<span data-ttu-id="7a8e2-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8e2-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a8e2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8e2-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a8e2-142">INPUTS</span></span>

### <span data-ttu-id="7a8e2-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7a8e2-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7a8e2-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a8e2-144">OUTPUTS</span></span>

### <span data-ttu-id="7a8e2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a8e2-145">System.Boolean</span></span>

## <span data-ttu-id="7a8e2-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a8e2-146">NOTES</span></span>

<span data-ttu-id="7a8e2-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7a8e2-147">ALIASES</span></span>

<span data-ttu-id="7a8e2-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7a8e2-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a8e2-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a8e2-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a8e2-151">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="7a8e2-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a8e2-152">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7a8e2-153">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7a8e2-154">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7a8e2-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="7a8e2-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a8e2-156">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7a8e2-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7a8e2-158">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="7a8e2-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7a8e2-160">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7a8e2-161">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7a8e2-162">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="7a8e2-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7a8e2-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a8e2-163">RELATED LINKS</span></span>

