---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911088"
---
# <span data-ttu-id="15bc0-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15bc0-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="15bc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="15bc0-103">Изменение размера существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="15bc0-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="15bc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15bc0-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15bc0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="15bc0-106">Командлет **resize-AzVirtualNetworkGateway** позволяет изменить единицу хранения (SKU) для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="15bc0-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="15bc0-107">SKU определяет возможности шлюза, включая такие аспекты, как пропускная способность и максимальное количество разрешенных IP-туннелей.</span><span class="sxs-lookup"><span data-stu-id="15bc0-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="15bc0-108">Azure поддерживает базовые и стандартные, высокопроизводительные, VpnGw1, VpnGw2 и VpnGw3 SKU (иногда называются небольшим, средним и крупными SKU).</span><span class="sxs-lookup"><span data-stu-id="15bc0-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="15bc0-109">Подробные сведения о возможностях каждого типа SKU можно найти в разделе https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="15bc0-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="15bc0-110">Имейте в виду, что номера SKU отличаются в ценах и возможностях.</span><span class="sxs-lookup"><span data-stu-id="15bc0-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="15bc0-111">Дополнительные сведения можно найти в разделе https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="15bc0-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="15bc0-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15bc0-112">EXAMPLES</span></span>

### <span data-ttu-id="15bc0-113">Пример 1: изменение размера шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="15bc0-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="15bc0-114">В этом примере изменяется размер шлюза виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="15bc0-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="15bc0-115">Первая команда создает ссылку на объект в ContosoVirtualGateway; Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="15bc0-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="15bc0-116">Вторая команда использует командлет **resize-AzVirtualNetworkGateway** , чтобы присвоить свойству *GatewaySku* значение Basic.</span><span class="sxs-lookup"><span data-stu-id="15bc0-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="15bc0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15bc0-117">PARAMETERS</span></span>

### <span data-ttu-id="15bc0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bc0-118">-DefaultProfile</span></span>
<span data-ttu-id="15bc0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15bc0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15bc0-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="15bc0-120">-GatewaySku</span></span>
<span data-ttu-id="15bc0-121">Указывает новый тип SKU шлюза.</span><span class="sxs-lookup"><span data-stu-id="15bc0-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="15bc0-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="15bc0-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15bc0-123">Базового</span><span class="sxs-lookup"><span data-stu-id="15bc0-123">Basic</span></span>
- <span data-ttu-id="15bc0-124">Стандартная</span><span class="sxs-lookup"><span data-stu-id="15bc0-124">Standard</span></span>
- <span data-ttu-id="15bc0-125">Высокая производительность</span><span class="sxs-lookup"><span data-stu-id="15bc0-125">High Performance</span></span>
- <span data-ttu-id="15bc0-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="15bc0-126">VpnGw1</span></span>
- <span data-ttu-id="15bc0-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="15bc0-127">VpnGw2</span></span>
- <span data-ttu-id="15bc0-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="15bc0-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bc0-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15bc0-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="15bc0-130">Указывает ссылку на объект для изменения шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="15bc0-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="15bc0-131">Вы можете создать ссылку на объект, используя Get-AzVirtualNetworkGateway и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="15bc0-131">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15bc0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bc0-132">CommonParameters</span></span>
<span data-ttu-id="15bc0-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15bc0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bc0-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15bc0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bc0-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15bc0-135">INPUTS</span></span>

###  
<span data-ttu-id="15bc0-136">Этот командлет принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="15bc0-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="15bc0-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15bc0-137">OUTPUTS</span></span>

###  
<span data-ttu-id="15bc0-138">Этот командлет изменяет существующие экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="15bc0-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="15bc0-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="15bc0-139">NOTES</span></span>
<span data-ttu-id="15bc0-140">В новой конфигурации VpnGw1/VpnGw2/VpnGw3 SKU нельзя изменить размер из базовой/стандартной/HighPerformance SKU.</span><span class="sxs-lookup"><span data-stu-id="15bc0-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="15bc0-141">Для получения инструкций ознакомьтесь с https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways инструкциями.</span><span class="sxs-lookup"><span data-stu-id="15bc0-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="15bc0-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15bc0-142">RELATED LINKS</span></span>

[<span data-ttu-id="15bc0-143">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="15bc0-143">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="15bc0-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15bc0-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="15bc0-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="15bc0-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


