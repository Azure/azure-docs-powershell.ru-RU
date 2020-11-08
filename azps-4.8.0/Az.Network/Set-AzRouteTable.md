---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: bd419d3b6ec55af885a0f05b7be5c5de269fccdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235980"
---
# <span data-ttu-id="18b4b-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="18b4b-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="18b4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="18b4b-103">Обновляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="18b4b-103">Updates a route table.</span></span>

## <span data-ttu-id="18b4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18b4b-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18b4b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="18b4b-106">Командлет **Set-AzRouteTable** обновляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="18b4b-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="18b4b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18b4b-107">EXAMPLES</span></span>

### <span data-ttu-id="18b4b-108">Пример 1: обновление таблицы маршрутов путем добавления к ней конфигурации маршрута</span><span class="sxs-lookup"><span data-stu-id="18b4b-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
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

<span data-ttu-id="18b4b-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета Get-AzRouteTable.</span><span class="sxs-lookup"><span data-stu-id="18b4b-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="18b4b-110">Команда передает эту таблицу командлету Add-AzRouteConfig с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="18b4b-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="18b4b-111">**Add-AzRouteConfig** добавляет маршрут с именем Route07, а затем передает результат в текущий командлет, который обновляет таблицу, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="18b4b-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="18b4b-112">Пример 2: изменение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="18b4b-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="18b4b-113">Первая команда получает таблицу маршрутов с именем rtName и сохраняет ее в переменной $rt.</span><span class="sxs-lookup"><span data-stu-id="18b4b-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="18b4b-114">Вторая команда отображает значение DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="18b4b-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="18b4b-115">Третья команда обновляет значение DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="18b4b-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="18b4b-116">Четвертая команда обновляет таблицу маршрутов на сервере.</span><span class="sxs-lookup"><span data-stu-id="18b4b-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="18b4b-117">Пятая команда получает обновленную таблицу маршрутов и сохраняет ее в переменной $rt.</span><span class="sxs-lookup"><span data-stu-id="18b4b-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="18b4b-118">Шестая команда отображает значение DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="18b4b-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="18b4b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18b4b-119">PARAMETERS</span></span>

### <span data-ttu-id="18b4b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18b4b-120">-AsJob</span></span>
<span data-ttu-id="18b4b-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="18b4b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18b4b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b4b-122">-DefaultProfile</span></span>
<span data-ttu-id="18b4b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18b4b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18b4b-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="18b4b-124">-RouteTable</span></span>
<span data-ttu-id="18b4b-125">Указывает объект таблицы маршрутов, представляющий состояние, в котором должна быть задана таблица маршрутов.</span><span class="sxs-lookup"><span data-stu-id="18b4b-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

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

### <span data-ttu-id="18b4b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18b4b-126">-Confirm</span></span>
<span data-ttu-id="18b4b-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="18b4b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b4b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b4b-128">-WhatIf</span></span>
<span data-ttu-id="18b4b-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="18b4b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18b4b-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="18b4b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b4b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b4b-131">CommonParameters</span></span>
<span data-ttu-id="18b4b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18b4b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b4b-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b4b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b4b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18b4b-134">INPUTS</span></span>

### <span data-ttu-id="18b4b-135">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="18b4b-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="18b4b-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18b4b-136">OUTPUTS</span></span>

### <span data-ttu-id="18b4b-137">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="18b4b-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="18b4b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="18b4b-138">NOTES</span></span>

## <span data-ttu-id="18b4b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18b4b-139">RELATED LINKS</span></span>

[<span data-ttu-id="18b4b-140">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="18b4b-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="18b4b-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="18b4b-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="18b4b-142">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="18b4b-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="18b4b-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="18b4b-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

