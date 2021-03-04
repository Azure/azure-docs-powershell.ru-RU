---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: ef5609a34104ca8502b8e4ce96fe294a4714366d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954067"
---
# <span data-ttu-id="23a81-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="23a81-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="23a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23a81-102">SYNOPSIS</span></span>
<span data-ttu-id="23a81-103">Получить Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="23a81-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="23a81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23a81-104">SYNTAX</span></span>

### <span data-ttu-id="23a81-105">RouteServerSubscriptionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23a81-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23a81-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23a81-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23a81-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23a81-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23a81-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23a81-108">DESCRIPTION</span></span>
<span data-ttu-id="23a81-109">**Cmdlet Get-AzRouteServer** получает Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="23a81-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="23a81-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23a81-110">EXAMPLES</span></span>

### <span data-ttu-id="23a81-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23a81-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="23a81-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="23a81-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="23a81-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23a81-113">PARAMETERS</span></span>

### <span data-ttu-id="23a81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a81-114">-DefaultProfile</span></span>
<span data-ttu-id="23a81-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23a81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23a81-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23a81-116">-ResourceGroupName</span></span>
<span data-ttu-id="23a81-117">Имя группы ресурсов сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="23a81-117">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a81-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23a81-118">-ResourceId</span></span>
<span data-ttu-id="23a81-119">ResourceId сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="23a81-119">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a81-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="23a81-120">-RouteServerName</span></span>
<span data-ttu-id="23a81-121">Имя сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="23a81-121">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a81-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a81-122">CommonParameters</span></span>
<span data-ttu-id="23a81-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a81-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a81-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23a81-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a81-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23a81-125">INPUTS</span></span>

### <span data-ttu-id="23a81-126">System.String</span><span class="sxs-lookup"><span data-stu-id="23a81-126">System.String</span></span>

## <span data-ttu-id="23a81-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23a81-127">OUTPUTS</span></span>

### <span data-ttu-id="23a81-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="23a81-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="23a81-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23a81-129">NOTES</span></span>

## <span data-ttu-id="23a81-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23a81-130">RELATED LINKS</span></span>
