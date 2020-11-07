---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: 704ac762bdc7569fd5ad2c0c4912ebf9634e25ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734330"
---
# <span data-ttu-id="b2494-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b2494-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="b2494-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2494-102">SYNOPSIS</span></span>
<span data-ttu-id="b2494-103">Удаляет маршрут из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b2494-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2494-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2494-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2494-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2494-105">DESCRIPTION</span></span>
<span data-ttu-id="b2494-106">Командлет **Remove-AzureRmRouteConfig** удаляет маршрут из таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="b2494-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="b2494-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2494-107">EXAMPLES</span></span>

### <span data-ttu-id="b2494-108">Пример 1: Удаление маршрута</span><span class="sxs-lookup"><span data-stu-id="b2494-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
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

<span data-ttu-id="b2494-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="b2494-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="b2494-110">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="b2494-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b2494-111">Текущий командлет удаляет маршрут с именем Route02 и передает результат командлету **Set-AzureRmRouteTable** , который обновляет таблицу, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="b2494-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="b2494-112">Таблица больше не будет содержать маршрут с именем Route02.</span><span class="sxs-lookup"><span data-stu-id="b2494-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="b2494-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2494-113">PARAMETERS</span></span>

### <span data-ttu-id="b2494-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2494-114">-DefaultProfile</span></span>
<span data-ttu-id="b2494-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2494-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2494-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2494-116">-Name</span></span>
<span data-ttu-id="b2494-117">Указывает имя маршрута, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b2494-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b2494-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b2494-118">-RouteTable</span></span>
<span data-ttu-id="b2494-119">Указывает таблицу маршрутов, которая содержит маршрут, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b2494-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b2494-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2494-120">-Confirm</span></span>
<span data-ttu-id="b2494-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2494-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2494-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2494-122">-WhatIf</span></span>
<span data-ttu-id="b2494-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2494-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2494-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2494-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2494-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2494-125">CommonParameters</span></span>
<span data-ttu-id="b2494-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2494-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2494-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2494-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2494-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2494-128">INPUTS</span></span>

### <span data-ttu-id="b2494-129">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b2494-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="b2494-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2494-130">OUTPUTS</span></span>

### <span data-ttu-id="b2494-131">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b2494-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="b2494-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2494-132">NOTES</span></span>

## <span data-ttu-id="b2494-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2494-133">RELATED LINKS</span></span>

[<span data-ttu-id="b2494-134">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b2494-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="b2494-135">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b2494-135">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="b2494-136">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b2494-136">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="b2494-137">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b2494-137">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


