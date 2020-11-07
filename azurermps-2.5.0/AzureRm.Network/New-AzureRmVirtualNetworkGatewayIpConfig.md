---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 1a043b14ef957eed6ac4983c4a30edf6fc72521f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915121"
---
# <span data-ttu-id="886ad-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="886ad-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="886ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="886ad-102">SYNOPSIS</span></span>
<span data-ttu-id="886ad-103">Создание конфигурации IP для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="886ad-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="886ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="886ad-104">SYNTAX</span></span>

### <span data-ttu-id="886ad-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="886ad-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="886ad-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="886ad-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="886ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="886ad-107">DESCRIPTION</span></span>
<span data-ttu-id="886ad-108">Командлет **New-AzureRmVirtualNetworkGatewayIpConfig** создает конфигурацию, назначенную виртуальному сетевому шлюзу с общедоступным IP-адресом, который основан на номере подсети.</span><span class="sxs-lookup"><span data-stu-id="886ad-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="886ad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="886ad-109">EXAMPLES</span></span>

### <span data-ttu-id="886ad-110">1: создание IP-конфигурации для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="886ad-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="886ad-111">Настройка шлюза виртуальной сети с общедоступным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="886ad-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="886ad-112">Переменная $myGWsubnet получается с помощью командлета **Get-AzureRmVirtualNetworkSubnetConfig** на "GatewaySubnet" в виртуальной сети, для которой вы собираетесь создать шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="886ad-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="886ad-113">Переменная $myGWpip получается с помощью командлета **New-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="886ad-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="886ad-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="886ad-114">PARAMETERS</span></span>

### <span data-ttu-id="886ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="886ad-115">-DefaultProfile</span></span>
<span data-ttu-id="886ad-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="886ad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886ad-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="886ad-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886ad-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="886ad-118">-PrivateIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886ad-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="886ad-119">-PublicIpAddress</span></span>
```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886ad-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="886ad-120">-PublicIpAddressId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886ad-121">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="886ad-121">-Subnet</span></span>
```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886ad-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="886ad-122">-SubnetId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="886ad-123">CommonParameters</span></span>
<span data-ttu-id="886ad-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="886ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="886ad-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="886ad-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="886ad-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="886ad-126">INPUTS</span></span>

## <span data-ttu-id="886ad-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="886ad-127">OUTPUTS</span></span>

### <span data-ttu-id="886ad-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="886ad-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="886ad-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="886ad-129">NOTES</span></span>

## <span data-ttu-id="886ad-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="886ad-130">RELATED LINKS</span></span>

