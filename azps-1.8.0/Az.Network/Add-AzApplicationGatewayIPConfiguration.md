---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c8dd9faf54d92f34b523292a8b25465978074ad5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730740"
---
# <span data-ttu-id="d8115-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8115-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d8115-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8115-102">SYNOPSIS</span></span>
<span data-ttu-id="d8115-103">Добавление IP-конфигурации к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="d8115-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="d8115-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8115-104">SYNTAX</span></span>

### <span data-ttu-id="d8115-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8115-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8115-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d8115-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8115-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8115-107">DESCRIPTION</span></span>
<span data-ttu-id="d8115-108">Командлет **Add-AzApplicationGatewayIPConfiguration** добавляет конфигурацию IP-адресов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="d8115-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="d8115-109">IP-конфигурации содержат подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="d8115-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="d8115-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8115-110">EXAMPLES</span></span>

### <span data-ttu-id="d8115-111">Пример 1: Добавление конфигурации виртуальной сети к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="d8115-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="d8115-112">Первая команда получает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="d8115-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="d8115-113">Вторая команда получает подсеть, используя ранее созданную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="d8115-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="d8115-114">Третья команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d8115-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d8115-115">Команда fouth добавляет конфигурацию IP-адресов в шлюз приложений, хранящийся в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d8115-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d8115-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8115-116">PARAMETERS</span></span>

### <span data-ttu-id="d8115-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8115-117">-ApplicationGateway</span></span>
<span data-ttu-id="d8115-118">Указывает шлюз приложений, к которому этот командлет добавляет IP-конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d8115-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="d8115-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8115-119">-DefaultProfile</span></span>
<span data-ttu-id="d8115-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8115-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8115-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8115-121">-Name</span></span>
<span data-ttu-id="d8115-122">Указывает имя конфигурации IP, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="d8115-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="d8115-123">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="d8115-123">-Subnet</span></span>
<span data-ttu-id="d8115-124">Указывает подсеть.</span><span class="sxs-lookup"><span data-stu-id="d8115-124">Specifies a subnet.</span></span>
<span data-ttu-id="d8115-125">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="d8115-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="d8115-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d8115-126">-SubnetId</span></span>
<span data-ttu-id="d8115-127">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="d8115-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="d8115-128">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="d8115-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="d8115-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8115-129">CommonParameters</span></span>
<span data-ttu-id="d8115-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8115-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8115-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8115-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8115-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8115-132">INPUTS</span></span>

### <span data-ttu-id="d8115-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8115-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8115-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8115-134">OUTPUTS</span></span>

### <span data-ttu-id="d8115-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8115-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8115-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8115-136">NOTES</span></span>

## <span data-ttu-id="d8115-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8115-137">RELATED LINKS</span></span>

[<span data-ttu-id="d8115-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8115-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d8115-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8115-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d8115-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8115-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d8115-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8115-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


