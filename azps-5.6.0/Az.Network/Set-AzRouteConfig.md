---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: a4cdcbf52dfb20f0282347d5dc1ce9a5aec14da0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990923"
---
# <span data-ttu-id="89f55-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="89f55-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="89f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89f55-102">SYNOPSIS</span></span>
<span data-ttu-id="89f55-103">Обновляет конфигурацию маршрутов для таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="89f55-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="89f55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89f55-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89f55-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89f55-105">DESCRIPTION</span></span>
<span data-ttu-id="89f55-106">Для **таблицы маршрутов cmdlet Set-AzRouteConfig** обновляет конфигурацию маршрутов.</span><span class="sxs-lookup"><span data-stu-id="89f55-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="89f55-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89f55-107">EXAMPLES</span></span>

### <span data-ttu-id="89f55-108">Пример 1. Изменение маршрута</span><span class="sxs-lookup"><span data-stu-id="89f55-108">Example 1: Modify a route</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
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

<span data-ttu-id="89f55-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью Get-AzRouteTable командлета.</span><span class="sxs-lookup"><span data-stu-id="89f55-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="89f55-110">Эта команда передает эту таблицу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="89f55-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="89f55-111">Текущий cmdlet изменяет маршрут Route02, а затем передает результат в **cmdlet Set-AzRouteTable,** который обновляет таблицу с учетом внесенных изменений.</span><span class="sxs-lookup"><span data-stu-id="89f55-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="89f55-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89f55-112">PARAMETERS</span></span>

### <span data-ttu-id="89f55-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="89f55-113">-AddressPrefix</span></span>
<span data-ttu-id="89f55-114">Определяет место назначения в CIDR формате CIDR, к которому применяется маршрут.</span><span class="sxs-lookup"><span data-stu-id="89f55-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="89f55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f55-115">-DefaultProfile</span></span>
<span data-ttu-id="89f55-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89f55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89f55-117">-Name</span><span class="sxs-lookup"><span data-stu-id="89f55-117">-Name</span></span>
<span data-ttu-id="89f55-118">Указывает имя маршрута, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f55-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="89f55-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="89f55-119">-NextHopIpAddress</span></span>
<span data-ttu-id="89f55-120">Определяет IP-адрес виртуального устройства, который вы добавляете в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="89f55-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="89f55-121">Этот маршрут передает пакеты на этот адрес.</span><span class="sxs-lookup"><span data-stu-id="89f55-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="89f55-122">Укажите этот параметр, только если укажите значение VirtualAppliance для *параметра NextHopType.*</span><span class="sxs-lookup"><span data-stu-id="89f55-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="89f55-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="89f55-123">-NextHopType</span></span>
<span data-ttu-id="89f55-124">Определяет, как этот маршрут передает пакеты.</span><span class="sxs-lookup"><span data-stu-id="89f55-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="89f55-125">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="89f55-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89f55-126">Интернет.</span><span class="sxs-lookup"><span data-stu-id="89f55-126">Internet.</span></span>
<span data-ttu-id="89f55-127">Стандартный шлюз Интернета, предоставляемый Azure.</span><span class="sxs-lookup"><span data-stu-id="89f55-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="89f55-128">Нет.</span><span class="sxs-lookup"><span data-stu-id="89f55-128">None.</span></span>
<span data-ttu-id="89f55-129">Если указать это значение, маршрут не будет перенаад значит, что пакеты перена являются маршрутами.</span><span class="sxs-lookup"><span data-stu-id="89f55-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="89f55-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="89f55-130">VirtualAppliance.</span></span>
<span data-ttu-id="89f55-131">Виртуальная устройство, добавляемая в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="89f55-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="89f55-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="89f55-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="89f55-133">Виртуальный частный сетевой шлюз Azureserver-to-server.</span><span class="sxs-lookup"><span data-stu-id="89f55-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="89f55-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="89f55-134">VnetLocal.</span></span>
<span data-ttu-id="89f55-135">Локализованная виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="89f55-135">The local virtual network.</span></span>
<span data-ttu-id="89f55-136">Если в одной виртуальной сети есть две подсети: 10.1.0.0/16 и 10.2.0.0/16, выберите значение VnetLocal для каждой подсети, чтобы она перенаполала в другую.</span><span class="sxs-lookup"><span data-stu-id="89f55-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="89f55-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="89f55-137">-RouteTable</span></span>
<span data-ttu-id="89f55-138">Определяет таблицу маршрутов, с которой связан этот маршрут.</span><span class="sxs-lookup"><span data-stu-id="89f55-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="89f55-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89f55-139">-Confirm</span></span>
<span data-ttu-id="89f55-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f55-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f55-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f55-141">-WhatIf</span></span>
<span data-ttu-id="89f55-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f55-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89f55-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89f55-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f55-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f55-144">CommonParameters</span></span>
<span data-ttu-id="89f55-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f55-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f55-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f55-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f55-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89f55-147">INPUTS</span></span>

### <span data-ttu-id="89f55-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="89f55-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="89f55-149">System.String</span><span class="sxs-lookup"><span data-stu-id="89f55-149">System.String</span></span>

## <span data-ttu-id="89f55-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89f55-150">OUTPUTS</span></span>

### <span data-ttu-id="89f55-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="89f55-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="89f55-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89f55-152">NOTES</span></span>

## <span data-ttu-id="89f55-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89f55-153">RELATED LINKS</span></span>

[<span data-ttu-id="89f55-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="89f55-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="89f55-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="89f55-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="89f55-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="89f55-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="89f55-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="89f55-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


