---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: ba5a389bd726822c24931fecb631f6c70cf7ce48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564235"
---
# <span data-ttu-id="b8762-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b8762-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="b8762-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8762-102">SYNOPSIS</span></span>
<span data-ttu-id="b8762-103">Создает маршрут для таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b8762-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8762-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8762-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8762-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8762-105">DESCRIPTION</span></span>
<span data-ttu-id="b8762-106">Командлет **New-AzureRmRouteConfig** создает маршрут для таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="b8762-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="b8762-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8762-107">EXAMPLES</span></span>

### <span data-ttu-id="b8762-108">Пример 1: создание маршрута</span><span class="sxs-lookup"><span data-stu-id="b8762-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="b8762-109">Первая команда создает маршрут с именем Route07 и сохраняет его в переменной $Route.</span><span class="sxs-lookup"><span data-stu-id="b8762-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="b8762-110">Этот маршрут перенаправляет пакеты в локальную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b8762-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="b8762-111">Вторая команда отображает свойства маршрута.</span><span class="sxs-lookup"><span data-stu-id="b8762-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="b8762-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8762-112">PARAMETERS</span></span>

### <span data-ttu-id="b8762-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b8762-113">-AddressPrefix</span></span>
<span data-ttu-id="b8762-114">Указывает место назначения в формате безклассной маршрутизации (CIDR), к которому применяется маршрут.</span><span class="sxs-lookup"><span data-stu-id="b8762-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8762-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8762-115">-DefaultProfile</span></span>
<span data-ttu-id="b8762-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8762-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8762-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8762-117">-Name</span></span>
<span data-ttu-id="b8762-118">Задает имя маршрута.</span><span class="sxs-lookup"><span data-stu-id="b8762-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="b8762-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b8762-119">-NextHopIpAddress</span></span>
<span data-ttu-id="b8762-120">Указывает IP-адрес виртуального устройства, добавляемого в сеть Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="b8762-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="b8762-121">Этот маршрут перенаправляет пакеты на этот адрес.</span><span class="sxs-lookup"><span data-stu-id="b8762-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="b8762-122">Указывайте этот параметр только в том случае, если для параметра *NextHopType* задано значение VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="b8762-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8762-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="b8762-123">-NextHopType</span></span>
<span data-ttu-id="b8762-124">Указывает, как этот маршрут перенаправляет пакеты.</span><span class="sxs-lookup"><span data-stu-id="b8762-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="b8762-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b8762-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8762-126">IIS.</span><span class="sxs-lookup"><span data-stu-id="b8762-126">Internet.</span></span>
<span data-ttu-id="b8762-127">Шлюз Интернета по умолчанию, предоставленный службой Azure.</span><span class="sxs-lookup"><span data-stu-id="b8762-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="b8762-128">Ничего.</span><span class="sxs-lookup"><span data-stu-id="b8762-128">None.</span></span>
<span data-ttu-id="b8762-129">Если указать это значение, маршрут не пересылает пакеты.</span><span class="sxs-lookup"><span data-stu-id="b8762-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="b8762-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="b8762-130">VirtualAppliance.</span></span>
<span data-ttu-id="b8762-131">Виртуальное устройство, добавляемое в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="b8762-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="b8762-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="b8762-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="b8762-133">Шлюз виртуальных частных сетей Azure "сервер-сервер".</span><span class="sxs-lookup"><span data-stu-id="b8762-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="b8762-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="b8762-134">VnetLocal.</span></span>
<span data-ttu-id="b8762-135">Локальная виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="b8762-135">The local virtual network.</span></span>
<span data-ttu-id="b8762-136">Если у вас есть две подсети, 10.1.0.0/16 и 10.2.0.0/16 в одной виртуальной сети, выберите значение VnetLocal для каждой подсети, чтобы переслать в другую подсеть.</span><span class="sxs-lookup"><span data-stu-id="b8762-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8762-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8762-137">-Confirm</span></span>
<span data-ttu-id="b8762-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8762-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8762-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8762-139">-WhatIf</span></span>
<span data-ttu-id="b8762-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8762-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8762-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8762-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8762-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8762-142">CommonParameters</span></span>
<span data-ttu-id="b8762-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8762-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8762-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8762-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8762-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8762-145">INPUTS</span></span>

### <span data-ttu-id="b8762-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b8762-146">System.String</span></span>

## <span data-ttu-id="b8762-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8762-147">OUTPUTS</span></span>

### <span data-ttu-id="b8762-148">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="b8762-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="b8762-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8762-149">NOTES</span></span>

## <span data-ttu-id="b8762-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8762-150">RELATED LINKS</span></span>

[<span data-ttu-id="b8762-151">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b8762-151">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="b8762-152">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b8762-152">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="b8762-153">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b8762-153">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="b8762-154">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b8762-154">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


