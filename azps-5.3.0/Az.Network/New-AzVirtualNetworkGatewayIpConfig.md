---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507797"
---
# <span data-ttu-id="10c53-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="10c53-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="10c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10c53-102">SYNOPSIS</span></span>
<span data-ttu-id="10c53-103">Создание конфигурации IP-адреса для виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="10c53-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="10c53-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10c53-104">SYNTAX</span></span>

### <span data-ttu-id="10c53-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10c53-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10c53-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10c53-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c53-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10c53-107">DESCRIPTION</span></span>
<span data-ttu-id="10c53-108">Командлет **New-AzVirtualNetworkGatewayIpConfig** создает конфигурацию, назначенную виртуальному сетевому шлюзу с ранее созданным общедоступным IP-адресом на основе ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="10c53-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="10c53-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10c53-109">EXAMPLES</span></span>

### <span data-ttu-id="10c53-110">1. Создание конфигурации IP-адреса для виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="10c53-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="10c53-111">Настраивает виртуальный сетевой шлюз с общедоступным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="10c53-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="10c53-112">Переменная $myGWsubnet получена с помощью командлета **Get-AzVirtualNetworkSubnetConfig** в сети GatewaySubnet в рамках виртуальной сети, в рамках сети, в которая предполагается создать виртуальный сетевой шлюз.</span><span class="sxs-lookup"><span data-stu-id="10c53-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="10c53-113">Переменная $myGWpip получена с помощью **cmdlet New-AzPublicIpAddress.**</span><span class="sxs-lookup"><span data-stu-id="10c53-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="10c53-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10c53-114">PARAMETERS</span></span>

### <span data-ttu-id="10c53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c53-115">-DefaultProfile</span></span>
<span data-ttu-id="10c53-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10c53-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10c53-117">-Name</span><span class="sxs-lookup"><span data-stu-id="10c53-117">-Name</span></span>
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

### <span data-ttu-id="10c53-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="10c53-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="10c53-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="10c53-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="10c53-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="10c53-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="10c53-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="10c53-121">-Subnet</span></span>
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

### <span data-ttu-id="10c53-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10c53-122">-SubnetId</span></span>
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

### <span data-ttu-id="10c53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c53-123">CommonParameters</span></span>
<span data-ttu-id="10c53-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c53-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c53-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c53-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10c53-126">INPUTS</span></span>

### <span data-ttu-id="10c53-127">Нет</span><span class="sxs-lookup"><span data-stu-id="10c53-127">None</span></span>

## <span data-ttu-id="10c53-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10c53-128">OUTPUTS</span></span>

### <span data-ttu-id="10c53-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10c53-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="10c53-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10c53-130">NOTES</span></span>

## <span data-ttu-id="10c53-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10c53-131">RELATED LINKS</span></span>

[<span data-ttu-id="10c53-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="10c53-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="10c53-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="10c53-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
