---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: 0fef46fb32c299a0d3117e8168e845777293d496
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963192"
---
# <span data-ttu-id="9970a-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9970a-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="9970a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9970a-102">SYNOPSIS</span></span>
<span data-ttu-id="9970a-103">Создайте правило сети.</span><span class="sxs-lookup"><span data-stu-id="9970a-103">Create a network rule.</span></span>

## <span data-ttu-id="9970a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9970a-104">SYNTAX</span></span>

### <span data-ttu-id="9970a-105">ByVirtualNetworkRule (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9970a-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9970a-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="9970a-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9970a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9970a-107">DESCRIPTION</span></span>
<span data-ttu-id="9970a-108">Создайте объект сетевого правила в текущем сеансе Powershell.</span><span class="sxs-lookup"><span data-stu-id="9970a-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="9970a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9970a-109">EXAMPLES</span></span>

### <span data-ttu-id="9970a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9970a-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="9970a-111">Создание набора правил виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9970a-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="9970a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9970a-112">PARAMETERS</span></span>

### <span data-ttu-id="9970a-113">-Action</span><span class="sxs-lookup"><span data-stu-id="9970a-113">-Action</span></span>
<span data-ttu-id="9970a-114">Действие правила сети.</span><span class="sxs-lookup"><span data-stu-id="9970a-114">The action of network rule.</span></span>

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

### <span data-ttu-id="9970a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9970a-115">-DefaultProfile</span></span>
<span data-ttu-id="9970a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9970a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9970a-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9970a-117">-IPAddressOrRange</span></span>
<span data-ttu-id="9970a-118">Указывает IP- или диапазон IP-адресов в формате CIDR.</span><span class="sxs-lookup"><span data-stu-id="9970a-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="9970a-119">Разрешен только IPV4-адрес.</span><span class="sxs-lookup"><span data-stu-id="9970a-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9970a-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="9970a-120">-IPRule</span></span>
<span data-ttu-id="9970a-121">Указать, что нужно создать IPRule.</span><span class="sxs-lookup"><span data-stu-id="9970a-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9970a-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9970a-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="9970a-123">ИД ресурса подсети, например: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="9970a-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9970a-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9970a-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="9970a-125">Указать, что нужно создать VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="9970a-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9970a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9970a-126">CommonParameters</span></span>
<span data-ttu-id="9970a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9970a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9970a-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9970a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9970a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9970a-129">INPUTS</span></span>

### <span data-ttu-id="9970a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9970a-130">System.String</span></span>

## <span data-ttu-id="9970a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9970a-131">OUTPUTS</span></span>

### <span data-ttu-id="9970a-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9970a-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="9970a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9970a-133">NOTES</span></span>

## <span data-ttu-id="9970a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9970a-134">RELATED LINKS</span></span>
