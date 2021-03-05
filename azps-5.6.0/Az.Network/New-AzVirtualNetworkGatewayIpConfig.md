---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: cfbfd8df28cf4f0d9c11e654694172b86a549141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964136"
---
# <span data-ttu-id="93db0-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="93db0-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="93db0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93db0-102">SYNOPSIS</span></span>
<span data-ttu-id="93db0-103">Создает конфигурацию IP-адреса для виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="93db0-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="93db0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93db0-104">SYNTAX</span></span>

### <span data-ttu-id="93db0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="93db0-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93db0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="93db0-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93db0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93db0-107">DESCRIPTION</span></span>
<span data-ttu-id="93db0-108">Командлет **New-AzVirtualNetworkGatewayIpConfig** создает конфигурацию, назначенную виртуальному сетевому шлюзу с ранее созданным общедоступным IP-адресом на основе ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="93db0-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="93db0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93db0-109">EXAMPLES</span></span>

### <span data-ttu-id="93db0-110">1. Создание конфигурации IP-адреса для виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="93db0-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="93db0-111">Настраивает виртуальный сетевой шлюз с общедоступным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="93db0-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="93db0-112">Переменная $myGWsubnet получена с помощью командлета **Get-AzVirtualNetworkSubnetConfig** в сети GatewaySubnet в рамках виртуальной сети, в рамках планируемой вами виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="93db0-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="93db0-113">Переменная $myGWpip получена с помощью **cmdlet New-AzPublicIpAddress.**</span><span class="sxs-lookup"><span data-stu-id="93db0-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="93db0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93db0-114">PARAMETERS</span></span>

### <span data-ttu-id="93db0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93db0-115">-DefaultProfile</span></span>
<span data-ttu-id="93db0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93db0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93db0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="93db0-117">-Name</span></span>
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

### <span data-ttu-id="93db0-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="93db0-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="93db0-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="93db0-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="93db0-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="93db0-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="93db0-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="93db0-121">-Subnet</span></span>
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

### <span data-ttu-id="93db0-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="93db0-122">-SubnetId</span></span>
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

### <span data-ttu-id="93db0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93db0-123">CommonParameters</span></span>
<span data-ttu-id="93db0-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93db0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93db0-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93db0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93db0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93db0-126">INPUTS</span></span>

### <span data-ttu-id="93db0-127">Нет</span><span class="sxs-lookup"><span data-stu-id="93db0-127">None</span></span>

## <span data-ttu-id="93db0-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93db0-128">OUTPUTS</span></span>

### <span data-ttu-id="93db0-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="93db0-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="93db0-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93db0-130">NOTES</span></span>

## <span data-ttu-id="93db0-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93db0-131">RELATED LINKS</span></span>

[<span data-ttu-id="93db0-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="93db0-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="93db0-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="93db0-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
