---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: b8a38bd16fcd08104f678752d03dbc4a6d1f054b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003480"
---
# <span data-ttu-id="96b3a-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96b3a-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="96b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="96b3a-103">Изменяет конфигурацию IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="96b3a-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="96b3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96b3a-104">SYNTAX</span></span>

### <span data-ttu-id="96b3a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="96b3a-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96b3a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="96b3a-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96b3a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96b3a-107">DESCRIPTION</span></span>
<span data-ttu-id="96b3a-108">**Cmdlet Set-AzApplicationGatewayIPConfiguration** изменяет конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="96b3a-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="96b3a-109">Конфигурация IP-адреса содержит подсеть, в которой развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="96b3a-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="96b3a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96b3a-110">EXAMPLES</span></span>

### <span data-ttu-id="96b3a-111">Пример 1. Обновление конфигурации IP-адреса для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="96b3a-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="96b3a-112">Первая команда получает виртуальную сеть VNet01, которая принадлежит к группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="96b3a-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="96b3a-113">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="96b3a-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="96b3a-114">Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="96b3a-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="96b3a-115">Данная команда задает конфигурацию IP-адреса шлюза приложения, $AppGw конфигурацию подсети, которая хранится в $Subnet.</span><span class="sxs-lookup"><span data-stu-id="96b3a-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="96b3a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96b3a-116">PARAMETERS</span></span>

### <span data-ttu-id="96b3a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96b3a-117">-ApplicationGateway</span></span>
<span data-ttu-id="96b3a-118">Определяет объект шлюза приложения, с которым этот cmdlet связывает конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="96b3a-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96b3a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b3a-119">-DefaultProfile</span></span>
<span data-ttu-id="96b3a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96b3a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96b3a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="96b3a-121">-Name</span></span>
<span data-ttu-id="96b3a-122">Указывает имя конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="96b3a-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="96b3a-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="96b3a-123">-Subnet</span></span>
<span data-ttu-id="96b3a-124">Указывает подсеть.</span><span class="sxs-lookup"><span data-stu-id="96b3a-124">Specifies the subnet.</span></span>
<span data-ttu-id="96b3a-125">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="96b3a-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="96b3a-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="96b3a-126">-SubnetId</span></span>
<span data-ttu-id="96b3a-127">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="96b3a-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="96b3a-128">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="96b3a-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="96b3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b3a-129">CommonParameters</span></span>
<span data-ttu-id="96b3a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96b3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b3a-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96b3a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b3a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96b3a-132">INPUTS</span></span>

### <span data-ttu-id="96b3a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96b3a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96b3a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96b3a-134">OUTPUTS</span></span>

### <span data-ttu-id="96b3a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96b3a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96b3a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96b3a-136">NOTES</span></span>

## <span data-ttu-id="96b3a-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96b3a-137">RELATED LINKS</span></span>

[<span data-ttu-id="96b3a-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96b3a-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="96b3a-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96b3a-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="96b3a-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96b3a-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="96b3a-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96b3a-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="96b3a-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96b3a-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


