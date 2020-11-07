---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: fe079282d85b5aea8ebedcf69504fbb0e3dab04b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911118"
---
# <span data-ttu-id="6ae7f-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6ae7f-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="6ae7f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ae7f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae7f-103">Удаляет маршрут из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="6ae7f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ae7f-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ae7f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ae7f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ae7f-106">Командлет **Remove-AzRouteConfig** удаляет маршрут из таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="6ae7f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ae7f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ae7f-108">Пример 1: Удаление маршрута</span><span class="sxs-lookup"><span data-stu-id="6ae7f-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="6ae7f-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="6ae7f-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="6ae7f-110">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ae7f-111">Текущий командлет удаляет маршрут с именем Route02 и передает результат командлету **Set-AzRouteTable** , который обновляет таблицу, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="6ae7f-112">Таблица больше не будет содержать маршрут с именем Route02.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="6ae7f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ae7f-113">PARAMETERS</span></span>

### <span data-ttu-id="6ae7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae7f-114">-DefaultProfile</span></span>
<span data-ttu-id="6ae7f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ae7f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6ae7f-116">-Name</span></span>
<span data-ttu-id="6ae7f-117">Указывает имя маршрута, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-117">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae7f-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="6ae7f-118">-RouteTable</span></span>
<span data-ttu-id="6ae7f-119">Указывает таблицу маршрутов, которая содержит маршрут, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae7f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ae7f-120">-Confirm</span></span>
<span data-ttu-id="6ae7f-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae7f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ae7f-122">-WhatIf</span></span>
<span data-ttu-id="6ae7f-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ae7f-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae7f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae7f-125">CommonParameters</span></span>
<span data-ttu-id="6ae7f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae7f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ae7f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae7f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ae7f-128">INPUTS</span></span>

### <span data-ttu-id="6ae7f-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ae7f-129">PSRouteTable</span></span>
<span data-ttu-id="6ae7f-130">Параметр "RouteTable" принимает значение типа "PSRouteTable" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6ae7f-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="6ae7f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ae7f-131">OUTPUTS</span></span>

### <span data-ttu-id="6ae7f-132">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ae7f-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="6ae7f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ae7f-133">NOTES</span></span>

## <span data-ttu-id="6ae7f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ae7f-134">RELATED LINKS</span></span>

[<span data-ttu-id="6ae7f-135">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6ae7f-135">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="6ae7f-136">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6ae7f-136">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="6ae7f-137">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6ae7f-137">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="6ae7f-138">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6ae7f-138">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


