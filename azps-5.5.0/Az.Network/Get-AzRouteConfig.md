---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236985"
---
# <span data-ttu-id="024cd-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="024cd-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="024cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="024cd-102">SYNOPSIS</span></span>
<span data-ttu-id="024cd-103">Маршруты из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="024cd-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="024cd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="024cd-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="024cd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="024cd-105">DESCRIPTION</span></span>
<span data-ttu-id="024cd-106">Для получения маршрутов из таблицы маршрутов Azure возвращается **cmdlet Get-AzRouteConfig.**</span><span class="sxs-lookup"><span data-stu-id="024cd-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="024cd-107">Вы можете указать маршрут по имени.</span><span class="sxs-lookup"><span data-stu-id="024cd-107">You can specify a route by name.</span></span>

## <span data-ttu-id="024cd-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="024cd-108">EXAMPLES</span></span>

### <span data-ttu-id="024cd-109">Пример 1. Получить таблицу маршрутов</span><span class="sxs-lookup"><span data-stu-id="024cd-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="024cd-110">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью **командлета Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="024cd-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="024cd-111">Эта команда передает эту таблицу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="024cd-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="024cd-112">Текущий cmdlet получит маршрут Route07 в таблице routetable01.</span><span class="sxs-lookup"><span data-stu-id="024cd-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="024cd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="024cd-113">PARAMETERS</span></span>

### <span data-ttu-id="024cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024cd-114">-DefaultProfile</span></span>
<span data-ttu-id="024cd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="024cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="024cd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="024cd-116">-Name</span></span>
<span data-ttu-id="024cd-117">Указывает имя маршрута, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="024cd-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="024cd-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="024cd-118">-RouteTable</span></span>
<span data-ttu-id="024cd-119">Определяет таблицу маршрутов, из которой этот cmdlet получает маршруты.</span><span class="sxs-lookup"><span data-stu-id="024cd-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="024cd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024cd-120">CommonParameters</span></span>
<span data-ttu-id="024cd-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="024cd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024cd-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="024cd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024cd-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="024cd-123">INPUTS</span></span>

### <span data-ttu-id="024cd-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="024cd-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="024cd-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="024cd-125">OUTPUTS</span></span>

### <span data-ttu-id="024cd-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="024cd-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="024cd-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="024cd-127">NOTES</span></span>

## <span data-ttu-id="024cd-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="024cd-128">RELATED LINKS</span></span>

[<span data-ttu-id="024cd-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="024cd-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="024cd-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="024cd-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="024cd-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="024cd-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="024cd-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="024cd-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="024cd-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="024cd-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


