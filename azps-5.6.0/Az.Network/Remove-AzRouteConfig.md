---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: e48da3a5f300d39051a9d1b07e9789855ed7dca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996120"
---
# <span data-ttu-id="5a1f0-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a1f0-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="5a1f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="5a1f0-103">Удаляет маршрут из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="5a1f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a1f0-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a1f0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a1f0-105">DESCRIPTION</span></span>
<span data-ttu-id="5a1f0-106">Для удаления маршрутов из таблицы маршрутов Azure удаляется **cmdlet Remove-AzRouteConfig.**</span><span class="sxs-lookup"><span data-stu-id="5a1f0-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="5a1f0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a1f0-107">EXAMPLES</span></span>

### <span data-ttu-id="5a1f0-108">Пример 1. Удаление маршрута</span><span class="sxs-lookup"><span data-stu-id="5a1f0-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="5a1f0-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью **командлета Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="5a1f0-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="5a1f0-110">Эта команда передает эту таблицу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5a1f0-111">Текущий cmdlet удаляет маршрут Route02, а его результат передается в **cmdlet Set-AzRouteTable,** который обновляет таблицу с учетом изменений.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="5a1f0-112">Таблица больше не содержит маршрут с именем Route02.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="5a1f0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a1f0-113">PARAMETERS</span></span>

### <span data-ttu-id="5a1f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a1f0-114">-DefaultProfile</span></span>
<span data-ttu-id="5a1f0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a1f0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a1f0-116">-Name</span></span>
<span data-ttu-id="5a1f0-117">Указывает имя маршрута, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a1f0-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5a1f0-118">-RouteTable</span></span>
<span data-ttu-id="5a1f0-119">Определяет таблицу маршрутов, которая содержит маршрут, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="5a1f0-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a1f0-120">-Confirm</span></span>
<span data-ttu-id="5a1f0-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a1f0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a1f0-122">-WhatIf</span></span>
<span data-ttu-id="5a1f0-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a1f0-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a1f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a1f0-125">CommonParameters</span></span>
<span data-ttu-id="5a1f0-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a1f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a1f0-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a1f0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a1f0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a1f0-128">INPUTS</span></span>

### <span data-ttu-id="5a1f0-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a1f0-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="5a1f0-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a1f0-130">OUTPUTS</span></span>

### <span data-ttu-id="5a1f0-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a1f0-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="5a1f0-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a1f0-132">NOTES</span></span>

## <span data-ttu-id="5a1f0-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a1f0-133">RELATED LINKS</span></span>

[<span data-ttu-id="5a1f0-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a1f0-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="5a1f0-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a1f0-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="5a1f0-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a1f0-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="5a1f0-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a1f0-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


