---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: a311d64fbdb086ca1d52ab5a1db725e278c6cc16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567454"
---
# <span data-ttu-id="a11d1-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a11d1-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="a11d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a11d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a11d1-103">Создание таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a11d1-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a11d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a11d1-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-DisableBgpRoutePropagation] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a11d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a11d1-105">DESCRIPTION</span></span>
<span data-ttu-id="a11d1-106">Командлет **New-AzureRmRouteTable** создает таблицу маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="a11d1-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="a11d1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a11d1-107">EXAMPLES</span></span>

### <span data-ttu-id="a11d1-108">Пример 1: создание таблицы маршрутов, содержащей маршрут</span><span class="sxs-lookup"><span data-stu-id="a11d1-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="a11d1-109">Первая команда создает маршрут с именем Route07 с помощью командлета New-AzureRmRouteConfig и сохраняет его в переменной $Route.</span><span class="sxs-lookup"><span data-stu-id="a11d1-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="a11d1-110">Этот маршрут перенаправляет пакеты в локальную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="a11d1-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="a11d1-111">Вторая команда создает таблицу маршрутов с именем RouteTable01 и добавляет в новую таблицу маршрут, хранящийся в $Route.</span><span class="sxs-lookup"><span data-stu-id="a11d1-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="a11d1-112">Команда определяет группу ресурсов, к которой принадлежит таблица, и расположение таблицы.</span><span class="sxs-lookup"><span data-stu-id="a11d1-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="a11d1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a11d1-113">PARAMETERS</span></span>

### <span data-ttu-id="a11d1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a11d1-114">-AsJob</span></span>
<span data-ttu-id="a11d1-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a11d1-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11d1-116">-DefaultProfile</span></span>
<span data-ttu-id="a11d1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a11d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a11d1-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="a11d1-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="a11d1-119">Отключить автоматическое распространение маршрутов BGP.</span><span class="sxs-lookup"><span data-stu-id="a11d1-119">Disable BGP Route auto propagation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a11d1-120">-Force</span></span>
<span data-ttu-id="a11d1-121">Указывает на то, что этот командлет создает таблицу маршрутов, даже если таблица маршрутов с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="a11d1-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a11d1-122">-Location</span></span>
<span data-ttu-id="a11d1-123">Указывает область Azure, в которой этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a11d1-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="a11d1-124">Дополнительные сведения можно найти в разделе [регионы Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="a11d1-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a11d1-125">-Name</span></span>
<span data-ttu-id="a11d1-126">Задает имя таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a11d1-126">Specifies a name for the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11d1-127">-ResourceGroupName</span></span>
<span data-ttu-id="a11d1-128">Указывает имя группы ресурсов, в которой этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a11d1-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-129">-Route</span><span class="sxs-lookup"><span data-stu-id="a11d1-129">-Route</span></span>
<span data-ttu-id="a11d1-130">Указывает массив объектов **маршрута** , которые нужно связать с таблицей маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a11d1-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="a11d1-131">-Tag</span></span>
<span data-ttu-id="a11d1-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a11d1-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a11d1-133">Например:</span><span class="sxs-lookup"><span data-stu-id="a11d1-133">For example:</span></span>

<span data-ttu-id="a11d1-134">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="a11d1-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a11d1-135">-Confirm</span></span>
<span data-ttu-id="a11d1-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a11d1-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a11d1-137">-WhatIf</span></span>
<span data-ttu-id="a11d1-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a11d1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a11d1-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a11d1-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11d1-140">CommonParameters</span></span>
<span data-ttu-id="a11d1-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a11d1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11d1-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a11d1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11d1-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a11d1-143">INPUTS</span></span>

### <span data-ttu-id="a11d1-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="a11d1-144">None</span></span>
<span data-ttu-id="a11d1-145">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a11d1-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a11d1-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a11d1-146">OUTPUTS</span></span>

### <span data-ttu-id="a11d1-147">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a11d1-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a11d1-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="a11d1-148">NOTES</span></span>

## <span data-ttu-id="a11d1-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a11d1-149">RELATED LINKS</span></span>

[<span data-ttu-id="a11d1-150">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a11d1-150">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="a11d1-151">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a11d1-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="a11d1-152">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a11d1-152">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="a11d1-153">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a11d1-153">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
