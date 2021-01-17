---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416119"
---
# <span data-ttu-id="f5bc0-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc0-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="f5bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="f5bc0-103">Маршруты из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f5bc0-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="f5bc0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5bc0-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5bc0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="f5bc0-106">Чтобы получить маршруты из таблицы маршрутов Azure, можно получить маршруты из таблицы маршрутов **Get-AzRouteConfig.**</span><span class="sxs-lookup"><span data-stu-id="f5bc0-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="f5bc0-107">Вы можете указать маршрут по имени.</span><span class="sxs-lookup"><span data-stu-id="f5bc0-107">You can specify a route by name.</span></span>

## <span data-ttu-id="f5bc0-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5bc0-108">EXAMPLES</span></span>

### <span data-ttu-id="f5bc0-109">Пример 1. Получить таблицу маршрутов</span><span class="sxs-lookup"><span data-stu-id="f5bc0-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="f5bc0-110">Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью **командлета Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="f5bc0-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="f5bc0-111">Эта команда передает эту таблицу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f5bc0-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5bc0-112">Текущий cmdlet получит маршрут Route07 в таблице routetable01.</span><span class="sxs-lookup"><span data-stu-id="f5bc0-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="f5bc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5bc0-113">PARAMETERS</span></span>

### <span data-ttu-id="f5bc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5bc0-114">-DefaultProfile</span></span>
<span data-ttu-id="f5bc0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5bc0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5bc0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f5bc0-116">-Name</span></span>
<span data-ttu-id="f5bc0-117">Указывает имя маршрута, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5bc0-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f5bc0-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f5bc0-118">-RouteTable</span></span>
<span data-ttu-id="f5bc0-119">Определяет таблицу маршрутов, из которой этот cmdlet получает маршруты.</span><span class="sxs-lookup"><span data-stu-id="f5bc0-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="f5bc0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5bc0-120">CommonParameters</span></span>
<span data-ttu-id="f5bc0-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5bc0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5bc0-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5bc0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5bc0-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5bc0-123">INPUTS</span></span>

### <span data-ttu-id="f5bc0-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5bc0-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f5bc0-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5bc0-125">OUTPUTS</span></span>

### <span data-ttu-id="f5bc0-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="f5bc0-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="f5bc0-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5bc0-127">NOTES</span></span>

## <span data-ttu-id="f5bc0-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5bc0-128">RELATED LINKS</span></span>

[<span data-ttu-id="f5bc0-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc0-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="f5bc0-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5bc0-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="f5bc0-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc0-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="f5bc0-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc0-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="f5bc0-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc0-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


