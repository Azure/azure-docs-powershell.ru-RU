---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: 6898077b20223339ed1e8be46ca9eb213e58ffa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560848"
---
# <span data-ttu-id="54d28-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="54d28-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="54d28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54d28-102">SYNOPSIS</span></span>
<span data-ttu-id="54d28-103">Задает состояние цели для маршрута.</span><span class="sxs-lookup"><span data-stu-id="54d28-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54d28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54d28-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>]
 [-NextHopType <String>] [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d28-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54d28-105">DESCRIPTION</span></span>
<span data-ttu-id="54d28-106">Командлет **Set-AzureRmRouteConfig** задает состояние цели для маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="54d28-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="54d28-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54d28-107">EXAMPLES</span></span>

### <span data-ttu-id="54d28-108">Пример 1: изменение маршрута</span><span class="sxs-lookup"><span data-stu-id="54d28-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="54d28-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="54d28-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="54d28-110">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="54d28-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="54d28-111">Текущий командлет изменяет маршрут с именем Route02 и передает результат в командлет **Set-AzureRmRouteTable** , который обновляет таблицу, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="54d28-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="54d28-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54d28-112">PARAMETERS</span></span>

### <span data-ttu-id="54d28-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="54d28-113">-AddressPrefix</span></span>
<span data-ttu-id="54d28-114">Указывает место назначения в формате безклассной маршрутизации (CIDR), к которому применяется маршрут.</span><span class="sxs-lookup"><span data-stu-id="54d28-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="54d28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d28-115">-DefaultProfile</span></span>
<span data-ttu-id="54d28-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54d28-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54d28-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54d28-117">-Name</span></span>
<span data-ttu-id="54d28-118">Указывает имя маршрута, измененного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="54d28-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="54d28-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="54d28-119">-NextHopIpAddress</span></span>
<span data-ttu-id="54d28-120">Указывает IP-адрес виртуального устройства, добавляемого в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="54d28-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="54d28-121">Этот маршрут перенаправляет пакеты на этот адрес.</span><span class="sxs-lookup"><span data-stu-id="54d28-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="54d28-122">Указывайте этот параметр только в том случае, если для параметра *NextHopType* задано значение VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="54d28-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="54d28-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="54d28-123">-NextHopType</span></span>
<span data-ttu-id="54d28-124">Указывает, как этот маршрут перенаправляет пакеты.</span><span class="sxs-lookup"><span data-stu-id="54d28-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="54d28-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="54d28-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54d28-126">IIS.</span><span class="sxs-lookup"><span data-stu-id="54d28-126">Internet.</span></span>
<span data-ttu-id="54d28-127">Шлюз Интернета по умолчанию, предоставленный службой Azure.</span><span class="sxs-lookup"><span data-stu-id="54d28-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="54d28-128">Ничего.</span><span class="sxs-lookup"><span data-stu-id="54d28-128">None.</span></span>
<span data-ttu-id="54d28-129">Если указать это значение, маршрут не пересылает пакеты.</span><span class="sxs-lookup"><span data-stu-id="54d28-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="54d28-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="54d28-130">VirtualAppliance.</span></span>
<span data-ttu-id="54d28-131">Виртуальное устройство, добавляемое в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="54d28-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="54d28-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="54d28-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="54d28-133">Шлюз виртуальных частных сетей с Azureserver на сервер.</span><span class="sxs-lookup"><span data-stu-id="54d28-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="54d28-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="54d28-134">VnetLocal.</span></span>
<span data-ttu-id="54d28-135">Локальная виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="54d28-135">The local virtual network.</span></span>
<span data-ttu-id="54d28-136">Если у вас есть две подсети, 10.1.0.0/16 и 10.2.0.0/16 в одной виртуальной сети, выберите значение VnetLocal для каждой подсети, чтобы переслать в другую подсеть.</span><span class="sxs-lookup"><span data-stu-id="54d28-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="54d28-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="54d28-137">-RouteTable</span></span>
<span data-ttu-id="54d28-138">Указывает таблицу маршрутов, с которой связан этот маршрут.</span><span class="sxs-lookup"><span data-stu-id="54d28-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54d28-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54d28-139">-Confirm</span></span>
<span data-ttu-id="54d28-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54d28-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d28-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d28-141">-WhatIf</span></span>
<span data-ttu-id="54d28-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54d28-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54d28-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54d28-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d28-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d28-144">CommonParameters</span></span>
<span data-ttu-id="54d28-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54d28-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d28-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d28-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d28-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54d28-147">INPUTS</span></span>

### <span data-ttu-id="54d28-148">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="54d28-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="54d28-149">System. String</span><span class="sxs-lookup"><span data-stu-id="54d28-149">System.String</span></span>

## <span data-ttu-id="54d28-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54d28-150">OUTPUTS</span></span>

### <span data-ttu-id="54d28-151">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="54d28-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="54d28-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="54d28-152">NOTES</span></span>

## <span data-ttu-id="54d28-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54d28-153">RELATED LINKS</span></span>

[<span data-ttu-id="54d28-154">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="54d28-154">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="54d28-155">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="54d28-155">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="54d28-156">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="54d28-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="54d28-157">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="54d28-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


