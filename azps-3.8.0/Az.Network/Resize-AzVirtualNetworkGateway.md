---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 31ec0453b0ce64c27d1bb37d4bf6c0f100a8c760
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411761"
---
# <span data-ttu-id="b2f16-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="b2f16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f16-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f16-103">Resizes an existing virtual network gateway.</span><span class="sxs-lookup"><span data-stu-id="b2f16-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="b2f16-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2f16-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2f16-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2f16-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f16-106">Командлет **Resize-AzVirtualNetworkGateway** позволяет изменить единицы управления акциями для виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="b2f16-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="b2f16-107">Номера номеров sk определяют возможности шлюза, в том числе пропускную способность и максимально допустимое количество разрешенных IP-туннельов.</span><span class="sxs-lookup"><span data-stu-id="b2f16-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="b2f16-108">Azure поддерживает базовые, стандартные, высокоскоростные, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (также называются небольшие, средние и большие СКА).</span><span class="sxs-lookup"><span data-stu-id="b2f16-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="b2f16-109">Подробные сведения о возможностях каждого типа SKU см. в https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="b2f16-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="b2f16-110">Помните о том, что цены и возможности СКАЙБ различаются.</span><span class="sxs-lookup"><span data-stu-id="b2f16-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="b2f16-111">Дополнительные сведения https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ см. в .</span><span class="sxs-lookup"><span data-stu-id="b2f16-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="b2f16-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2f16-112">EXAMPLES</span></span>

### <span data-ttu-id="b2f16-113">Пример 1. Изменение размера виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="b2f16-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="b2f16-114">В этом примере изменяется размер виртуального сетевого шлюза с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="b2f16-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="b2f16-115">Первая команда создает ссылку на объект ContosoVirtualGateway; эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="b2f16-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="b2f16-116">Вторая команда затем использует командлет **Resize-AzVirtualNetworkGateway** для свойства *GatewaySku* Basic.</span><span class="sxs-lookup"><span data-stu-id="b2f16-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="b2f16-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2f16-117">PARAMETERS</span></span>

### <span data-ttu-id="b2f16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f16-118">-DefaultProfile</span></span>
<span data-ttu-id="b2f16-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f16-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2f16-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="b2f16-120">-GatewaySku</span></span>
<span data-ttu-id="b2f16-121">Указывает новый тип SKU шлюза.</span><span class="sxs-lookup"><span data-stu-id="b2f16-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="b2f16-122">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b2f16-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2f16-123">Базовая</span><span class="sxs-lookup"><span data-stu-id="b2f16-123">Basic</span></span>
- <span data-ttu-id="b2f16-124">Стандартный</span><span class="sxs-lookup"><span data-stu-id="b2f16-124">Standard</span></span>
- <span data-ttu-id="b2f16-125">Высокая производительность</span><span class="sxs-lookup"><span data-stu-id="b2f16-125">High Performance</span></span>
- <span data-ttu-id="b2f16-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="b2f16-126">VpnGw1</span></span>
- <span data-ttu-id="b2f16-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="b2f16-127">VpnGw2</span></span>
- <span data-ttu-id="b2f16-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="b2f16-128">VpnGw3</span></span>
- <span data-ttu-id="b2f16-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="b2f16-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="b2f16-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="b2f16-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="b2f16-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="b2f16-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="b2f16-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="b2f16-132">ErGw1AZ</span></span> 
- <span data-ttu-id="b2f16-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="b2f16-133">ErGw2AZ</span></span> 
- <span data-ttu-id="b2f16-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="b2f16-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2f16-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b2f16-136">Указывает ссылку на объект на виртуальный сетевой шлюз, который нужно размеризировать.</span><span class="sxs-lookup"><span data-stu-id="b2f16-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="b2f16-137">Эту ссылку на объект можно создать, указав Get-AzVirtualNetworkGateway имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="b2f16-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2f16-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f16-138">CommonParameters</span></span>
<span data-ttu-id="b2f16-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f16-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f16-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f16-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f16-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2f16-141">INPUTS</span></span>

### <span data-ttu-id="b2f16-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b2f16-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b2f16-143">System.String</span></span>

## <span data-ttu-id="b2f16-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2f16-144">OUTPUTS</span></span>

### <span data-ttu-id="b2f16-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b2f16-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2f16-146">NOTES</span></span>
<span data-ttu-id="b2f16-147">Вы не можете 34-х новых СКАЙп Базовый, Стандартный или HighPerformance 2.</span><span class="sxs-lookup"><span data-stu-id="b2f16-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="b2f16-148">Для erGw1AZ/VpnGw2AZ/VpnGw3AZ или ErGw1AZ/ErGw1AZ/ErGw2AZ/ErGw3AZ не разрешается использовать дополнительные возможности.</span><span class="sxs-lookup"><span data-stu-id="b2f16-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="b2f16-149">Размер, допустимый только в рядах SKU, например, размер VPNGw1AZ можно использовать в vpnGw2AZ/VpnGw3AZ и ErGw1AZ, а также в ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="b2f16-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="b2f16-150">См. https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways инструкции.</span><span class="sxs-lookup"><span data-stu-id="b2f16-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="b2f16-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2f16-151">RELATED LINKS</span></span>

[<span data-ttu-id="b2f16-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b2f16-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b2f16-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b2f16-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b2f16-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b2f16-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b2f16-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="b2f16-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

