---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: d3a309d99dff493e2440618d87c20b1a543e2ed9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913576"
---
# <span data-ttu-id="94d10-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="94d10-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="94d10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94d10-102">SYNOPSIS</span></span>
<span data-ttu-id="94d10-103">Изменение конфигурации IP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="94d10-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94d10-104">SYNTAX</span></span>

### <span data-ttu-id="94d10-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="94d10-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94d10-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="94d10-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94d10-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d10-107">DESCRIPTION</span></span>
<span data-ttu-id="94d10-108">Командлет **Set-AzureRmApplicationGatewayIPConfiguration** изменяет конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="94d10-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="94d10-109">Конфигурация IP содержит подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="94d10-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="94d10-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94d10-110">EXAMPLES</span></span>

### <span data-ttu-id="94d10-111">Пример 1: Установка состояния цели IP-конфигурации</span><span class="sxs-lookup"><span data-stu-id="94d10-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="94d10-112">Первая команда получает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="94d10-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="94d10-113">Вторая команда получает конфигурацию подсети с именем Subnet01 с помощью $VNet и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="94d10-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="94d10-114">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="94d10-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="94d10-115">Эта команда задает конфигурацию IP-конфигурации шлюза приложений, хранящейся в $AppGw, в конфигурации подсети, хранящейся в $Subnet.</span><span class="sxs-lookup"><span data-stu-id="94d10-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="94d10-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94d10-116">PARAMETERS</span></span>

### <span data-ttu-id="94d10-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94d10-117">-ApplicationGateway</span></span>
<span data-ttu-id="94d10-118">Указывает объект шлюза приложения, с которым этот командлет связывает конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="94d10-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="94d10-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d10-119">-DefaultProfile</span></span>
<span data-ttu-id="94d10-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94d10-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d10-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94d10-121">-Name</span></span>
<span data-ttu-id="94d10-122">Указывает имя конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="94d10-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="94d10-123">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="94d10-123">-Subnet</span></span>
<span data-ttu-id="94d10-124">Указывает подсеть.</span><span class="sxs-lookup"><span data-stu-id="94d10-124">Specifies the subnet.</span></span>
<span data-ttu-id="94d10-125">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="94d10-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="94d10-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="94d10-126">-SubnetId</span></span>
<span data-ttu-id="94d10-127">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="94d10-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="94d10-128">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="94d10-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="94d10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d10-129">CommonParameters</span></span>
<span data-ttu-id="94d10-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94d10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d10-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d10-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d10-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94d10-132">INPUTS</span></span>

### <span data-ttu-id="94d10-133">System. String</span><span class="sxs-lookup"><span data-stu-id="94d10-133">System.String</span></span>

## <span data-ttu-id="94d10-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d10-134">OUTPUTS</span></span>

### <span data-ttu-id="94d10-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94d10-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="94d10-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="94d10-136">NOTES</span></span>

## <span data-ttu-id="94d10-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94d10-137">RELATED LINKS</span></span>

[<span data-ttu-id="94d10-138">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="94d10-138">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="94d10-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="94d10-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="94d10-140">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="94d10-140">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="94d10-141">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="94d10-141">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="94d10-142">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="94d10-142">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


