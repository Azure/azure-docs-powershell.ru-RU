---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: f4ef683b65967fe694713b7990d23eb173f02163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562447"
---
# <span data-ttu-id="2159b-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2159b-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="2159b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2159b-102">SYNOPSIS</span></span>
<span data-ttu-id="2159b-103">Создание таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2159b-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2159b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2159b-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -Location <String>
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2159b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2159b-105">DESCRIPTION</span></span>
<span data-ttu-id="2159b-106">Командлет **New-AzureRmRouteTable** создает таблицу маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="2159b-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="2159b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2159b-107">EXAMPLES</span></span>

### <span data-ttu-id="2159b-108">Пример 1: создание таблицы маршрутов, содержащей маршрут</span><span class="sxs-lookup"><span data-stu-id="2159b-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="2159b-109">Первая команда создает маршрут с именем Route07 с помощью командлета New-AzureRmRouteConfig и сохраняет его в переменной $Route.</span><span class="sxs-lookup"><span data-stu-id="2159b-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="2159b-110">Этот маршрут перенаправляет пакеты в локальную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="2159b-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="2159b-111">Вторая команда создает таблицу маршрутов с именем RouteTable01 и добавляет в новую таблицу маршрут, хранящийся в $Route.</span><span class="sxs-lookup"><span data-stu-id="2159b-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="2159b-112">Команда определяет группу ресурсов, к которой принадлежит таблица, и расположение таблицы.</span><span class="sxs-lookup"><span data-stu-id="2159b-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="2159b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2159b-113">PARAMETERS</span></span>

### <span data-ttu-id="2159b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2159b-114">-Force</span></span>
<span data-ttu-id="2159b-115">Указывает на то, что этот командлет создает таблицу маршрутов, даже если таблица маршрутов с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="2159b-115">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="2159b-116">-Location</span><span class="sxs-lookup"><span data-stu-id="2159b-116">-Location</span></span>
<span data-ttu-id="2159b-117">Указывает область Azure, в которой этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2159b-117">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="2159b-118">Дополнительные сведения можно найти в разделе [регионы Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="2159b-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="2159b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2159b-119">-Name</span></span>
<span data-ttu-id="2159b-120">Задает имя таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2159b-120">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="2159b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2159b-121">-ResourceGroupName</span></span>
<span data-ttu-id="2159b-122">Указывает имя группы ресурсов, в которой этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2159b-122">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="2159b-123">-Route</span><span class="sxs-lookup"><span data-stu-id="2159b-123">-Route</span></span>
<span data-ttu-id="2159b-124">Указывает массив объектов **маршрута** , которые нужно связать с таблицей маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2159b-124">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="2159b-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="2159b-125">-Tag</span></span>
<span data-ttu-id="2159b-126">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2159b-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2159b-127">Например:</span><span class="sxs-lookup"><span data-stu-id="2159b-127">For example:</span></span>

<span data-ttu-id="2159b-128">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2159b-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2159b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2159b-129">-Confirm</span></span>
<span data-ttu-id="2159b-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2159b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2159b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2159b-131">-WhatIf</span></span>
<span data-ttu-id="2159b-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2159b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2159b-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2159b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2159b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2159b-134">-DefaultProfile</span></span>
<span data-ttu-id="2159b-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2159b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2159b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2159b-136">CommonParameters</span></span>
<span data-ttu-id="2159b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2159b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2159b-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2159b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2159b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2159b-139">INPUTS</span></span>

## <span data-ttu-id="2159b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2159b-140">OUTPUTS</span></span>

### <span data-ttu-id="2159b-141">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2159b-141">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2159b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2159b-142">NOTES</span></span>

## <span data-ttu-id="2159b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2159b-143">RELATED LINKS</span></span>

[<span data-ttu-id="2159b-144">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2159b-144">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="2159b-145">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2159b-145">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="2159b-146">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2159b-146">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="2159b-147">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2159b-147">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
