---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077721"
---
# <span data-ttu-id="c4ab5-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4ab5-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c4ab5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ab5-103">Добавление IP-конфигурации к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="c4ab5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4ab5-104">SYNTAX</span></span>

### <span data-ttu-id="c4ab5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4ab5-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4ab5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c4ab5-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4ab5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4ab5-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ab5-108">Командлет **Add-AzApplicationGatewayIPConfiguration** добавляет конфигурацию IP-адресов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="c4ab5-109">IP-конфигурации содержат подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="c4ab5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4ab5-110">EXAMPLES</span></span>

### <span data-ttu-id="c4ab5-111">Пример 1: Добавление конфигурации виртуальной сети к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="c4ab5-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="c4ab5-112">Первая команда получает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="c4ab5-113">Вторая команда получает подсеть, используя ранее созданную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="c4ab5-114">Третья команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c4ab5-115">Четвертая команда добавляет конфигурацию IP-адресов в шлюз приложений, хранящийся в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c4ab5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4ab5-116">PARAMETERS</span></span>

### <span data-ttu-id="c4ab5-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4ab5-117">-ApplicationGateway</span></span>
<span data-ttu-id="c4ab5-118">Указывает шлюз приложений, к которому этот командлет добавляет IP-конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="c4ab5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ab5-119">-DefaultProfile</span></span>
<span data-ttu-id="c4ab5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4ab5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4ab5-121">-Name</span></span>
<span data-ttu-id="c4ab5-122">Указывает имя конфигурации IP, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="c4ab5-123">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="c4ab5-123">-Subnet</span></span>
<span data-ttu-id="c4ab5-124">Указывает подсеть.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-124">Specifies a subnet.</span></span>
<span data-ttu-id="c4ab5-125">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="c4ab5-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c4ab5-126">-SubnetId</span></span>
<span data-ttu-id="c4ab5-127">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="c4ab5-128">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="c4ab5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ab5-129">CommonParameters</span></span>
<span data-ttu-id="c4ab5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ab5-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ab5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ab5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4ab5-132">INPUTS</span></span>

### <span data-ttu-id="c4ab5-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4ab5-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c4ab5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4ab5-134">OUTPUTS</span></span>

### <span data-ttu-id="c4ab5-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4ab5-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c4ab5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4ab5-136">NOTES</span></span>

## <span data-ttu-id="c4ab5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4ab5-137">RELATED LINKS</span></span>

[<span data-ttu-id="c4ab5-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4ab5-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c4ab5-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4ab5-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c4ab5-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4ab5-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c4ab5-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4ab5-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

