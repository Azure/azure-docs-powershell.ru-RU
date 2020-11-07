---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 195ff0f8da8af5408f9b7ad2bffdd35507b10d1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902338"
---
# <span data-ttu-id="9a9a1-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9a9a1-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="9a9a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9a1-103">Возвращает маршруты из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="9a9a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a9a1-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a9a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="9a9a1-106">Командлет **Get-AzRouteConfig** получает маршруты из таблицы маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="9a9a1-107">Вы можете указать маршрут по имени.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-107">You can specify a route by name.</span></span>

## <span data-ttu-id="9a9a1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a9a1-108">EXAMPLES</span></span>

### <span data-ttu-id="9a9a1-109">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="9a9a1-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="9a9a1-110">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="9a9a1-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="9a9a1-111">Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9a9a1-112">Текущий командлет получает маршрут с именем Route07 в таблице маршрутов с именем RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="9a9a1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a9a1-113">PARAMETERS</span></span>

### <span data-ttu-id="9a9a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a9a1-114">-DefaultProfile</span></span>
<span data-ttu-id="9a9a1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a9a1-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a9a1-116">-Name</span></span>
<span data-ttu-id="9a9a1-117">Указывает имя маршрута, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9a9a1-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="9a9a1-118">-RouteTable</span></span>
<span data-ttu-id="9a9a1-119">Указывает таблицу маршрутов, из которой этот командлет получает маршруты.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="9a9a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9a1-120">CommonParameters</span></span>
<span data-ttu-id="9a9a1-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a9a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9a1-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a9a1-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9a1-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a9a1-123">INPUTS</span></span>

### <span data-ttu-id="9a9a1-124">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9a9a1-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="9a9a1-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a9a1-125">OUTPUTS</span></span>

### <span data-ttu-id="9a9a1-126">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="9a9a1-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="9a9a1-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a9a1-127">NOTES</span></span>

## <span data-ttu-id="9a9a1-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a9a1-128">RELATED LINKS</span></span>

[<span data-ttu-id="9a9a1-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9a9a1-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="9a9a1-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="9a9a1-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="9a9a1-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9a9a1-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="9a9a1-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9a9a1-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="9a9a1-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9a9a1-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


