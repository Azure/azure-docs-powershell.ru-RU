---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 17661a05a970a9661543220c35b122638ddbc524
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982616"
---
# <span data-ttu-id="53b58-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53b58-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="53b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53b58-102">SYNOPSIS</span></span>
<span data-ttu-id="53b58-103">Добавляет конфигурацию IP-адреса к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="53b58-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="53b58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53b58-104">SYNTAX</span></span>

### <span data-ttu-id="53b58-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53b58-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b58-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="53b58-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53b58-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53b58-107">DESCRIPTION</span></span>
<span data-ttu-id="53b58-108">**Cmdlet Add-AzApplicationGatewayIPConfiguration** добавляет конфигурацию IP-адреса к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="53b58-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="53b58-109">Конфигурации IP-адресов содержат подсеть, в которой развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="53b58-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="53b58-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53b58-110">EXAMPLES</span></span>

### <span data-ttu-id="53b58-111">Пример 1. Добавление виртуальной конфигурации сети к шлюзу приложения</span><span class="sxs-lookup"><span data-stu-id="53b58-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="53b58-112">Первая команда получает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="53b58-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="53b58-113">Вторая команда создает подсеть, используя ранее созданную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="53b58-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="53b58-114">Третья команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="53b58-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="53b58-115">Четвертая команда добавляет конфигурацию IP-адреса к шлюзу приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="53b58-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="53b58-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53b58-116">PARAMETERS</span></span>

### <span data-ttu-id="53b58-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53b58-117">-ApplicationGateway</span></span>
<span data-ttu-id="53b58-118">Указывает шлюз приложения, к которому этот cmdlet добавляет конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="53b58-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="53b58-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b58-119">-DefaultProfile</span></span>
<span data-ttu-id="53b58-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53b58-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53b58-121">-Name</span><span class="sxs-lookup"><span data-stu-id="53b58-121">-Name</span></span>
<span data-ttu-id="53b58-122">Указывает имя добавляемой конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="53b58-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="53b58-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="53b58-123">-Subnet</span></span>
<span data-ttu-id="53b58-124">Указывает подсеть.</span><span class="sxs-lookup"><span data-stu-id="53b58-124">Specifies a subnet.</span></span>
<span data-ttu-id="53b58-125">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="53b58-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="53b58-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="53b58-126">-SubnetId</span></span>
<span data-ttu-id="53b58-127">Указывает ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="53b58-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="53b58-128">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="53b58-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="53b58-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b58-129">CommonParameters</span></span>
<span data-ttu-id="53b58-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b58-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b58-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b58-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b58-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53b58-132">INPUTS</span></span>

### <span data-ttu-id="53b58-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53b58-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53b58-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53b58-134">OUTPUTS</span></span>

### <span data-ttu-id="53b58-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53b58-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53b58-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53b58-136">NOTES</span></span>

## <span data-ttu-id="53b58-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53b58-137">RELATED LINKS</span></span>

[<span data-ttu-id="53b58-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53b58-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="53b58-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53b58-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="53b58-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53b58-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="53b58-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53b58-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


