---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415804"
---
# <span data-ttu-id="e1fac-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="e1fac-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="e1fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1fac-102">SYNOPSIS</span></span>
<span data-ttu-id="e1fac-103">Создает пиринг vNet для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e1fac-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="e1fac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1fac-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e1fac-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1fac-105">DESCRIPTION</span></span>
<span data-ttu-id="e1fac-106">Создает пиринг vNet для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e1fac-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="e1fac-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1fac-107">EXAMPLES</span></span>

### <span data-ttu-id="e1fac-108">Пример 1. Создание пиринга vnet для datab ветвей</span><span class="sxs-lookup"><span data-stu-id="e1fac-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="e1fac-109">Эта команда создает пиринг vnet для datab ветвей.</span><span class="sxs-lookup"><span data-stu-id="e1fac-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="e1fac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1fac-110">PARAMETERS</span></span>

### <span data-ttu-id="e1fac-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="e1fac-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="e1fac-112">Будет ли разрешен/запрещен трафик, переадверляемый виртуальными сетями в удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e1fac-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="e1fac-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="e1fac-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="e1fac-114">Если связи шлюза можно использовать в удаленной виртуальной сети для связи с этой виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="e1fac-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="e1fac-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e1fac-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="e1fac-116">Могут ли виртуальные системы получать доступ к виртуальным сетям в удаленном сетевом пространстве.</span><span class="sxs-lookup"><span data-stu-id="e1fac-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="e1fac-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1fac-117">-AsJob</span></span>
<span data-ttu-id="e1fac-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e1fac-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e1fac-119">-DatabdresssAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="e1fac-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="e1fac-120">Список блоков адресов, зарезервированных для этой виртуальной сети, в нотации CIDR.</span><span class="sxs-lookup"><span data-stu-id="e1fac-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fac-121">-DatabvirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e1fac-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="e1fac-122">ИД виртуальной сети datab в сети.</span><span class="sxs-lookup"><span data-stu-id="e1fac-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="e1fac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1fac-123">-DefaultProfile</span></span>
<span data-ttu-id="e1fac-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1fac-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1fac-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e1fac-125">-Name</span></span>
<span data-ttu-id="e1fac-126">Имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e1fac-126">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fac-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e1fac-127">-NoWait</span></span>
<span data-ttu-id="e1fac-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e1fac-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e1fac-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="e1fac-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="e1fac-130">Список блоков адресов, зарезервированных для этой виртуальной сети, в нотации CIDR.</span><span class="sxs-lookup"><span data-stu-id="e1fac-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fac-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e1fac-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="e1fac-132">ИД удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e1fac-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="e1fac-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1fac-133">-ResourceGroupName</span></span>
<span data-ttu-id="e1fac-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1fac-134">The name of the resource group.</span></span>
<span data-ttu-id="e1fac-135">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e1fac-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fac-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1fac-136">-SubscriptionId</span></span>
<span data-ttu-id="e1fac-137">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e1fac-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fac-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="e1fac-138">-UseRemoteGateway</span></span>
<span data-ttu-id="e1fac-139">Если в этой виртуальной сети можно использовать удаленные шлюзы.</span><span class="sxs-lookup"><span data-stu-id="e1fac-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="e1fac-140">Если флаг имеет true и allowGatewayTransit для удаленного пиринга также имеет true, виртуальная сеть будет использовать шлюзы удаленной виртуальной сети для общественного транспорта.</span><span class="sxs-lookup"><span data-stu-id="e1fac-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="e1fac-141">Только один пиринг может иметь для этого флага истинное.</span><span class="sxs-lookup"><span data-stu-id="e1fac-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="e1fac-142">Этот флажок нельзя установить, если в виртуальной сети уже есть шлюз.</span><span class="sxs-lookup"><span data-stu-id="e1fac-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="e1fac-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e1fac-143">-WorkspaceName</span></span>
<span data-ttu-id="e1fac-144">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e1fac-144">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fac-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1fac-145">-Confirm</span></span>
<span data-ttu-id="e1fac-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1fac-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1fac-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1fac-147">-WhatIf</span></span>
<span data-ttu-id="e1fac-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1fac-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1fac-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e1fac-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1fac-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1fac-150">CommonParameters</span></span>
<span data-ttu-id="e1fac-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1fac-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1fac-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1fac-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1fac-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1fac-153">INPUTS</span></span>

## <span data-ttu-id="e1fac-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1fac-154">OUTPUTS</span></span>

### <span data-ttu-id="e1fac-155">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e1fac-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="e1fac-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1fac-156">NOTES</span></span>

<span data-ttu-id="e1fac-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e1fac-157">ALIASES</span></span>

## <span data-ttu-id="e1fac-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1fac-158">RELATED LINKS</span></span>

