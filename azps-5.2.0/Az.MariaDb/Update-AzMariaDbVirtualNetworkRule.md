---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394215"
---
# <span data-ttu-id="f8015-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f8015-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="f8015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8015-102">SYNOPSIS</span></span>
<span data-ttu-id="f8015-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f8015-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f8015-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8015-104">SYNTAX</span></span>

### <span data-ttu-id="f8015-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8015-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f8015-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f8015-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f8015-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8015-107">DESCRIPTION</span></span>
<span data-ttu-id="f8015-108">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f8015-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f8015-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8015-109">EXAMPLES</span></span>

### <span data-ttu-id="f8015-110">Пример 1. Обновление правила виртуальной сети MariaDB</span><span class="sxs-lookup"><span data-stu-id="f8015-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="f8015-111">Эта команда обновляет виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="f8015-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="f8015-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8015-112">PARAMETERS</span></span>

### <span data-ttu-id="f8015-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8015-113">-AsJob</span></span>
<span data-ttu-id="f8015-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f8015-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f8015-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8015-115">-DefaultProfile</span></span>
<span data-ttu-id="f8015-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8015-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8015-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8015-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="f8015-118">Создайте правило брандмауэра до того, как в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="f8015-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="f8015-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8015-119">-InputObject</span></span>
<span data-ttu-id="f8015-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f8015-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8015-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8015-121">-Name</span></span>
<span data-ttu-id="f8015-122">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f8015-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8015-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f8015-123">-NoWait</span></span>
<span data-ttu-id="f8015-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="f8015-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f8015-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8015-125">-PassThru</span></span>
<span data-ttu-id="f8015-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="f8015-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f8015-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8015-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8015-128">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="f8015-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f8015-129">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="f8015-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8015-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f8015-130">-ServerName</span></span>
<span data-ttu-id="f8015-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f8015-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8015-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f8015-132">-SubnetId</span></span>
<span data-ttu-id="f8015-133">Это ARM ресурса виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="f8015-133">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8015-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8015-134">-SubscriptionId</span></span>
<span data-ttu-id="f8015-135">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="f8015-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8015-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8015-136">-Confirm</span></span>
<span data-ttu-id="f8015-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f8015-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8015-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8015-138">-WhatIf</span></span>
<span data-ttu-id="f8015-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8015-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8015-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f8015-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8015-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8015-141">CommonParameters</span></span>
<span data-ttu-id="f8015-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8015-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8015-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8015-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8015-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8015-144">INPUTS</span></span>

### <span data-ttu-id="f8015-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="f8015-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="f8015-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8015-146">OUTPUTS</span></span>

### <span data-ttu-id="f8015-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f8015-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="f8015-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8015-148">NOTES</span></span>

<span data-ttu-id="f8015-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f8015-149">ALIASES</span></span>

<span data-ttu-id="f8015-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f8015-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8015-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f8015-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8015-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8015-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8015-153">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="f8015-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8015-154">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="f8015-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f8015-155">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f8015-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f8015-156">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f8015-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f8015-157">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="f8015-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8015-158">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="f8015-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f8015-159">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="f8015-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f8015-160">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="f8015-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f8015-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="f8015-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f8015-162">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f8015-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f8015-163">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="f8015-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="f8015-164">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="f8015-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f8015-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8015-165">RELATED LINKS</span></span>
