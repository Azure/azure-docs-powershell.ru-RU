---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227788"
---
# <span data-ttu-id="df71e-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="df71e-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="df71e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df71e-102">SYNOPSIS</span></span>
<span data-ttu-id="df71e-103">Возвращает виртуальную таблицу маршрутов концентратора в виртуальном центре или перечисляет все таблицы маршрутов в виртуальном центре.</span><span class="sxs-lookup"><span data-stu-id="df71e-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="df71e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="df71e-104">SYNTAX</span></span>

### <span data-ttu-id="df71e-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df71e-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df71e-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="df71e-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df71e-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="df71e-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df71e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df71e-108">DESCRIPTION</span></span>
<span data-ttu-id="df71e-109">Возвращает виртуальную таблицу маршрутов концентратора в виртуальном центре или перечисляет все таблицы маршрутов в виртуальном центре.</span><span class="sxs-lookup"><span data-stu-id="df71e-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="df71e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="df71e-110">EXAMPLES</span></span>

### <span data-ttu-id="df71e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df71e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="df71e-112">Этот cmdlet извлекает ресурс таблицы маршрутов, используя имя группы ресурсов, имя концентратора и имя таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="df71e-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="df71e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df71e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="df71e-114">Этот cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span><span class="sxs-lookup"><span data-stu-id="df71e-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="df71e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df71e-115">PARAMETERS</span></span>

### <span data-ttu-id="df71e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df71e-116">-DefaultProfile</span></span>
<span data-ttu-id="df71e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df71e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df71e-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="df71e-118">-HubName</span></span>
<span data-ttu-id="df71e-119">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="df71e-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df71e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="df71e-120">-Name</span></span>
<span data-ttu-id="df71e-121">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="df71e-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df71e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="df71e-122">-ParentResourceId</span></span>
<span data-ttu-id="df71e-123">Родительский ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="df71e-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df71e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df71e-124">-ResourceGroupName</span></span>
<span data-ttu-id="df71e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df71e-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df71e-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="df71e-126">-VirtualHub</span></span>
<span data-ttu-id="df71e-127">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="df71e-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df71e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df71e-128">CommonParameters</span></span>
<span data-ttu-id="df71e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df71e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df71e-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df71e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df71e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df71e-131">INPUTS</span></span>

### <span data-ttu-id="df71e-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="df71e-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="df71e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="df71e-133">System.String</span></span>

## <span data-ttu-id="df71e-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df71e-134">OUTPUTS</span></span>

### <span data-ttu-id="df71e-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="df71e-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="df71e-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="df71e-136">NOTES</span></span>

## <span data-ttu-id="df71e-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df71e-137">RELATED LINKS</span></span>
