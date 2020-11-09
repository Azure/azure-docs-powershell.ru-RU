---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311882"
---
# <span data-ttu-id="a128f-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a128f-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="a128f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a128f-102">SYNOPSIS</span></span>
<span data-ttu-id="a128f-103">Создание сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="a128f-103">Create a network rule.</span></span>

## <span data-ttu-id="a128f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a128f-104">SYNTAX</span></span>

### <span data-ttu-id="a128f-105">ByVirtualNetworkRule (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a128f-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a128f-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="a128f-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a128f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a128f-107">DESCRIPTION</span></span>
<span data-ttu-id="a128f-108">Создание объекта сетевого правила в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a128f-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="a128f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a128f-109">EXAMPLES</span></span>

### <span data-ttu-id="a128f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a128f-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="a128f-111">Создание virtualnetwork правила.</span><span class="sxs-lookup"><span data-stu-id="a128f-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="a128f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a128f-112">PARAMETERS</span></span>

### <span data-ttu-id="a128f-113">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="a128f-113">-Action</span></span>
<span data-ttu-id="a128f-114">Действие сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="a128f-114">The action of network rule.</span></span>

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

### <span data-ttu-id="a128f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a128f-115">-DefaultProfile</span></span>
<span data-ttu-id="a128f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a128f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a128f-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a128f-117">-IPAddressOrRange</span></span>
<span data-ttu-id="a128f-118">Указывает диапазон IP-адресов или IP-адресов в формате CIDR.</span><span class="sxs-lookup"><span data-stu-id="a128f-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="a128f-119">Разрешен только адрес IPV4.</span><span class="sxs-lookup"><span data-stu-id="a128f-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="a128f-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="a128f-120">-IPRule</span></span>
<span data-ttu-id="a128f-121">Укажите, что нужно сделать, чтобы создать IPRule.</span><span class="sxs-lookup"><span data-stu-id="a128f-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="a128f-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a128f-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="a128f-123">Идентификатор ресурса подсети, например:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="a128f-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="a128f-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a128f-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="a128f-125">Укажите, что нужно сделать, чтобы создать VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="a128f-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="a128f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a128f-126">CommonParameters</span></span>
<span data-ttu-id="a128f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a128f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a128f-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a128f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a128f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a128f-129">INPUTS</span></span>

### <span data-ttu-id="a128f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a128f-130">System.String</span></span>

## <span data-ttu-id="a128f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a128f-131">OUTPUTS</span></span>

### <span data-ttu-id="a128f-132">Microsoft. Azure. Commands. ContainerRegistry. Models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a128f-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="a128f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a128f-133">NOTES</span></span>

## <span data-ttu-id="a128f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a128f-134">RELATED LINKS</span></span>
