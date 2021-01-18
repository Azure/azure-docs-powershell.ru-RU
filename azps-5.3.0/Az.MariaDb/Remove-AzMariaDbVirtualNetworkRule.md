---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507123"
---
# <span data-ttu-id="45bb4-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="45bb4-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="45bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="45bb4-103">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="45bb4-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="45bb4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45bb4-104">SYNTAX</span></span>

### <span data-ttu-id="45bb4-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45bb4-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="45bb4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45bb4-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45bb4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45bb4-107">DESCRIPTION</span></span>
<span data-ttu-id="45bb4-108">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="45bb4-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="45bb4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45bb4-109">EXAMPLES</span></span>

### <span data-ttu-id="45bb4-110">Пример 1. Удаление виртуального правила сети</span><span class="sxs-lookup"><span data-stu-id="45bb4-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="45bb4-111">Эта команда удаляет виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="45bb4-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="45bb4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45bb4-112">PARAMETERS</span></span>

### <span data-ttu-id="45bb4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45bb4-113">-AsJob</span></span>
<span data-ttu-id="45bb4-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="45bb4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="45bb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bb4-115">-DefaultProfile</span></span>
<span data-ttu-id="45bb4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45bb4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45bb4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45bb4-117">-InputObject</span></span>
<span data-ttu-id="45bb4-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="45bb4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45bb4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="45bb4-119">-Name</span></span>
<span data-ttu-id="45bb4-120">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="45bb4-120">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="45bb4-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="45bb4-121">-NoWait</span></span>
<span data-ttu-id="45bb4-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="45bb4-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="45bb4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45bb4-123">-PassThru</span></span>
<span data-ttu-id="45bb4-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="45bb4-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="45bb4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45bb4-125">-ResourceGroupName</span></span>
<span data-ttu-id="45bb4-126">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="45bb4-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="45bb4-127">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="45bb4-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="45bb4-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="45bb4-128">-ServerName</span></span>
<span data-ttu-id="45bb4-129">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="45bb4-129">The name of the server.</span></span>

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

### <span data-ttu-id="45bb4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45bb4-130">-SubscriptionId</span></span>
<span data-ttu-id="45bb4-131">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="45bb4-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="45bb4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45bb4-132">-Confirm</span></span>
<span data-ttu-id="45bb4-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45bb4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45bb4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45bb4-134">-WhatIf</span></span>
<span data-ttu-id="45bb4-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45bb4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45bb4-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45bb4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45bb4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bb4-137">CommonParameters</span></span>
<span data-ttu-id="45bb4-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45bb4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bb4-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45bb4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bb4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45bb4-140">INPUTS</span></span>

### <span data-ttu-id="45bb4-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="45bb4-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="45bb4-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45bb4-142">OUTPUTS</span></span>

### <span data-ttu-id="45bb4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45bb4-143">System.Boolean</span></span>

## <span data-ttu-id="45bb4-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45bb4-144">NOTES</span></span>

<span data-ttu-id="45bb4-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="45bb4-145">ALIASES</span></span>

<span data-ttu-id="45bb4-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="45bb4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45bb4-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="45bb4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45bb4-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45bb4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45bb4-149">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="45bb4-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45bb4-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="45bb4-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="45bb4-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="45bb4-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="45bb4-152">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="45bb4-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="45bb4-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="45bb4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45bb4-154">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="45bb4-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="45bb4-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="45bb4-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="45bb4-156">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="45bb4-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="45bb4-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="45bb4-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="45bb4-158">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="45bb4-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="45bb4-159">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="45bb4-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="45bb4-160">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="45bb4-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="45bb4-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45bb4-161">RELATED LINKS</span></span>

