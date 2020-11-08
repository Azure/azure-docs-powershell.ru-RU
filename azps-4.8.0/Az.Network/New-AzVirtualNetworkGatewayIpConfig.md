---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234972"
---
# <span data-ttu-id="3d9b0-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d9b0-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="3d9b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9b0-103">Создание конфигурации IP для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3d9b0-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="3d9b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d9b0-104">SYNTAX</span></span>

### <span data-ttu-id="3d9b0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d9b0-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9b0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3d9b0-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d9b0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d9b0-107">DESCRIPTION</span></span>
<span data-ttu-id="3d9b0-108">Командлет **New-AzVirtualNetworkGatewayIpConfig** создает конфигурацию, назначенную виртуальному сетевому шлюзу с общедоступным IP-адресом, который основан на номере подсети.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="3d9b0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d9b0-109">EXAMPLES</span></span>

### <span data-ttu-id="3d9b0-110">1: создание IP-конфигурации для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3d9b0-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="3d9b0-111">Настройка шлюза виртуальной сети с общедоступным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="3d9b0-112">Переменная $myGWsubnet получается с помощью командлета **Get-AzVirtualNetworkSubnetConfig** на "GatewaySubnet" в виртуальной сети, для которой вы собираетесь создать шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="3d9b0-113">Переменная $myGWpip получается с помощью командлета **New-AzPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="3d9b0-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="3d9b0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d9b0-114">PARAMETERS</span></span>

### <span data-ttu-id="3d9b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9b0-115">-DefaultProfile</span></span>
<span data-ttu-id="3d9b0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d9b0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d9b0-117">-Name</span></span>
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

### <span data-ttu-id="3d9b0-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3d9b0-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="3d9b0-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3d9b0-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="3d9b0-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3d9b0-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="3d9b0-121">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="3d9b0-121">-Subnet</span></span>
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

### <span data-ttu-id="3d9b0-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3d9b0-122">-SubnetId</span></span>
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

### <span data-ttu-id="3d9b0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9b0-123">CommonParameters</span></span>
<span data-ttu-id="3d9b0-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9b0-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9b0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9b0-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d9b0-126">INPUTS</span></span>

### <span data-ttu-id="3d9b0-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="3d9b0-127">None</span></span>

## <span data-ttu-id="3d9b0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d9b0-128">OUTPUTS</span></span>

### <span data-ttu-id="3d9b0-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d9b0-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="3d9b0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d9b0-130">NOTES</span></span>

## <span data-ttu-id="3d9b0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d9b0-131">RELATED LINKS</span></span>

[<span data-ttu-id="3d9b0-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d9b0-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="3d9b0-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d9b0-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
