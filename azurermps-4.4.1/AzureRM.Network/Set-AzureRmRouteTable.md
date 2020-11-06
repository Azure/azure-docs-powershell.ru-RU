---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: e525580d7384eef6b7fa7518fc6ddc5707a010ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565225"
---
# <span data-ttu-id="85719-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="85719-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="85719-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85719-102">SYNOPSIS</span></span>
<span data-ttu-id="85719-103">Задает состояние цели для таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="85719-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85719-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85719-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85719-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85719-105">DESCRIPTION</span></span>
<span data-ttu-id="85719-106">Командлет **Set-AzureRmRouteTable** задает состояние цели для таблицы маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="85719-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="85719-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85719-107">EXAMPLES</span></span>

### <span data-ttu-id="85719-108">Пример 1: добавить маршрут, а затем задать состояние цели для таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="85719-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
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

<span data-ttu-id="85719-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="85719-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="85719-110">Команда передает эту таблицу командлету Add-AzureRmRouteConfig с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="85719-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="85719-111">**Add-AzureRmRouteConfig** добавляет маршрут с именем Route07, а затем передает результат в текущий командлет, который обновляет таблицу, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="85719-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="85719-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85719-112">PARAMETERS</span></span>

### <span data-ttu-id="85719-113">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="85719-113">-RouteTable</span></span>
<span data-ttu-id="85719-114">Указывает объект таблицы маршрутов, представляющий состояние цели, на которое этот командлет задает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="85719-114">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

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

### <span data-ttu-id="85719-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85719-115">-DefaultProfile</span></span>
<span data-ttu-id="85719-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85719-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85719-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85719-117">CommonParameters</span></span>
<span data-ttu-id="85719-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85719-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85719-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85719-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85719-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85719-120">INPUTS</span></span>

### <span data-ttu-id="85719-121">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="85719-121">PSRouteTable</span></span>
<span data-ttu-id="85719-122">Параметр "RouteTable" принимает значение типа "PSRouteTable" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="85719-122">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="85719-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85719-123">OUTPUTS</span></span>

### <span data-ttu-id="85719-124">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="85719-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="85719-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="85719-125">NOTES</span></span>

## <span data-ttu-id="85719-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85719-126">RELATED LINKS</span></span>

[<span data-ttu-id="85719-127">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="85719-127">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="85719-128">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="85719-128">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="85719-129">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="85719-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="85719-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="85719-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


