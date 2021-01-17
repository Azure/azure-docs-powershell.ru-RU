---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416412"
---
# <span data-ttu-id="85689-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85689-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="85689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85689-102">SYNOPSIS</span></span>
<span data-ttu-id="85689-103">Изменяет конфигурацию IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="85689-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="85689-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85689-104">SYNTAX</span></span>

### <span data-ttu-id="85689-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="85689-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85689-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="85689-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85689-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85689-107">DESCRIPTION</span></span>
<span data-ttu-id="85689-108">**Cmdlet Set-AzApplicationGatewayIPConfiguration** изменяет конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="85689-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="85689-109">Конфигурация IP-адреса содержит подсеть, в которой развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="85689-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="85689-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85689-110">EXAMPLES</span></span>

### <span data-ttu-id="85689-111">Пример 1. Обновление конфигурации IP-адреса для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="85689-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="85689-112">Первая команда получает виртуальную сеть VNet01, которая принадлежит к группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="85689-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="85689-113">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="85689-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="85689-114">Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="85689-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="85689-115">Данная команда задает конфигурацию IP-адреса шлюза приложения, $AppGw конфигурацию подсети, которая хранится в $Subnet.</span><span class="sxs-lookup"><span data-stu-id="85689-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="85689-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85689-116">PARAMETERS</span></span>

### <span data-ttu-id="85689-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85689-117">-ApplicationGateway</span></span>
<span data-ttu-id="85689-118">Указывает объект шлюза приложения, с которым этот cmdlet связывает конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="85689-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="85689-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85689-119">-DefaultProfile</span></span>
<span data-ttu-id="85689-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85689-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85689-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85689-121">-Name</span></span>
<span data-ttu-id="85689-122">Указывает имя конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="85689-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="85689-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="85689-123">-Subnet</span></span>
<span data-ttu-id="85689-124">Определяет подсеть.</span><span class="sxs-lookup"><span data-stu-id="85689-124">Specifies the subnet.</span></span>
<span data-ttu-id="85689-125">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="85689-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="85689-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="85689-126">-SubnetId</span></span>
<span data-ttu-id="85689-127">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="85689-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="85689-128">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="85689-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="85689-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85689-129">CommonParameters</span></span>
<span data-ttu-id="85689-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85689-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85689-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85689-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85689-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85689-132">INPUTS</span></span>

### <span data-ttu-id="85689-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85689-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85689-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85689-134">OUTPUTS</span></span>

### <span data-ttu-id="85689-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85689-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85689-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85689-136">NOTES</span></span>

## <span data-ttu-id="85689-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85689-137">RELATED LINKS</span></span>

[<span data-ttu-id="85689-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85689-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85689-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85689-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85689-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85689-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85689-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85689-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85689-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85689-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


