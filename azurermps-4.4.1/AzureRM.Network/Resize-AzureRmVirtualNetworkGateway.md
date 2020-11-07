---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 9f7b85ed3c8f7c1c64ec89f8575975dde81fed7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735147"
---
# <span data-ttu-id="0d14b-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0d14b-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="0d14b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d14b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d14b-103">Изменение размера существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0d14b-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d14b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d14b-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d14b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d14b-105">DESCRIPTION</span></span>
<span data-ttu-id="0d14b-106">Командлет **resize-AzureRmVirtualNetworkGateway** позволяет изменить единицу хранения (SKU) для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0d14b-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="0d14b-107">SKU определяет возможности шлюза, включая такие аспекты, как пропускная способность и максимальное количество разрешенных IP-туннелей.</span><span class="sxs-lookup"><span data-stu-id="0d14b-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="0d14b-108">Azure поддерживает базовые и стандартные, высокопроизводительные, VpnGw1, VpnGw2 и VpnGw3 SKU (иногда называются небольшим, средним и крупными SKU).</span><span class="sxs-lookup"><span data-stu-id="0d14b-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="0d14b-109">Подробные сведения о возможностях каждого типа SKU можно найти в разделе https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="0d14b-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="0d14b-110">Имейте в виду, что номера SKU отличаются в ценах и возможностях.</span><span class="sxs-lookup"><span data-stu-id="0d14b-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="0d14b-111">Дополнительные сведения можно найти в разделе https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="0d14b-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="0d14b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d14b-112">EXAMPLES</span></span>

### <span data-ttu-id="0d14b-113">Пример 1: изменение размера шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="0d14b-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="0d14b-114">В этом примере изменяется размер шлюза виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="0d14b-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="0d14b-115">Первая команда создает ссылку на объект в ContosoVirtualGateway; Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="0d14b-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="0d14b-116">Вторая команда использует командлет **resize-AzureRmVirtualNetworkGateway** , чтобы присвоить свойству *GatewaySku* значение Basic.</span><span class="sxs-lookup"><span data-stu-id="0d14b-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="0d14b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d14b-117">PARAMETERS</span></span>

### <span data-ttu-id="0d14b-118">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="0d14b-118">-GatewaySku</span></span>
<span data-ttu-id="0d14b-119">Указывает новый тип SKU шлюза.</span><span class="sxs-lookup"><span data-stu-id="0d14b-119">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="0d14b-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d14b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d14b-121">Базового</span><span class="sxs-lookup"><span data-stu-id="0d14b-121">Basic</span></span>
- <span data-ttu-id="0d14b-122">Стандартная</span><span class="sxs-lookup"><span data-stu-id="0d14b-122">Standard</span></span>
- <span data-ttu-id="0d14b-123">Высокая производительность</span><span class="sxs-lookup"><span data-stu-id="0d14b-123">High Performance</span></span>
- <span data-ttu-id="0d14b-124">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="0d14b-124">VpnGw1</span></span>
- <span data-ttu-id="0d14b-125">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="0d14b-125">VpnGw2</span></span>
- <span data-ttu-id="0d14b-126">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="0d14b-126">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d14b-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0d14b-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="0d14b-128">Указывает ссылку на объект для изменения шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0d14b-128">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="0d14b-129">Вы можете создать ссылку на объект, используя Get-AzureRmVirtualNetworkGateway и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="0d14b-129">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="0d14b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d14b-130">-DefaultProfile</span></span>
<span data-ttu-id="0d14b-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d14b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d14b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d14b-132">CommonParameters</span></span>
<span data-ttu-id="0d14b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d14b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d14b-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d14b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d14b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d14b-135">INPUTS</span></span>

###  
<span data-ttu-id="0d14b-136">Этот командлет принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="0d14b-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="0d14b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d14b-137">OUTPUTS</span></span>

###  
<span data-ttu-id="0d14b-138">Этот командлет изменяет существующие экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="0d14b-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="0d14b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d14b-139">NOTES</span></span>
<span data-ttu-id="0d14b-140">В новой конфигурации VpnGw1/VpnGw2/VpnGw3 SKU нельзя изменить размер из базовой/стандартной/HighPerformance SKU.</span><span class="sxs-lookup"><span data-stu-id="0d14b-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="0d14b-141">Для получения инструкций ознакомьтесь с https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways инструкциями.</span><span class="sxs-lookup"><span data-stu-id="0d14b-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="0d14b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d14b-142">RELATED LINKS</span></span>

[<span data-ttu-id="0d14b-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="0d14b-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="0d14b-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0d14b-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="0d14b-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="0d14b-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


