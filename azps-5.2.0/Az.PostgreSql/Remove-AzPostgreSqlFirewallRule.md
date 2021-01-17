---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391916"
---
# <span data-ttu-id="38ee9-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="38ee9-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="38ee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="38ee9-103">Удаляет правило брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="38ee9-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="38ee9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38ee9-104">SYNTAX</span></span>

### <span data-ttu-id="38ee9-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38ee9-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="38ee9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38ee9-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38ee9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38ee9-107">DESCRIPTION</span></span>
<span data-ttu-id="38ee9-108">Удаляет правило брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="38ee9-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="38ee9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38ee9-109">EXAMPLES</span></span>

### <span data-ttu-id="38ee9-110">Пример 1. Удаление правила брандмауэра PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="38ee9-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="38ee9-111">Этот cmdlet удаляет правило брандмауэра PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="38ee9-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="38ee9-112">Пример 2. Удаление правила брандмауэра PostgreSql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="38ee9-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="38ee9-113">Эти cmdlets remove PostgreSql Firewall Rule by identity.</span><span class="sxs-lookup"><span data-stu-id="38ee9-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="38ee9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38ee9-114">PARAMETERS</span></span>

### <span data-ttu-id="38ee9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38ee9-115">-AsJob</span></span>
<span data-ttu-id="38ee9-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="38ee9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="38ee9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ee9-117">-DefaultProfile</span></span>
<span data-ttu-id="38ee9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38ee9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ee9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38ee9-119">-InputObject</span></span>
<span data-ttu-id="38ee9-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="38ee9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="38ee9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="38ee9-121">-Name</span></span>
<span data-ttu-id="38ee9-122">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="38ee9-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="38ee9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="38ee9-123">-NoWait</span></span>
<span data-ttu-id="38ee9-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="38ee9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="38ee9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38ee9-125">-PassThru</span></span>
<span data-ttu-id="38ee9-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="38ee9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="38ee9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ee9-127">-ResourceGroupName</span></span>
<span data-ttu-id="38ee9-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38ee9-128">The name of the resource group.</span></span>
<span data-ttu-id="38ee9-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="38ee9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="38ee9-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38ee9-130">-ServerName</span></span>
<span data-ttu-id="38ee9-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="38ee9-131">The name of the server.</span></span>

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

### <span data-ttu-id="38ee9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38ee9-132">-SubscriptionId</span></span>
<span data-ttu-id="38ee9-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="38ee9-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="38ee9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38ee9-134">-Confirm</span></span>
<span data-ttu-id="38ee9-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="38ee9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ee9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ee9-136">-WhatIf</span></span>
<span data-ttu-id="38ee9-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ee9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ee9-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38ee9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ee9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ee9-139">CommonParameters</span></span>
<span data-ttu-id="38ee9-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ee9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ee9-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38ee9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ee9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38ee9-142">INPUTS</span></span>

### <span data-ttu-id="38ee9-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="38ee9-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="38ee9-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38ee9-144">OUTPUTS</span></span>

### <span data-ttu-id="38ee9-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38ee9-145">System.Boolean</span></span>

## <span data-ttu-id="38ee9-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38ee9-146">NOTES</span></span>

<span data-ttu-id="38ee9-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="38ee9-147">ALIASES</span></span>

<span data-ttu-id="38ee9-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="38ee9-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38ee9-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="38ee9-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38ee9-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38ee9-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38ee9-151">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="38ee9-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38ee9-152">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="38ee9-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="38ee9-153">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="38ee9-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="38ee9-154">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="38ee9-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="38ee9-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="38ee9-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38ee9-156">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="38ee9-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="38ee9-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38ee9-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="38ee9-158">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="38ee9-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="38ee9-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="38ee9-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="38ee9-160">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="38ee9-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="38ee9-161">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="38ee9-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="38ee9-162">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="38ee9-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="38ee9-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38ee9-163">RELATED LINKS</span></span>

