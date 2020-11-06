---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 7b28c50cfc53fee03d5715697a88e9356ea7664b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567583"
---
# <span data-ttu-id="de841-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="de841-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="de841-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de841-102">SYNOPSIS</span></span>
<span data-ttu-id="de841-103">Добавляет маршрут к таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="de841-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de841-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de841-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de841-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de841-105">DESCRIPTION</span></span>
<span data-ttu-id="de841-106">Командлет **Add-AzureRmRouteConfig** добавляет маршрут к таблице маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="de841-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="de841-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de841-107">EXAMPLES</span></span>

### <span data-ttu-id="de841-108">Пример 1: Добавление маршрута к таблице маршрутов</span><span class="sxs-lookup"><span data-stu-id="de841-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="de841-109">Первая команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="de841-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="de841-110">Эта команда хранит таблицу в переменной $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="de841-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="de841-111">Вторая команда добавляет маршрут с именем Route13 в таблицу маршрутов, хранящуюся в $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="de841-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="de841-112">Этот маршрут перенаправляет пакеты в локальную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="de841-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="de841-113">Пример 2: Добавление маршрута к таблице маршрутов с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="de841-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="de841-114">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="de841-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="de841-115">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="de841-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="de841-116">Текущий командлет добавляет маршрут с именем Route02 и передает результат в командлет **Set-AzureRmRouteTable** , который обновляет таблицу, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="de841-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="de841-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de841-117">PARAMETERS</span></span>

### <span data-ttu-id="de841-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="de841-118">-AddressPrefix</span></span>
<span data-ttu-id="de841-119">Указывает место назначения в формате безклассной маршрутизации (CIDR), к которому применяется маршрут.</span><span class="sxs-lookup"><span data-stu-id="de841-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="de841-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de841-120">-Name</span></span>
<span data-ttu-id="de841-121">Указывает имя маршрута, который нужно добавить в таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="de841-121">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="de841-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="de841-122">-NextHopIpAddress</span></span>
<span data-ttu-id="de841-123">Указывает IP-адрес виртуального устройства, добавляемого в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="de841-123">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="de841-124">Этот маршрут перенаправляет пакеты на этот адрес.</span><span class="sxs-lookup"><span data-stu-id="de841-124">This route forwards packets to that address.</span></span>
<span data-ttu-id="de841-125">Указывайте этот параметр только в том случае, если для параметра *NextHopType* задано значение VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="de841-125">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="de841-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="de841-126">-NextHopType</span></span>
<span data-ttu-id="de841-127">Указывает, как этот маршрут перенаправляет пакеты.</span><span class="sxs-lookup"><span data-stu-id="de841-127">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="de841-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="de841-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de841-129">IIS.</span><span class="sxs-lookup"><span data-stu-id="de841-129">Internet.</span></span>
<span data-ttu-id="de841-130">Шлюз Интернета по умолчанию, предоставленный службой Azure.</span><span class="sxs-lookup"><span data-stu-id="de841-130">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="de841-131">Ничего.</span><span class="sxs-lookup"><span data-stu-id="de841-131">None.</span></span>
<span data-ttu-id="de841-132">Если указать это значение, маршрут не пересылает пакеты.</span><span class="sxs-lookup"><span data-stu-id="de841-132">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="de841-133">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="de841-133">VirtualAppliance.</span></span>
<span data-ttu-id="de841-134">Виртуальное устройство, добавляемое в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="de841-134">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="de841-135">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="de841-135">VirtualNetworkGateway.</span></span>
<span data-ttu-id="de841-136">Шлюз виртуальных частных сетей Azure "сервер-сервер".</span><span class="sxs-lookup"><span data-stu-id="de841-136">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="de841-137">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="de841-137">VnetLocal.</span></span>
<span data-ttu-id="de841-138">Локальная виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="de841-138">The local virtual network.</span></span>
<span data-ttu-id="de841-139">Если у вас есть две подсети, 10.1.0.0/16 и 10.2.0.0/16 в одной виртуальной сети, выберите значение VnetLocal для каждой подсети, чтобы переслать в другую подсеть.</span><span class="sxs-lookup"><span data-stu-id="de841-139">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="de841-140">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="de841-140">-RouteTable</span></span>
<span data-ttu-id="de841-141">Указывает таблицу маршрутов, к которой этот командлет добавляет маршрут.</span><span class="sxs-lookup"><span data-stu-id="de841-141">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de841-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de841-142">-DefaultProfile</span></span>
<span data-ttu-id="de841-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de841-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de841-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de841-144">CommonParameters</span></span>
<span data-ttu-id="de841-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de841-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de841-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de841-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de841-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de841-147">INPUTS</span></span>

### <span data-ttu-id="de841-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="de841-148">PSRouteTable</span></span>
<span data-ttu-id="de841-149">Параметр "RouteTable" принимает значение типа "PSRouteTable" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="de841-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="de841-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de841-150">OUTPUTS</span></span>

### <span data-ttu-id="de841-151">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="de841-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="de841-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="de841-152">NOTES</span></span>

## <span data-ttu-id="de841-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de841-153">RELATED LINKS</span></span>

[<span data-ttu-id="de841-154">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="de841-154">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="de841-155">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="de841-155">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="de841-156">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="de841-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="de841-157">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="de841-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="de841-158">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="de841-158">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="de841-159">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="de841-159">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


