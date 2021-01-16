---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329142"
---
# <span data-ttu-id="bed87-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bed87-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="bed87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed87-102">SYNOPSIS</span></span>
<span data-ttu-id="bed87-103">Добавляет конфигурацию IP-адреса к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="bed87-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="bed87-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bed87-104">SYNTAX</span></span>

### <span data-ttu-id="bed87-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bed87-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bed87-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bed87-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed87-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bed87-107">DESCRIPTION</span></span>
<span data-ttu-id="bed87-108">**Cmdlet Add-AzApplicationGatewayIPConfiguration** добавляет конфигурацию IP-адреса к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="bed87-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="bed87-109">Конфигурации IP-адресов содержат подсеть, в которой развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="bed87-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="bed87-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bed87-110">EXAMPLES</span></span>

### <span data-ttu-id="bed87-111">Пример 1. Добавление виртуальной конфигурации сети к шлюзу приложения</span><span class="sxs-lookup"><span data-stu-id="bed87-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="bed87-112">Первая команда получает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="bed87-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="bed87-113">Вторая команда создает подсеть, используя ранее созданную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="bed87-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="bed87-114">Третья команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bed87-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bed87-115">Четвертая команда добавляет конфигурацию IP-адреса к шлюзу приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bed87-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="bed87-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bed87-116">PARAMETERS</span></span>

### <span data-ttu-id="bed87-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bed87-117">-ApplicationGateway</span></span>
<span data-ttu-id="bed87-118">Указывает шлюз приложения, к которому этот cmdlet добавляет конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="bed87-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="bed87-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed87-119">-DefaultProfile</span></span>
<span data-ttu-id="bed87-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bed87-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bed87-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bed87-121">-Name</span></span>
<span data-ttu-id="bed87-122">Указывает имя добавляемой конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="bed87-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="bed87-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="bed87-123">-Subnet</span></span>
<span data-ttu-id="bed87-124">Указывает подсеть.</span><span class="sxs-lookup"><span data-stu-id="bed87-124">Specifies a subnet.</span></span>
<span data-ttu-id="bed87-125">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="bed87-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="bed87-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bed87-126">-SubnetId</span></span>
<span data-ttu-id="bed87-127">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="bed87-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="bed87-128">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="bed87-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="bed87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed87-129">CommonParameters</span></span>
<span data-ttu-id="bed87-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed87-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bed87-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed87-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bed87-132">INPUTS</span></span>

### <span data-ttu-id="bed87-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bed87-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bed87-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bed87-134">OUTPUTS</span></span>

### <span data-ttu-id="bed87-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bed87-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bed87-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bed87-136">NOTES</span></span>

## <span data-ttu-id="bed87-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bed87-137">RELATED LINKS</span></span>

[<span data-ttu-id="bed87-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bed87-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bed87-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bed87-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bed87-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bed87-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bed87-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bed87-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


