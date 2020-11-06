---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: b64fe52b95fb116b08aade300f622b8ea612dcc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568723"
---
# <span data-ttu-id="8845d-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8845d-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="8845d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8845d-102">SYNOPSIS</span></span>
<span data-ttu-id="8845d-103">Удаляет маршрут из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8845d-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8845d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8845d-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8845d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8845d-105">DESCRIPTION</span></span>
<span data-ttu-id="8845d-106">Командлет **Remove-AzureRmRouteConfig** удаляет маршрут из таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="8845d-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="8845d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8845d-107">EXAMPLES</span></span>

### <span data-ttu-id="8845d-108">Пример 1: Удаление маршрута</span><span class="sxs-lookup"><span data-stu-id="8845d-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="8845d-109">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="8845d-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="8845d-110">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="8845d-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8845d-111">Текущий командлет удаляет маршрут с именем Route02 и передает результат командлету **Set-AzureRmRouteTable** , который обновляет таблицу, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="8845d-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="8845d-112">Таблица больше не будет содержать маршрут с именем Route02.</span><span class="sxs-lookup"><span data-stu-id="8845d-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="8845d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8845d-113">PARAMETERS</span></span>

### <span data-ttu-id="8845d-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8845d-114">-Name</span></span>
<span data-ttu-id="8845d-115">Указывает имя маршрута, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8845d-115">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8845d-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="8845d-116">-RouteTable</span></span>
<span data-ttu-id="8845d-117">Указывает таблицу маршрутов, которая содержит маршрут, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8845d-117">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="8845d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8845d-118">-DefaultProfile</span></span>
<span data-ttu-id="8845d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8845d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8845d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8845d-120">CommonParameters</span></span>
<span data-ttu-id="8845d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8845d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8845d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8845d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8845d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8845d-123">INPUTS</span></span>

### <span data-ttu-id="8845d-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="8845d-124">PSRouteTable</span></span>
<span data-ttu-id="8845d-125">Параметр "RouteTable" принимает значение типа "PSRouteTable" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8845d-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="8845d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8845d-126">OUTPUTS</span></span>

### <span data-ttu-id="8845d-127">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="8845d-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="8845d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8845d-128">NOTES</span></span>

## <span data-ttu-id="8845d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8845d-129">RELATED LINKS</span></span>

[<span data-ttu-id="8845d-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8845d-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="8845d-131">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8845d-131">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="8845d-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8845d-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="8845d-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8845d-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


