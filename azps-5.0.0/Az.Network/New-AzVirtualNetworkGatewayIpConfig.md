---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248114"
---
# <span data-ttu-id="da164-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="da164-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="da164-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da164-102">SYNOPSIS</span></span>
<span data-ttu-id="da164-103">Создание конфигурации IP для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="da164-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="da164-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da164-104">SYNTAX</span></span>

### <span data-ttu-id="da164-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="da164-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da164-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="da164-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da164-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da164-107">DESCRIPTION</span></span>
<span data-ttu-id="da164-108">Командлет **New-AzVirtualNetworkGatewayIpConfig** создает конфигурацию, назначенную виртуальному сетевому шлюзу с общедоступным IP-адресом, который основан на номере подсети.</span><span class="sxs-lookup"><span data-stu-id="da164-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="da164-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da164-109">EXAMPLES</span></span>

### <span data-ttu-id="da164-110">1: создание IP-конфигурации для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="da164-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="da164-111">Настройка шлюза виртуальной сети с общедоступным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="da164-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="da164-112">Переменная $myGWsubnet получается с помощью командлета **Get-AzVirtualNetworkSubnetConfig** на "GatewaySubnet" в виртуальной сети, для которой вы собираетесь создать шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="da164-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="da164-113">Переменная $myGWpip получается с помощью командлета **New-AzPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="da164-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="da164-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da164-114">PARAMETERS</span></span>

### <span data-ttu-id="da164-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da164-115">-DefaultProfile</span></span>
<span data-ttu-id="da164-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da164-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da164-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da164-117">-Name</span></span>
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

### <span data-ttu-id="da164-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="da164-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="da164-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da164-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="da164-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="da164-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="da164-121">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="da164-121">-Subnet</span></span>
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

### <span data-ttu-id="da164-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="da164-122">-SubnetId</span></span>
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

### <span data-ttu-id="da164-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da164-123">CommonParameters</span></span>
<span data-ttu-id="da164-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da164-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da164-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da164-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da164-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da164-126">INPUTS</span></span>

### <span data-ttu-id="da164-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="da164-127">None</span></span>

## <span data-ttu-id="da164-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da164-128">OUTPUTS</span></span>

### <span data-ttu-id="da164-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="da164-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="da164-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="da164-130">NOTES</span></span>

## <span data-ttu-id="da164-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da164-131">RELATED LINKS</span></span>

[<span data-ttu-id="da164-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="da164-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="da164-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="da164-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
