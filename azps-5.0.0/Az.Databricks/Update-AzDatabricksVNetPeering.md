---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312806"
---
# <span data-ttu-id="fb3b4-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="fb3b4-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="fb3b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3b4-103">Обновите одноранговую сеть для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="fb3b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb3b4-104">SYNTAX</span></span>

### <span data-ttu-id="fb3b4-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb3b4-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fb3b4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fb3b4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb3b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb3b4-107">DESCRIPTION</span></span>
<span data-ttu-id="fb3b4-108">Обновите одноранговую сеть для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="fb3b4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb3b4-109">EXAMPLES</span></span>

### <span data-ttu-id="fb3b4-110">Пример 1: обновление AllowForwardedTraffic для пиринга vnet</span><span class="sxs-lookup"><span data-stu-id="fb3b4-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="fb3b4-111">Эта команда обновляет AllowForwardedTraffic пиринга vnet.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="fb3b4-112">Пример 2: обновление AllowForwardedTraffic пиринга vnet по объекту</span><span class="sxs-lookup"><span data-stu-id="fb3b4-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="fb3b4-113">Эта команда обновляет AllowForwardedTraffic пиринга vnet по объекту.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="fb3b4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb3b4-114">PARAMETERS</span></span>

### <span data-ttu-id="fb3b4-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="fb3b4-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="fb3b4-116">[System. Management. Automation. SwitchParameter] разрешено и не разрешено переадресованный трафик из виртуальных машин в локальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="fb3b4-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="fb3b4-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="fb3b4-118">[System. Management. Automation. SwitchParameter], если вы можете использовать ссылки на шлюзы в удаленных виртуальных сетях для связи с этой виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="fb3b4-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="fb3b4-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="fb3b4-120">[System. Management. Automation. SwitchParameter] позволяет получать доступ к виртуальным машинам в удаленной виртуальной сети в пространстве локальных виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="fb3b4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb3b4-121">-AsJob</span></span>
<span data-ttu-id="fb3b4-122">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fb3b4-122">Run the command as a job</span></span>

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

### <span data-ttu-id="fb3b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3b4-123">-DefaultProfile</span></span>
<span data-ttu-id="fb3b4-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb3b4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb3b4-125">-InputObject</span></span>
<span data-ttu-id="fb3b4-126">Параметр удостоверения.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-126">Identity parameter.</span></span>
<span data-ttu-id="fb3b4-127">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb3b4-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb3b4-128">-Name</span></span>
<span data-ttu-id="fb3b4-129">Имя VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="fb3b4-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="fb3b4-130">-NoWait</span></span>
<span data-ttu-id="fb3b4-131">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="fb3b4-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fb3b4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3b4-132">-ResourceGroupName</span></span>
<span data-ttu-id="fb3b4-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-133">The name of the resource group.</span></span>
<span data-ttu-id="fb3b4-134">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fb3b4-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb3b4-135">-SubscriptionId</span></span>
<span data-ttu-id="fb3b4-136">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fb3b4-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="fb3b4-137">-UseRemoteGateway</span></span>
<span data-ttu-id="fb3b4-138">[System. Management. Automation. SwitchParameter], если удаленные шлюзы можно использовать в этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="fb3b4-139">Если флаг имеет значение true, а allowGatewayTransit на удаленном одноранговом соединении также имеет значение true, виртуальная сеть будет использовать шлюзы удаленной виртуальной сети для транзита.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="fb3b4-140">Этот флаг может иметь значение true только для одного однорангового элемента.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="fb3b4-141">Этот флаг не может быть установлен, если у виртуальной сети уже есть шлюз.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="fb3b4-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb3b4-142">-WorkspaceName</span></span>
<span data-ttu-id="fb3b4-143">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="fb3b4-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb3b4-144">-Confirm</span></span>
<span data-ttu-id="fb3b4-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3b4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3b4-146">-WhatIf</span></span>
<span data-ttu-id="fb3b4-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3b4-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3b4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3b4-149">CommonParameters</span></span>
<span data-ttu-id="fb3b4-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3b4-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb3b4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3b4-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb3b4-152">INPUTS</span></span>

### <span data-ttu-id="fb3b4-153">Microsoft. Azure. PowerShell. командлеты. кирпичи. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="fb3b4-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="fb3b4-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb3b4-154">OUTPUTS</span></span>

### <span data-ttu-id="fb3b4-155">Microsoft. Azure. PowerShell. командлеты. кирпичи. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fb3b4-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="fb3b4-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb3b4-156">NOTES</span></span>

<span data-ttu-id="fb3b4-157">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="fb3b4-157">ALIASES</span></span>

<span data-ttu-id="fb3b4-158">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fb3b4-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb3b4-159">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb3b4-160">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb3b4-161">INPUTOBJECT <IDatabricksIdentity> : параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="fb3b4-162">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="fb3b4-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb3b4-163">`[PeeringName <String>]`: Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="fb3b4-164">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fb3b4-165">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="fb3b4-166">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fb3b4-167">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fb3b4-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="fb3b4-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb3b4-168">RELATED LINKS</span></span>

