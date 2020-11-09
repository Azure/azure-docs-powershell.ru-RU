---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318572"
---
# <span data-ttu-id="9f500-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="9f500-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f500-102">SYNOPSIS</span></span>
<span data-ttu-id="9f500-103">Изменение размера существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9f500-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="9f500-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f500-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f500-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f500-105">DESCRIPTION</span></span>
<span data-ttu-id="9f500-106">Командлет **resize-AzVirtualNetworkGateway** позволяет изменить единицу хранения (SKU) для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9f500-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="9f500-107">SKU определяет возможности шлюза, включая такие аспекты, как пропускная способность и максимальное количество разрешенных IP-туннелей.</span><span class="sxs-lookup"><span data-stu-id="9f500-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="9f500-108">Azure поддерживает базовые, стандартные, высокопроизводительные, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ и ErGw2AZ, ErGw3AZ SKU (иногда называются небольшим, средним и крупными SKU).</span><span class="sxs-lookup"><span data-stu-id="9f500-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="9f500-109">Подробные сведения о возможностях каждого типа SKU можно найти в разделе https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="9f500-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="9f500-110">Имейте в виду, что номера SKU отличаются в ценах и возможностях.</span><span class="sxs-lookup"><span data-stu-id="9f500-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="9f500-111">Дополнительные сведения можно найти в разделе https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="9f500-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="9f500-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f500-112">EXAMPLES</span></span>

### <span data-ttu-id="9f500-113">Пример 1: изменение размера шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="9f500-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="9f500-114">В этом примере изменяется размер шлюза виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="9f500-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="9f500-115">Первая команда создает ссылку на объект в ContosoVirtualGateway; Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="9f500-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="9f500-116">Вторая команда использует командлет **resize-AzVirtualNetworkGateway** , чтобы присвоить свойству *GatewaySku* значение Basic.</span><span class="sxs-lookup"><span data-stu-id="9f500-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="9f500-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f500-117">PARAMETERS</span></span>

### <span data-ttu-id="9f500-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f500-118">-DefaultProfile</span></span>
<span data-ttu-id="9f500-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f500-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f500-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="9f500-120">-GatewaySku</span></span>
<span data-ttu-id="9f500-121">Указывает новый тип SKU шлюза.</span><span class="sxs-lookup"><span data-stu-id="9f500-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="9f500-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9f500-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f500-123">Базового</span><span class="sxs-lookup"><span data-stu-id="9f500-123">Basic</span></span>
- <span data-ttu-id="9f500-124">Стандартная</span><span class="sxs-lookup"><span data-stu-id="9f500-124">Standard</span></span>
- <span data-ttu-id="9f500-125">Высокая производительность</span><span class="sxs-lookup"><span data-stu-id="9f500-125">High Performance</span></span>
- <span data-ttu-id="9f500-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="9f500-126">VpnGw1</span></span>
- <span data-ttu-id="9f500-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="9f500-127">VpnGw2</span></span>
- <span data-ttu-id="9f500-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="9f500-128">VpnGw3</span></span>
- <span data-ttu-id="9f500-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="9f500-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="9f500-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="9f500-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="9f500-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="9f500-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="9f500-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="9f500-132">ErGw1AZ</span></span> 
- <span data-ttu-id="9f500-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="9f500-133">ErGw2AZ</span></span> 
- <span data-ttu-id="9f500-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="9f500-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="9f500-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="9f500-136">Указывает ссылку на объект для изменения шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9f500-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="9f500-137">Вы можете создать ссылку на объект, используя Get-AzVirtualNetworkGateway и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="9f500-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="9f500-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f500-138">CommonParameters</span></span>
<span data-ttu-id="9f500-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f500-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f500-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f500-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f500-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f500-141">INPUTS</span></span>

### <span data-ttu-id="9f500-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="9f500-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9f500-143">System.String</span></span>

## <span data-ttu-id="9f500-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f500-144">OUTPUTS</span></span>

### <span data-ttu-id="9f500-145">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9f500-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f500-146">NOTES</span></span>
<span data-ttu-id="9f500-147">В новой конфигурации VpnGw1/VpnGw2/VpnGw3 SKU нельзя изменить размер из базовой/стандартной/HighPerformance SKU.</span><span class="sxs-lookup"><span data-stu-id="9f500-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="9f500-148">Дальнейшее изменение размера не разрешено для VpnGw1AZ/VpnGw2AZ/VpnGw3AZ или ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="9f500-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="9f500-149">Изменение размера разрешено только в пределах номера SKU, например, VpnGw1AZ можно изменить до и из VpnGw2AZ/VpnGw3AZ и ErGw1AZ можно изменить до/с ErGw2AZ или ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="9f500-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="9f500-150">Для получения инструкций ознакомьтесь с https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways инструкциями.</span><span class="sxs-lookup"><span data-stu-id="9f500-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="9f500-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f500-151">RELATED LINKS</span></span>

[<span data-ttu-id="9f500-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9f500-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9f500-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9f500-155">Сброс — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9f500-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f500-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9f500-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="9f500-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="9f500-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="9f500-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
