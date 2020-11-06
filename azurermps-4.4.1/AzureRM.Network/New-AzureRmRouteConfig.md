---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562464"
---
# <span data-ttu-id="04c06-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="04c06-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="04c06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04c06-102">SYNOPSIS</span></span>
<span data-ttu-id="04c06-103">Создает маршрут для таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="04c06-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04c06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04c06-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c06-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04c06-105">DESCRIPTION</span></span>
<span data-ttu-id="04c06-106">Командлет **New-AzureRmRouteConfig** создает маршрут для таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="04c06-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="04c06-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04c06-107">EXAMPLES</span></span>

### <span data-ttu-id="04c06-108">Пример 1: создание маршрута</span><span class="sxs-lookup"><span data-stu-id="04c06-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="04c06-109">Первая команда создает маршрут с именем Route07 и сохраняет его в переменной $Route.</span><span class="sxs-lookup"><span data-stu-id="04c06-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="04c06-110">Этот маршрут перенаправляет пакеты в локальную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="04c06-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="04c06-111">Вторая команда отображает свойства маршрута.</span><span class="sxs-lookup"><span data-stu-id="04c06-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="04c06-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04c06-112">PARAMETERS</span></span>

### <span data-ttu-id="04c06-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="04c06-113">-AddressPrefix</span></span>
<span data-ttu-id="04c06-114">Указывает место назначения в формате безклассной маршрутизации (CIDR), к которому применяется маршрут.</span><span class="sxs-lookup"><span data-stu-id="04c06-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c06-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04c06-115">-Name</span></span>
<span data-ttu-id="04c06-116">Задает имя маршрута.</span><span class="sxs-lookup"><span data-stu-id="04c06-116">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="04c06-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="04c06-117">-NextHopIpAddress</span></span>
<span data-ttu-id="04c06-118">Указывает IP-адрес виртуального устройства, добавляемого в сеть Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="04c06-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="04c06-119">Этот маршрут перенаправляет пакеты на этот адрес.</span><span class="sxs-lookup"><span data-stu-id="04c06-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="04c06-120">Указывайте этот параметр только в том случае, если для параметра *NextHopType* задано значение VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="04c06-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c06-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="04c06-121">-NextHopType</span></span>
<span data-ttu-id="04c06-122">Указывает, как этот маршрут перенаправляет пакеты.</span><span class="sxs-lookup"><span data-stu-id="04c06-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="04c06-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="04c06-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04c06-124">IIS.</span><span class="sxs-lookup"><span data-stu-id="04c06-124">Internet.</span></span>
<span data-ttu-id="04c06-125">Шлюз Интернета по умолчанию, предоставленный службой Azure.</span><span class="sxs-lookup"><span data-stu-id="04c06-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="04c06-126">Ничего.</span><span class="sxs-lookup"><span data-stu-id="04c06-126">None.</span></span>
<span data-ttu-id="04c06-127">Если указать это значение, маршрут не пересылает пакеты.</span><span class="sxs-lookup"><span data-stu-id="04c06-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="04c06-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="04c06-128">VirtualAppliance.</span></span>
<span data-ttu-id="04c06-129">Виртуальное устройство, добавляемое в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="04c06-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="04c06-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="04c06-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="04c06-131">Шлюз виртуальных частных сетей Azure "сервер-сервер".</span><span class="sxs-lookup"><span data-stu-id="04c06-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="04c06-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="04c06-132">VnetLocal.</span></span>
<span data-ttu-id="04c06-133">Локальная виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="04c06-133">The local virtual network.</span></span>
<span data-ttu-id="04c06-134">Если у вас есть две подсети, 10.1.0.0/16 и 10.2.0.0/16 в одной виртуальной сети, выберите значение VnetLocal для каждой подсети, чтобы переслать в другую подсеть.</span><span class="sxs-lookup"><span data-stu-id="04c06-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c06-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c06-135">-DefaultProfile</span></span>
<span data-ttu-id="04c06-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04c06-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04c06-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c06-137">CommonParameters</span></span>
<span data-ttu-id="04c06-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04c06-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c06-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04c06-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c06-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04c06-140">INPUTS</span></span>

## <span data-ttu-id="04c06-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04c06-141">OUTPUTS</span></span>

### <span data-ttu-id="04c06-142">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="04c06-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="04c06-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="04c06-143">NOTES</span></span>

## <span data-ttu-id="04c06-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04c06-144">RELATED LINKS</span></span>

[<span data-ttu-id="04c06-145">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="04c06-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="04c06-146">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="04c06-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="04c06-147">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="04c06-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="04c06-148">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="04c06-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


