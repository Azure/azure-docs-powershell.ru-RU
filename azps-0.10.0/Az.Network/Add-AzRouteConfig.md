---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 1afd855be89f83e9591bbd180b1357e1b03952eb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910128"
---
# <span data-ttu-id="f5f37-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5f37-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="f5f37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5f37-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f37-103">Добавляет маршрут к таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f5f37-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="f5f37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5f37-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5f37-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5f37-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f37-106">Командлет **Add-AzRouteConfig** добавляет маршрут к таблице маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f37-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="f5f37-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5f37-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f37-108">Пример 1: Добавление маршрута к таблице маршрутов</span><span class="sxs-lookup"><span data-stu-id="f5f37-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="f5f37-109">Первая команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета Get-AzRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f5f37-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="f5f37-110">Эта команда хранит таблицу в переменной $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="f5f37-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="f5f37-111">Вторая команда добавляет маршрут с именем Route13 в таблицу маршрутов, хранящуюся в $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="f5f37-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="f5f37-112">Этот маршрут перенаправляет пакеты в локальную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="f5f37-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="f5f37-113">Пример 2: Добавление маршрута к таблице маршрутов с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="f5f37-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="f5f37-114">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью **Get-AzRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="f5f37-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="f5f37-115">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f5f37-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5f37-116">Текущий командлет добавляет маршрут с именем Route02 и передает результат в командлет **Set-AzRouteTable** , который обновляет таблицу, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="f5f37-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="f5f37-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5f37-117">PARAMETERS</span></span>

### <span data-ttu-id="f5f37-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f5f37-118">-AddressPrefix</span></span>
<span data-ttu-id="f5f37-119">Указывает место назначения в формате безклассной маршрутизации (CIDR), к которому применяется маршрут.</span><span class="sxs-lookup"><span data-stu-id="f5f37-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f37-120">-DefaultProfile</span></span>
<span data-ttu-id="f5f37-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f37-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5f37-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5f37-122">-Name</span></span>
<span data-ttu-id="f5f37-123">Указывает имя маршрута, который нужно добавить в таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f5f37-123">Specifies a name of the route to add to the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f37-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5f37-124">-NextHopIpAddress</span></span>
<span data-ttu-id="f5f37-125">Указывает IP-адрес виртуального устройства, добавляемого в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f37-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="f5f37-126">Этот маршрут перенаправляет пакеты на этот адрес.</span><span class="sxs-lookup"><span data-stu-id="f5f37-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="f5f37-127">Указывайте этот параметр только в том случае, если для параметра *NextHopType* задано значение VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="f5f37-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f37-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="f5f37-128">-NextHopType</span></span>
<span data-ttu-id="f5f37-129">Указывает, как этот маршрут перенаправляет пакеты.</span><span class="sxs-lookup"><span data-stu-id="f5f37-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="f5f37-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f5f37-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5f37-131">IIS.</span><span class="sxs-lookup"><span data-stu-id="f5f37-131">Internet.</span></span>
<span data-ttu-id="f5f37-132">Шлюз Интернета по умолчанию, предоставленный службой Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f37-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="f5f37-133">Ничего.</span><span class="sxs-lookup"><span data-stu-id="f5f37-133">None.</span></span>
<span data-ttu-id="f5f37-134">Если указать это значение, маршрут не пересылает пакеты.</span><span class="sxs-lookup"><span data-stu-id="f5f37-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="f5f37-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="f5f37-135">VirtualAppliance.</span></span>
<span data-ttu-id="f5f37-136">Виртуальное устройство, добавляемое в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f37-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="f5f37-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="f5f37-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="f5f37-138">Шлюз виртуальных частных сетей Azure "сервер-сервер".</span><span class="sxs-lookup"><span data-stu-id="f5f37-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="f5f37-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="f5f37-139">VnetLocal.</span></span>
<span data-ttu-id="f5f37-140">Локальная виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="f5f37-140">The local virtual network.</span></span>
<span data-ttu-id="f5f37-141">Если у вас есть две подсети, 10.1.0.0/16 и 10.2.0.0/16 в одной виртуальной сети, выберите значение VnetLocal для каждой подсети, чтобы переслать в другую подсеть.</span><span class="sxs-lookup"><span data-stu-id="f5f37-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f37-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f5f37-142">-RouteTable</span></span>
<span data-ttu-id="f5f37-143">Указывает таблицу маршрутов, к которой этот командлет добавляет маршрут.</span><span class="sxs-lookup"><span data-stu-id="f5f37-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f37-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5f37-144">-Confirm</span></span>
<span data-ttu-id="f5f37-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f5f37-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f37-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f37-146">-WhatIf</span></span>
<span data-ttu-id="f5f37-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f5f37-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5f37-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5f37-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f37-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f37-149">CommonParameters</span></span>
<span data-ttu-id="f5f37-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5f37-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f37-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f37-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f37-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5f37-152">INPUTS</span></span>

### <span data-ttu-id="f5f37-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5f37-153">PSRouteTable</span></span>
<span data-ttu-id="f5f37-154">Параметр "RouteTable" принимает значение типа "PSRouteTable" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f5f37-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="f5f37-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5f37-155">OUTPUTS</span></span>

### <span data-ttu-id="f5f37-156">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5f37-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f5f37-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5f37-157">NOTES</span></span>

## <span data-ttu-id="f5f37-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5f37-158">RELATED LINKS</span></span>

[<span data-ttu-id="f5f37-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5f37-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="f5f37-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5f37-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="f5f37-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5f37-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="f5f37-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5f37-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="f5f37-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5f37-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="f5f37-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5f37-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


