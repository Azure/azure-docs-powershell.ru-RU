---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 224d60bdeca8b8884be02a716159374f5d0e31c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506198"
---
# <span data-ttu-id="80edd-101">Remove-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="80edd-101">Remove-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="80edd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80edd-102">SYNOPSIS</span></span>
<span data-ttu-id="80edd-103">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="80edd-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="80edd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80edd-104">SYNTAX</span></span>

### <span data-ttu-id="80edd-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80edd-105">Delete (Default)</span></span>
```
Remove-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="80edd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80edd-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80edd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80edd-107">DESCRIPTION</span></span>
<span data-ttu-id="80edd-108">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="80edd-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="80edd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80edd-109">EXAMPLES</span></span>

### <span data-ttu-id="80edd-110">Пример 1. Удаление правила виртуальной сети mySql server по имени</span><span class="sxs-lookup"><span data-stu-id="80edd-110">Example 1: Remove MySql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest-ServerName mysql-test

```

<span data-ttu-id="80edd-111">Этот cmdlet removes MySql Server Virtual Network Rule by name.</span><span class="sxs-lookup"><span data-stu-id="80edd-111">This cmdlet removes MySql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="80edd-112">Пример 2. Удаление виртуальных сетевых правил mySql server по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="80edd-112">Example 2: Remove MySql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Remove-AzMySqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="80edd-113">Эти cmdlets remove MySql Server Virtual Network Rule by identity.</span><span class="sxs-lookup"><span data-stu-id="80edd-113">These cmdlets remove MySql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="80edd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80edd-114">PARAMETERS</span></span>

### <span data-ttu-id="80edd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80edd-115">-AsJob</span></span>
<span data-ttu-id="80edd-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="80edd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="80edd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80edd-117">-DefaultProfile</span></span>
<span data-ttu-id="80edd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80edd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80edd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80edd-119">-InputObject</span></span>
<span data-ttu-id="80edd-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="80edd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80edd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="80edd-121">-Name</span></span>
<span data-ttu-id="80edd-122">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="80edd-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80edd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="80edd-123">-NoWait</span></span>
<span data-ttu-id="80edd-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="80edd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80edd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80edd-125">-PassThru</span></span>
<span data-ttu-id="80edd-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="80edd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80edd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80edd-127">-ResourceGroupName</span></span>
<span data-ttu-id="80edd-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80edd-128">The name of the resource group.</span></span>
<span data-ttu-id="80edd-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="80edd-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="80edd-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80edd-130">-ServerName</span></span>
<span data-ttu-id="80edd-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="80edd-131">The name of the server.</span></span>

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

### <span data-ttu-id="80edd-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80edd-132">-SubscriptionId</span></span>
<span data-ttu-id="80edd-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="80edd-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="80edd-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80edd-134">-Confirm</span></span>
<span data-ttu-id="80edd-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="80edd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80edd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80edd-136">-WhatIf</span></span>
<span data-ttu-id="80edd-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80edd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80edd-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="80edd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80edd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80edd-139">CommonParameters</span></span>
<span data-ttu-id="80edd-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80edd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80edd-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80edd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80edd-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80edd-142">INPUTS</span></span>

### <span data-ttu-id="80edd-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="80edd-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="80edd-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80edd-144">OUTPUTS</span></span>

### <span data-ttu-id="80edd-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="80edd-145">System.Boolean</span></span>

## <span data-ttu-id="80edd-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80edd-146">NOTES</span></span>

<span data-ttu-id="80edd-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="80edd-147">ALIASES</span></span>

<span data-ttu-id="80edd-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="80edd-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80edd-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="80edd-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80edd-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80edd-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80edd-151">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="80edd-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80edd-152">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="80edd-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="80edd-153">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="80edd-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="80edd-154">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="80edd-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="80edd-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="80edd-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80edd-156">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="80edd-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="80edd-157">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="80edd-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="80edd-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80edd-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="80edd-159">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="80edd-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="80edd-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="80edd-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="80edd-161">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="80edd-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="80edd-162">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="80edd-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="80edd-163">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="80edd-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="80edd-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80edd-164">RELATED LINKS</span></span>

