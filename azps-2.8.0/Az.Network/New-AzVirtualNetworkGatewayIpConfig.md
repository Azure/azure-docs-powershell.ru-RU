---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 8793da5f73ba1b6891d3522c171c167753188c1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902058"
---
# <span data-ttu-id="f0c55-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0c55-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="f0c55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0c55-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c55-103">Создание конфигурации IP для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f0c55-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="f0c55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0c55-104">SYNTAX</span></span>

### <span data-ttu-id="f0c55-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f0c55-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0c55-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f0c55-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0c55-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0c55-107">DESCRIPTION</span></span>
<span data-ttu-id="f0c55-108">Командлет **New-AzVirtualNetworkGatewayIpConfig** создает конфигурацию, назначенную виртуальному сетевому шлюзу с общедоступным IP-адресом, который основан на номере подсети.</span><span class="sxs-lookup"><span data-stu-id="f0c55-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="f0c55-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0c55-109">EXAMPLES</span></span>

### <span data-ttu-id="f0c55-110">1: создание IP-конфигурации для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f0c55-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="f0c55-111">Настройка шлюза виртуальной сети с общедоступным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="f0c55-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="f0c55-112">Переменная $myGWsubnet получается с помощью командлета **Get-AzVirtualNetworkSubnetConfig** на "GatewaySubnet" в виртуальной сети, для которой вы собираетесь создать шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f0c55-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="f0c55-113">Переменная $myGWpip получается с помощью командлета **New-AzPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="f0c55-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="f0c55-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0c55-114">PARAMETERS</span></span>

### <span data-ttu-id="f0c55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c55-115">-DefaultProfile</span></span>
<span data-ttu-id="f0c55-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0c55-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0c55-117">-Name</span></span>
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

### <span data-ttu-id="f0c55-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0c55-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="f0c55-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0c55-119">-PublicIpAddress</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c55-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f0c55-120">-PublicIpAddressId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c55-121">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="f0c55-121">-Subnet</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c55-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f0c55-122">-SubnetId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c55-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c55-123">CommonParameters</span></span>
<span data-ttu-id="f0c55-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0c55-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c55-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c55-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c55-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0c55-126">INPUTS</span></span>

### <span data-ttu-id="f0c55-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="f0c55-127">None</span></span>

## <span data-ttu-id="f0c55-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0c55-128">OUTPUTS</span></span>

### <span data-ttu-id="f0c55-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0c55-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="f0c55-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0c55-130">NOTES</span></span>

## <span data-ttu-id="f0c55-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0c55-131">RELATED LINKS</span></span>

[<span data-ttu-id="f0c55-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0c55-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="f0c55-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0c55-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
