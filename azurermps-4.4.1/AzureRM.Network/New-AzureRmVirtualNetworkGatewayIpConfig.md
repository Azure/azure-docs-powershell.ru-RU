---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: faf242ea76e5985b0b8544e889fdc3240c87afb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559660"
---
# <span data-ttu-id="f89fa-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f89fa-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="f89fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f89fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f89fa-103">Создание конфигурации IP для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f89fa-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f89fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f89fa-104">SYNTAX</span></span>

### <span data-ttu-id="f89fa-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f89fa-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f89fa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f89fa-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f89fa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f89fa-107">DESCRIPTION</span></span>
<span data-ttu-id="f89fa-108">Командлет **New-AzureRmVirtualNetworkGatewayIpConfig** создает конфигурацию, назначенную виртуальному сетевому шлюзу с общедоступным IP-адресом, который основан на номере подсети.</span><span class="sxs-lookup"><span data-stu-id="f89fa-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="f89fa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f89fa-109">EXAMPLES</span></span>

### <span data-ttu-id="f89fa-110">1: создание IP-конфигурации для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f89fa-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="f89fa-111">Настройка шлюза виртуальной сети с общедоступным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="f89fa-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="f89fa-112">Переменная $myGWsubnet получается с помощью командлета **Get-AzureRmVirtualNetworkSubnetConfig** на "GatewaySubnet" в виртуальной сети, для которой вы собираетесь создать шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f89fa-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="f89fa-113">Переменная $myGWpip получается с помощью командлета **New-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="f89fa-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="f89fa-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f89fa-114">PARAMETERS</span></span>

### <span data-ttu-id="f89fa-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f89fa-115">-Name</span></span>
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

### <span data-ttu-id="f89fa-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f89fa-116">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="f89fa-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f89fa-117">-PublicIpAddress</span></span>
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

### <span data-ttu-id="f89fa-118">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f89fa-118">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="f89fa-119">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="f89fa-119">-Subnet</span></span>
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

### <span data-ttu-id="f89fa-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f89fa-120">-SubnetId</span></span>
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

### <span data-ttu-id="f89fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89fa-121">-DefaultProfile</span></span>
<span data-ttu-id="f89fa-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f89fa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89fa-123">CommonParameters</span></span>
<span data-ttu-id="f89fa-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f89fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89fa-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89fa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89fa-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f89fa-126">INPUTS</span></span>

## <span data-ttu-id="f89fa-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f89fa-127">OUTPUTS</span></span>

### <span data-ttu-id="f89fa-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f89fa-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="f89fa-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f89fa-129">NOTES</span></span>

## <span data-ttu-id="f89fa-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f89fa-130">RELATED LINKS</span></span>

