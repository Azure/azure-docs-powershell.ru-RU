---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568444"
---
# <span data-ttu-id="5213d-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5213d-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="5213d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5213d-102">SYNOPSIS</span></span>
<span data-ttu-id="5213d-103">Изменение размера существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5213d-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5213d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5213d-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5213d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5213d-105">DESCRIPTION</span></span>
<span data-ttu-id="5213d-106">Командлет **resize-AzureRmVirtualNetworkGateway** позволяет изменить единицу хранения (SKU) для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5213d-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="5213d-107">SKU определяет возможности шлюза, включая такие аспекты, как пропускная способность и максимальное количество разрешенных IP-туннелей.</span><span class="sxs-lookup"><span data-stu-id="5213d-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="5213d-108">Azure поддерживает базовые, стандартные, высокопроизводительные, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ и ErGw2AZ, ErGw3AZ SKU (иногда называются небольшим, средним и крупными SKU).</span><span class="sxs-lookup"><span data-stu-id="5213d-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="5213d-109">Подробные сведения о возможностях каждого типа SKU можно найти в разделе https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="5213d-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="5213d-110">Имейте в виду, что номера SKU отличаются в ценах и возможностях.</span><span class="sxs-lookup"><span data-stu-id="5213d-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="5213d-111">Дополнительные сведения можно найти в разделе https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="5213d-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="5213d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5213d-112">EXAMPLES</span></span>

### <span data-ttu-id="5213d-113">Пример 1: изменение размера шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="5213d-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="5213d-114">В этом примере изменяется размер шлюза виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5213d-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="5213d-115">Первая команда создает ссылку на объект в ContosoVirtualGateway; Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="5213d-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="5213d-116">Вторая команда использует командлет **resize-AzureRmVirtualNetworkGateway** , чтобы присвоить свойству *GatewaySku* значение Basic.</span><span class="sxs-lookup"><span data-stu-id="5213d-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="5213d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5213d-117">PARAMETERS</span></span>

### <span data-ttu-id="5213d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5213d-118">-DefaultProfile</span></span>
<span data-ttu-id="5213d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5213d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5213d-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="5213d-120">-GatewaySku</span></span>
<span data-ttu-id="5213d-121">Указывает новый тип SKU шлюза.</span><span class="sxs-lookup"><span data-stu-id="5213d-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="5213d-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5213d-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5213d-123">Базового</span><span class="sxs-lookup"><span data-stu-id="5213d-123">Basic</span></span>
- <span data-ttu-id="5213d-124">Стандартная</span><span class="sxs-lookup"><span data-stu-id="5213d-124">Standard</span></span>
- <span data-ttu-id="5213d-125">Высокая производительность</span><span class="sxs-lookup"><span data-stu-id="5213d-125">High Performance</span></span>
- <span data-ttu-id="5213d-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="5213d-126">VpnGw1</span></span>
- <span data-ttu-id="5213d-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="5213d-127">VpnGw2</span></span>
- <span data-ttu-id="5213d-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="5213d-128">VpnGw3</span></span>
- <span data-ttu-id="5213d-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="5213d-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="5213d-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="5213d-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="5213d-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="5213d-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="5213d-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="5213d-132">ErGw1AZ</span></span> 
- <span data-ttu-id="5213d-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="5213d-133">ErGw2AZ</span></span> 
- <span data-ttu-id="5213d-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="5213d-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="5213d-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5213d-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5213d-136">Указывает ссылку на объект для изменения шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5213d-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="5213d-137">Вы можете создать ссылку на объект, используя Get-AzureRmVirtualNetworkGateway и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="5213d-137">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="5213d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5213d-138">CommonParameters</span></span>
<span data-ttu-id="5213d-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5213d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5213d-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5213d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5213d-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5213d-141">INPUTS</span></span>

### <span data-ttu-id="5213d-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5213d-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="5213d-143">Параметры: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5213d-143">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="5213d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5213d-144">System.String</span></span>

## <span data-ttu-id="5213d-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5213d-145">OUTPUTS</span></span>

### <span data-ttu-id="5213d-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5213d-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5213d-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="5213d-147">NOTES</span></span>
<span data-ttu-id="5213d-148">В новой конфигурации VpnGw1/VpnGw2/VpnGw3 SKU нельзя изменить размер из базовой/стандартной/HighPerformance SKU.</span><span class="sxs-lookup"><span data-stu-id="5213d-148">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="5213d-149">Дальнейшее изменение размера не разрешено для VpnGw1AZ/VpnGw2AZ/VpnGw3AZ или ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="5213d-149">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="5213d-150">Изменение размера разрешено только в пределах номера SKU, например, VpnGw1AZ можно изменить до и из VpnGw2AZ/VpnGw3AZ и ErGw1AZ можно изменить до/с ErGw2AZ или ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="5213d-150">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="5213d-151">Для получения инструкций ознакомьтесь с https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways инструкциями.</span><span class="sxs-lookup"><span data-stu-id="5213d-151">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="5213d-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5213d-152">RELATED LINKS</span></span>

[<span data-ttu-id="5213d-153">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="5213d-153">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="5213d-154">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5213d-154">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="5213d-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="5213d-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


