---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: ac7b370a6a10aff5a9524a2536b5f4dedaff5a9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903590"
---
# <span data-ttu-id="546b0-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="546b0-101">New-AzRouteTable</span></span>

## <span data-ttu-id="546b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="546b0-102">SYNOPSIS</span></span>
<span data-ttu-id="546b0-103">Создание таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="546b0-103">Creates a route table.</span></span>

## <span data-ttu-id="546b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="546b0-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="546b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="546b0-105">DESCRIPTION</span></span>
<span data-ttu-id="546b0-106">Командлет **New-AzRouteTable** создает таблицу маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="546b0-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="546b0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="546b0-107">EXAMPLES</span></span>

### <span data-ttu-id="546b0-108">Пример 1: создание таблицы маршрутов, содержащей маршрут</span><span class="sxs-lookup"><span data-stu-id="546b0-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="546b0-109">Первая команда создает маршрут с именем Route07 с помощью командлета New-AzRouteConfig и сохраняет его в переменной $Route.</span><span class="sxs-lookup"><span data-stu-id="546b0-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="546b0-110">Этот маршрут перенаправляет пакеты в локальную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="546b0-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="546b0-111">Вторая команда создает таблицу маршрутов с именем RouteTable01 и добавляет в новую таблицу маршрут, хранящийся в $Route.</span><span class="sxs-lookup"><span data-stu-id="546b0-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="546b0-112">Команда определяет группу ресурсов, к которой принадлежит таблица, и расположение таблицы.</span><span class="sxs-lookup"><span data-stu-id="546b0-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="546b0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="546b0-113">PARAMETERS</span></span>

### <span data-ttu-id="546b0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="546b0-114">-AsJob</span></span>
<span data-ttu-id="546b0-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="546b0-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546b0-116">-DefaultProfile</span></span>
<span data-ttu-id="546b0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="546b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="546b0-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="546b0-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="546b0-119">Отключить автоматическое распространение маршрутов BGP.</span><span class="sxs-lookup"><span data-stu-id="546b0-119">Disable BGP Route auto propagation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="546b0-120">-Force</span></span>
<span data-ttu-id="546b0-121">Указывает на то, что этот командлет создает таблицу маршрутов, даже если таблица маршрутов с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="546b0-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-122">-Location</span><span class="sxs-lookup"><span data-stu-id="546b0-122">-Location</span></span>
<span data-ttu-id="546b0-123">Указывает область Azure, в которой этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="546b0-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="546b0-124">Дополнительные сведения можно найти в разделе [регионы Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="546b0-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="546b0-125">-Name</span></span>
<span data-ttu-id="546b0-126">Задает имя таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="546b0-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="546b0-128">Указывает имя группы ресурсов, в которой этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="546b0-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-129">-Route</span><span class="sxs-lookup"><span data-stu-id="546b0-129">-Route</span></span>
<span data-ttu-id="546b0-130">Указывает массив объектов **маршрута** , которые нужно связать с таблицей маршрутов.</span><span class="sxs-lookup"><span data-stu-id="546b0-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="546b0-131">-Tag</span></span>
<span data-ttu-id="546b0-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="546b0-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="546b0-133">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="546b0-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="546b0-134">-Confirm</span></span>
<span data-ttu-id="546b0-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="546b0-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="546b0-136">-WhatIf</span></span>
<span data-ttu-id="546b0-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="546b0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="546b0-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="546b0-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546b0-139">CommonParameters</span></span>
<span data-ttu-id="546b0-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="546b0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546b0-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546b0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546b0-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="546b0-142">INPUTS</span></span>

### <span data-ttu-id="546b0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="546b0-143">System.String</span></span>

### <span data-ttu-id="546b0-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="546b0-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="546b0-145">Microsoft. Azure. Commands. Network. Models. PSRoute []</span><span class="sxs-lookup"><span data-stu-id="546b0-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="546b0-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="546b0-146">OUTPUTS</span></span>

### <span data-ttu-id="546b0-147">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="546b0-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="546b0-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="546b0-148">NOTES</span></span>

## <span data-ttu-id="546b0-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="546b0-149">RELATED LINKS</span></span>

[<span data-ttu-id="546b0-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="546b0-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="546b0-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="546b0-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="546b0-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="546b0-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="546b0-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="546b0-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
