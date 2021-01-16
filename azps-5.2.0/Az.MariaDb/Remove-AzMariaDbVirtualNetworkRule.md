---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414932"
---
# <span data-ttu-id="64200-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="64200-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="64200-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64200-102">SYNOPSIS</span></span>
<span data-ttu-id="64200-103">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="64200-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="64200-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64200-104">SYNTAX</span></span>

### <span data-ttu-id="64200-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64200-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="64200-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64200-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64200-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64200-107">DESCRIPTION</span></span>
<span data-ttu-id="64200-108">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="64200-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="64200-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64200-109">EXAMPLES</span></span>

### <span data-ttu-id="64200-110">Пример 1. Удаление виртуального правила сети</span><span class="sxs-lookup"><span data-stu-id="64200-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="64200-111">Эта команда удаляет виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="64200-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="64200-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64200-112">PARAMETERS</span></span>

### <span data-ttu-id="64200-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64200-113">-AsJob</span></span>
<span data-ttu-id="64200-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="64200-114">Run the command as a job</span></span>

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

### <span data-ttu-id="64200-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64200-115">-DefaultProfile</span></span>
<span data-ttu-id="64200-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64200-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64200-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64200-117">-InputObject</span></span>
<span data-ttu-id="64200-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="64200-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64200-119">-Name</span><span class="sxs-lookup"><span data-stu-id="64200-119">-Name</span></span>
<span data-ttu-id="64200-120">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="64200-120">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="64200-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64200-121">-NoWait</span></span>
<span data-ttu-id="64200-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="64200-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64200-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64200-123">-PassThru</span></span>
<span data-ttu-id="64200-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="64200-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64200-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64200-125">-ResourceGroupName</span></span>
<span data-ttu-id="64200-126">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="64200-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="64200-127">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="64200-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="64200-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="64200-128">-ServerName</span></span>
<span data-ttu-id="64200-129">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="64200-129">The name of the server.</span></span>

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

### <span data-ttu-id="64200-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64200-130">-SubscriptionId</span></span>
<span data-ttu-id="64200-131">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="64200-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="64200-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64200-132">-Confirm</span></span>
<span data-ttu-id="64200-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="64200-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64200-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64200-134">-WhatIf</span></span>
<span data-ttu-id="64200-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64200-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64200-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="64200-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64200-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64200-137">CommonParameters</span></span>
<span data-ttu-id="64200-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64200-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64200-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64200-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64200-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64200-140">INPUTS</span></span>

### <span data-ttu-id="64200-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="64200-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="64200-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64200-142">OUTPUTS</span></span>

### <span data-ttu-id="64200-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64200-143">System.Boolean</span></span>

## <span data-ttu-id="64200-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64200-144">NOTES</span></span>

<span data-ttu-id="64200-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="64200-145">ALIASES</span></span>

<span data-ttu-id="64200-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="64200-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64200-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="64200-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64200-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64200-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64200-149">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="64200-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64200-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="64200-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="64200-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="64200-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="64200-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="64200-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="64200-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="64200-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64200-154">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="64200-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="64200-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="64200-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="64200-156">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="64200-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="64200-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="64200-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="64200-158">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="64200-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="64200-159">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="64200-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="64200-160">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="64200-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="64200-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64200-161">RELATED LINKS</span></span>

