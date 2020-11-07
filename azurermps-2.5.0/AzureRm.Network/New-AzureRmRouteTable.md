---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9ba23a33e82e003413172240264ef8485b12d4e0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914837"
---
# <span data-ttu-id="468b0-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b0-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="468b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="468b0-102">SYNOPSIS</span></span>
<span data-ttu-id="468b0-103">Создание таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="468b0-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="468b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="468b0-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="468b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="468b0-105">DESCRIPTION</span></span>
<span data-ttu-id="468b0-106">Командлет **New-AzureRmRouteTable** создает таблицу маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="468b0-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="468b0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="468b0-107">EXAMPLES</span></span>

### <span data-ttu-id="468b0-108">Пример 1: создание таблицы маршрутов, содержащей маршрут</span><span class="sxs-lookup"><span data-stu-id="468b0-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="468b0-109">Первая команда создает маршрут с именем Route07 с помощью командлета New-AzureRmRouteConfig и сохраняет его в переменной $Route.</span><span class="sxs-lookup"><span data-stu-id="468b0-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="468b0-110">Этот маршрут перенаправляет пакеты в локальную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="468b0-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="468b0-111">Вторая команда создает таблицу маршрутов с именем RouteTable01 и добавляет в новую таблицу маршрут, хранящийся в $Route.</span><span class="sxs-lookup"><span data-stu-id="468b0-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="468b0-112">Команда определяет группу ресурсов, к которой принадлежит таблица, и расположение таблицы.</span><span class="sxs-lookup"><span data-stu-id="468b0-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="468b0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="468b0-113">PARAMETERS</span></span>

### <span data-ttu-id="468b0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="468b0-114">-AsJob</span></span>
<span data-ttu-id="468b0-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="468b0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="468b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468b0-116">-DefaultProfile</span></span>
<span data-ttu-id="468b0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="468b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="468b0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="468b0-118">-Force</span></span>
<span data-ttu-id="468b0-119">Указывает на то, что этот командлет создает таблицу маршрутов, даже если таблица маршрутов с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="468b0-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="468b0-120">-Location</span><span class="sxs-lookup"><span data-stu-id="468b0-120">-Location</span></span>
<span data-ttu-id="468b0-121">Указывает область Azure, в которой этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="468b0-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="468b0-122">Дополнительные сведения можно найти в разделе [регионы Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="468b0-122">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="468b0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="468b0-123">-Name</span></span>
<span data-ttu-id="468b0-124">Задает имя таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="468b0-124">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="468b0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468b0-125">-ResourceGroupName</span></span>
<span data-ttu-id="468b0-126">Указывает имя группы ресурсов, в которой этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="468b0-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="468b0-127">-Route</span><span class="sxs-lookup"><span data-stu-id="468b0-127">-Route</span></span>
<span data-ttu-id="468b0-128">Указывает массив объектов **маршрута** , которые нужно связать с таблицей маршрутов.</span><span class="sxs-lookup"><span data-stu-id="468b0-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="468b0-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="468b0-129">-Tag</span></span>
<span data-ttu-id="468b0-130">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="468b0-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="468b0-131">Например:</span><span class="sxs-lookup"><span data-stu-id="468b0-131">For example:</span></span>

<span data-ttu-id="468b0-132">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="468b0-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="468b0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="468b0-133">-Confirm</span></span>
<span data-ttu-id="468b0-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="468b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="468b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="468b0-135">-WhatIf</span></span>
<span data-ttu-id="468b0-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="468b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="468b0-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="468b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="468b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468b0-138">CommonParameters</span></span>
<span data-ttu-id="468b0-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="468b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468b0-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="468b0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468b0-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="468b0-141">INPUTS</span></span>

## <span data-ttu-id="468b0-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="468b0-142">OUTPUTS</span></span>

### <span data-ttu-id="468b0-143">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b0-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="468b0-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="468b0-144">NOTES</span></span>

## <span data-ttu-id="468b0-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="468b0-145">RELATED LINKS</span></span>

[<span data-ttu-id="468b0-146">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b0-146">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="468b0-147">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="468b0-147">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="468b0-148">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b0-148">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="468b0-149">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b0-149">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
