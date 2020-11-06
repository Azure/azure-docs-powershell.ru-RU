---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: cc84daecf4c98a48bb37ff0edd38f1136960a273
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566971"
---
# <span data-ttu-id="b8a91-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a91-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b8a91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8a91-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a91-103">Добавление IP-конфигурации к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="b8a91-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8a91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8a91-104">SYNTAX</span></span>

### <span data-ttu-id="b8a91-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8a91-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a91-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b8a91-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a91-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a91-107">DESCRIPTION</span></span>
<span data-ttu-id="b8a91-108">Командлет **Add-AzureRmApplicationGatewayIPConfiguration** добавляет конфигурацию IP-адресов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b8a91-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="b8a91-109">IP-конфигурации содержат подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b8a91-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="b8a91-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8a91-110">EXAMPLES</span></span>

### <span data-ttu-id="b8a91-111">Пример 1: Добавление конфигурации виртуальной сети к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="b8a91-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="b8a91-112">Первая команда создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b8a91-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="b8a91-113">Вторая команда создает подсеть, используя ранее созданную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b8a91-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="b8a91-114">Третья команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b8a91-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b8a91-115">Команда fouth добавляет конфигурацию IP-адресов в шлюз приложений, хранящийся в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b8a91-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b8a91-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8a91-116">PARAMETERS</span></span>

### <span data-ttu-id="b8a91-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8a91-117">-ApplicationGateway</span></span>
<span data-ttu-id="b8a91-118">Указывает шлюз приложений, к которому этот командлет добавляет IP-конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b8a91-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a91-119">-DefaultProfile</span></span>
<span data-ttu-id="b8a91-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a91-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8a91-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8a91-121">-Name</span></span>
<span data-ttu-id="b8a91-122">Указывает имя конфигурации IP, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="b8a91-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="b8a91-123">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="b8a91-123">-Subnet</span></span>
<span data-ttu-id="b8a91-124">Указывает подсеть.</span><span class="sxs-lookup"><span data-stu-id="b8a91-124">Specifies a subnet.</span></span>
<span data-ttu-id="b8a91-125">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b8a91-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="b8a91-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b8a91-126">-SubnetId</span></span>
<span data-ttu-id="b8a91-127">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="b8a91-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="b8a91-128">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b8a91-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="b8a91-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a91-129">CommonParameters</span></span>
<span data-ttu-id="b8a91-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8a91-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a91-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a91-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a91-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8a91-132">INPUTS</span></span>

### <span data-ttu-id="b8a91-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b8a91-133">System.String</span></span>

## <span data-ttu-id="b8a91-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a91-134">OUTPUTS</span></span>

### <span data-ttu-id="b8a91-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8a91-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8a91-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8a91-136">NOTES</span></span>

## <span data-ttu-id="b8a91-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8a91-137">RELATED LINKS</span></span>

[<span data-ttu-id="b8a91-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a91-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b8a91-139">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a91-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b8a91-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a91-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b8a91-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a91-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


