---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ca7335abfd8fe2dc9591dcb7d96fb6ca71dda4fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393116"
---
# <span data-ttu-id="b4783-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b4783-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="b4783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4783-102">SYNOPSIS</span></span>
<span data-ttu-id="b4783-103">Обновляет конфигурацию маршрутов для таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b4783-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="b4783-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4783-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4783-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4783-105">DESCRIPTION</span></span>
<span data-ttu-id="b4783-106">Для таблицы маршрутов сетет **Set-AzRouteConfig** обновляет конфигурацию маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b4783-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="b4783-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4783-107">EXAMPLES</span></span>

### <span data-ttu-id="b4783-108">Пример 1. Изменение маршрута</span><span class="sxs-lookup"><span data-stu-id="b4783-108">Example 1: Modify a route</span></span>
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

<span data-ttu-id="b4783-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью Get-AzRouteTable командлета.</span><span class="sxs-lookup"><span data-stu-id="b4783-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="b4783-110">Эта команда передает эту таблицу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="b4783-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4783-111">Текущий cmdlet изменяет маршрут Route02, а затем передает результат в **cmdlet Set-AzRouteTable,** который обновляет таблицу с учетом внесенных изменений.</span><span class="sxs-lookup"><span data-stu-id="b4783-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="b4783-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4783-112">PARAMETERS</span></span>

### <span data-ttu-id="b4783-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4783-113">-AddressPrefix</span></span>
<span data-ttu-id="b4783-114">Определяет место назначения в CIDR формате CIDR, к которому применяется маршрут.</span><span class="sxs-lookup"><span data-stu-id="b4783-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="b4783-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4783-115">-DefaultProfile</span></span>
<span data-ttu-id="b4783-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4783-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4783-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b4783-117">-Name</span></span>
<span data-ttu-id="b4783-118">Указывает имя маршрута, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4783-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b4783-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4783-119">-NextHopIpAddress</span></span>
<span data-ttu-id="b4783-120">Определяет IP-адрес виртуального устройства, который вы добавляете в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="b4783-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="b4783-121">Этот маршрут передает пакеты на этот адрес.</span><span class="sxs-lookup"><span data-stu-id="b4783-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="b4783-122">Укажите этот параметр, только если укажите значение VirtualAppliance для *параметра NextHopType.*</span><span class="sxs-lookup"><span data-stu-id="b4783-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="b4783-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="b4783-123">-NextHopType</span></span>
<span data-ttu-id="b4783-124">Определяет, как этот маршрут передает пакеты.</span><span class="sxs-lookup"><span data-stu-id="b4783-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="b4783-125">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="b4783-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4783-126">Интернет.</span><span class="sxs-lookup"><span data-stu-id="b4783-126">Internet.</span></span>
<span data-ttu-id="b4783-127">Стандартный шлюз Интернета, предоставляемый Azure.</span><span class="sxs-lookup"><span data-stu-id="b4783-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="b4783-128">Нет.</span><span class="sxs-lookup"><span data-stu-id="b4783-128">None.</span></span>
<span data-ttu-id="b4783-129">Если указать это значение, маршрут не будет перенадвигать пакеты.</span><span class="sxs-lookup"><span data-stu-id="b4783-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="b4783-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="b4783-130">VirtualAppliance.</span></span>
<span data-ttu-id="b4783-131">Виртуальная устройство, которую вы добавляете в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="b4783-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="b4783-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="b4783-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="b4783-133">Виртуальный частный сетевой шлюз Azureserver-to-server.</span><span class="sxs-lookup"><span data-stu-id="b4783-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="b4783-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="b4783-134">VnetLocal.</span></span>
<span data-ttu-id="b4783-135">Локализованная виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="b4783-135">The local virtual network.</span></span>
<span data-ttu-id="b4783-136">Если в одной виртуальной сети есть две подсети: 10.1.0.0/16 и 10.2.0.0/16, выберите значение VnetLocal для каждой подсети, чтобы она перенаполала в другую.</span><span class="sxs-lookup"><span data-stu-id="b4783-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="b4783-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b4783-137">-RouteTable</span></span>
<span data-ttu-id="b4783-138">Определяет таблицу маршрутов, с которой связан этот маршрут.</span><span class="sxs-lookup"><span data-stu-id="b4783-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="b4783-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4783-139">-Confirm</span></span>
<span data-ttu-id="b4783-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4783-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4783-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4783-141">-WhatIf</span></span>
<span data-ttu-id="b4783-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4783-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4783-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4783-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4783-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4783-144">CommonParameters</span></span>
<span data-ttu-id="b4783-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4783-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4783-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4783-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4783-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4783-147">INPUTS</span></span>

### <span data-ttu-id="b4783-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4783-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="b4783-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b4783-149">System.String</span></span>

## <span data-ttu-id="b4783-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4783-150">OUTPUTS</span></span>

### <span data-ttu-id="b4783-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4783-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="b4783-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4783-152">NOTES</span></span>

## <span data-ttu-id="b4783-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4783-153">RELATED LINKS</span></span>

[<span data-ttu-id="b4783-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b4783-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="b4783-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b4783-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="b4783-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b4783-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="b4783-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b4783-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


