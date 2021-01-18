---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516950"
---
# <span data-ttu-id="e608c-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="e608c-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="e608c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e608c-102">SYNOPSIS</span></span>
<span data-ttu-id="e608c-103">Обновление пиринга vNet для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e608c-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="e608c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e608c-104">SYNTAX</span></span>

### <span data-ttu-id="e608c-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e608c-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e608c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e608c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e608c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e608c-107">DESCRIPTION</span></span>
<span data-ttu-id="e608c-108">Обновление пиринга vNet для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e608c-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="e608c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e608c-109">EXAMPLES</span></span>

### <span data-ttu-id="e608c-110">Пример 1. Обновление для пиринга vnet AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="e608c-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="e608c-111">Эта команда обновляет пиринг vnet AllowForwardedTraffic.</span><span class="sxs-lookup"><span data-stu-id="e608c-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="e608c-112">Пример 2. Обновление для пиринга vnet по объектам AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="e608c-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="e608c-113">Эта команда обновляет для объекта разрешениеForwardedTraffic пиринга vnet.</span><span class="sxs-lookup"><span data-stu-id="e608c-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="e608c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e608c-114">PARAMETERS</span></span>

### <span data-ttu-id="e608c-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="e608c-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="e608c-116">[System.Management.Automation.SwitchParameter] Будет ли в удаленной виртуальной сети разрешен и запрещен трафик, переадрекованный из виртуальных м-карт в локальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e608c-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="e608c-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="e608c-118">[System.Management.Automation.SwitchParameter] Если в удаленной виртуальной сети можно использовать связи шлюза для связывания с этой виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="e608c-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e608c-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="e608c-120">[System.Management.Automation.SwitchParameter] Позволяет ли виртуальным виртуальным мс в локальном виртуальном сетевом пространстве получать доступ к виртуальным пространствам.</span><span class="sxs-lookup"><span data-stu-id="e608c-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e608c-121">-AsJob</span></span>
<span data-ttu-id="e608c-122">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e608c-122">Run the command as a job</span></span>

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

### <span data-ttu-id="e608c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e608c-123">-DefaultProfile</span></span>
<span data-ttu-id="e608c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e608c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e608c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e608c-125">-InputObject</span></span>
<span data-ttu-id="e608c-126">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="e608c-126">Identity parameter.</span></span>
<span data-ttu-id="e608c-127">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="e608c-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e608c-128">-Name</span></span>
<span data-ttu-id="e608c-129">Имя VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="e608c-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e608c-130">-NoWait</span></span>
<span data-ttu-id="e608c-131">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e608c-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e608c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e608c-132">-ResourceGroupName</span></span>
<span data-ttu-id="e608c-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e608c-133">The name of the resource group.</span></span>
<span data-ttu-id="e608c-134">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e608c-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e608c-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e608c-135">-SubscriptionId</span></span>
<span data-ttu-id="e608c-136">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e608c-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e608c-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="e608c-137">-UseRemoteGateway</span></span>
<span data-ttu-id="e608c-138">[System.Management.Automation.SwitchParameter] Если в этой виртуальной сети можно использовать удаленные шлюзы.</span><span class="sxs-lookup"><span data-stu-id="e608c-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="e608c-139">Если флаг имеет true и allowGatewayTransit для удаленного пиринга также имеет true, виртуальная сеть будет использовать шлюзы удаленной виртуальной сети для общественного транспорта.</span><span class="sxs-lookup"><span data-stu-id="e608c-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="e608c-140">Только один пиринг может иметь для этого флага истинное.</span><span class="sxs-lookup"><span data-stu-id="e608c-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="e608c-141">Этот флажок нельзя установить, если в виртуальной сети уже есть шлюз.</span><span class="sxs-lookup"><span data-stu-id="e608c-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e608c-142">-WorkspaceName</span></span>
<span data-ttu-id="e608c-143">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e608c-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="e608c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e608c-144">-Confirm</span></span>
<span data-ttu-id="e608c-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e608c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e608c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e608c-146">-WhatIf</span></span>
<span data-ttu-id="e608c-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e608c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e608c-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e608c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e608c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e608c-149">CommonParameters</span></span>
<span data-ttu-id="e608c-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e608c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e608c-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e608c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e608c-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e608c-152">INPUTS</span></span>

### <span data-ttu-id="e608c-153">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Models.IDatabоsIdentity</span><span class="sxs-lookup"><span data-stu-id="e608c-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e608c-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e608c-154">OUTPUTS</span></span>

### <span data-ttu-id="e608c-155">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e608c-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="e608c-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e608c-156">NOTES</span></span>

<span data-ttu-id="e608c-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e608c-157">ALIASES</span></span>

<span data-ttu-id="e608c-158">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e608c-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e608c-159">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="e608c-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e608c-160">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e608c-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e608c-161">INPUTOBJECT <IDatabricksIdentity> : Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="e608c-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="e608c-162">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="e608c-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e608c-163">`[PeeringName <String>]`: имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e608c-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e608c-164">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e608c-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e608c-165">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e608c-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="e608c-166">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e608c-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e608c-167">`[WorkspaceName <String>]`: имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e608c-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e608c-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e608c-168">RELATED LINKS</span></span>

