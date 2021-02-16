---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 326baa91b8da8f9bae67cf47dcc69246549d7c06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237073"
---
# <span data-ttu-id="377b9-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="377b9-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="377b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="377b9-102">SYNOPSIS</span></span>
<span data-ttu-id="377b9-103">Добавляет маршрут в таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="377b9-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="377b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="377b9-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="377b9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="377b9-105">DESCRIPTION</span></span>
<span data-ttu-id="377b9-106">С **его использованием** можно добавить маршрут в таблицу маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="377b9-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="377b9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="377b9-107">EXAMPLES</span></span>

### <span data-ttu-id="377b9-108">Пример 1. Добавление маршрута в таблицу маршрутов</span><span class="sxs-lookup"><span data-stu-id="377b9-108">Example 1: Add a route to a route table</span></span>
```powershell
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="377b9-109">Первая команда получает таблицу маршрутов с именем RouteTable01 с помощью Get-AzRouteTable командлета.</span><span class="sxs-lookup"><span data-stu-id="377b9-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="377b9-110">Команда сохраняет таблицу в переменной $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="377b9-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="377b9-111">Вторая команда добавляет маршрут "Маршрут13" в таблицу маршрутов, $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="377b9-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="377b9-112">Этот маршрут передает пакеты в локализованную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="377b9-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="377b9-113">Пример 2. Добавление маршрутов в таблицу маршрутов с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="377b9-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```powershell
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

<span data-ttu-id="377b9-114">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью **Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="377b9-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="377b9-115">Эта команда передает эту таблицу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="377b9-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="377b9-116">Текущий cmdlet добавляет маршрут Route02, а затем передает результат в **cmdlet Set-AzRouteTable,** который обновляет таблицу с учетом изменений.</span><span class="sxs-lookup"><span data-stu-id="377b9-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="377b9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="377b9-117">PARAMETERS</span></span>

### <span data-ttu-id="377b9-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="377b9-118">-AddressPrefix</span></span>
<span data-ttu-id="377b9-119">Определяет место назначения в CIDR формате CIDR, к которому применяется маршрут.</span><span class="sxs-lookup"><span data-stu-id="377b9-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="377b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377b9-120">-DefaultProfile</span></span>
<span data-ttu-id="377b9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="377b9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="377b9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="377b9-122">-Name</span></span>
<span data-ttu-id="377b9-123">Указывает имя маршрута, который нужно добавить в таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="377b9-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="377b9-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="377b9-124">-NextHopIpAddress</span></span>
<span data-ttu-id="377b9-125">Определяет IP-адрес виртуального устройства, который вы добавляете в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="377b9-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="377b9-126">Этот маршрут передает пакеты на этот адрес.</span><span class="sxs-lookup"><span data-stu-id="377b9-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="377b9-127">Укажите этот параметр только в том случае, если для параметра *NextHopType* задано значение VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="377b9-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="377b9-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="377b9-128">-NextHopType</span></span>
<span data-ttu-id="377b9-129">Определяет, как этот маршрут передает пакеты.</span><span class="sxs-lookup"><span data-stu-id="377b9-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="377b9-130">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="377b9-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="377b9-131">Интернет.</span><span class="sxs-lookup"><span data-stu-id="377b9-131">Internet.</span></span>
<span data-ttu-id="377b9-132">Стандартный шлюз Интернета, предоставляемый Azure.</span><span class="sxs-lookup"><span data-stu-id="377b9-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="377b9-133">Нет.</span><span class="sxs-lookup"><span data-stu-id="377b9-133">None.</span></span>
<span data-ttu-id="377b9-134">Если указать это значение, маршрут не будет перенаад значит, что пакеты перена являются маршрутами.</span><span class="sxs-lookup"><span data-stu-id="377b9-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="377b9-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="377b9-135">VirtualAppliance.</span></span>
<span data-ttu-id="377b9-136">Виртуальная устройство, добавляемая в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="377b9-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="377b9-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="377b9-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="377b9-138">Виртуальный частный сетевой шлюз Azure "сервер-сервер"</span><span class="sxs-lookup"><span data-stu-id="377b9-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="377b9-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="377b9-139">VnetLocal.</span></span>
<span data-ttu-id="377b9-140">Локализованная виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="377b9-140">The local virtual network.</span></span>
<span data-ttu-id="377b9-141">Если в одной виртуальной сети есть две подсети: 10.1.0.0/16 и 10.2.0.0/16, выберите значение VnetLocal для каждой подсети, чтобы она перенаполала в другую.</span><span class="sxs-lookup"><span data-stu-id="377b9-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="377b9-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="377b9-142">-RouteTable</span></span>
<span data-ttu-id="377b9-143">Определяет таблицу маршрутов, в которую этот cmdlet добавляет маршрут.</span><span class="sxs-lookup"><span data-stu-id="377b9-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="377b9-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="377b9-144">-Confirm</span></span>
<span data-ttu-id="377b9-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="377b9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="377b9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="377b9-146">-WhatIf</span></span>
<span data-ttu-id="377b9-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="377b9-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="377b9-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="377b9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="377b9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377b9-149">CommonParameters</span></span>
<span data-ttu-id="377b9-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="377b9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377b9-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="377b9-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377b9-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="377b9-152">INPUTS</span></span>

### <span data-ttu-id="377b9-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="377b9-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="377b9-154">System.String</span><span class="sxs-lookup"><span data-stu-id="377b9-154">System.String</span></span>

## <span data-ttu-id="377b9-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="377b9-155">OUTPUTS</span></span>

### <span data-ttu-id="377b9-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="377b9-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="377b9-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="377b9-157">NOTES</span></span>

## <span data-ttu-id="377b9-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="377b9-158">RELATED LINKS</span></span>

[<span data-ttu-id="377b9-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="377b9-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="377b9-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="377b9-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="377b9-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="377b9-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="377b9-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="377b9-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="377b9-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="377b9-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="377b9-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="377b9-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


