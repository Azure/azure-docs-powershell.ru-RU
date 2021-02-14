---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237657"
---
# <span data-ttu-id="67ca6-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="67ca6-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="67ca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="67ca6-103">Сведения о маршруте в центре IoT</span><span class="sxs-lookup"><span data-stu-id="67ca6-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="67ca6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67ca6-104">SYNTAX</span></span>

### <span data-ttu-id="67ca6-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67ca6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ca6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67ca6-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67ca6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="67ca6-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67ca6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="67ca6-109">Получите сведения о маршруте. Вы можете получить все маршруты из концентратора IoT, получить маршруты до определенной конечной точки или до конкретной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="67ca6-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="67ca6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67ca6-110">EXAMPLES</span></span>

### <span data-ttu-id="67ca6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67ca6-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="67ca6-112">Получите весь маршрут из концентратора IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="67ca6-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="67ca6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="67ca6-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="67ca6-114">Сведения о маршруте можно получить из IoT Hub myiothub.</span><span class="sxs-lookup"><span data-stu-id="67ca6-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="67ca6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67ca6-115">PARAMETERS</span></span>

### <span data-ttu-id="67ca6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ca6-116">-DefaultProfile</span></span>
<span data-ttu-id="67ca6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67ca6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ca6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67ca6-118">-InputObject</span></span>
<span data-ttu-id="67ca6-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="67ca6-119">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67ca6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="67ca6-120">-Name</span></span>
<span data-ttu-id="67ca6-121">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="67ca6-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ca6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ca6-122">-ResourceGroupName</span></span>
<span data-ttu-id="67ca6-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="67ca6-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ca6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67ca6-124">-ResourceId</span></span>
<span data-ttu-id="67ca6-125">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="67ca6-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ca6-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="67ca6-126">-RouteName</span></span>
<span data-ttu-id="67ca6-127">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="67ca6-127">Name of the Route</span></span>

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

### <span data-ttu-id="67ca6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ca6-128">CommonParameters</span></span>
<span data-ttu-id="67ca6-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ca6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ca6-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ca6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ca6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67ca6-131">INPUTS</span></span>

### <span data-ttu-id="67ca6-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="67ca6-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="67ca6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="67ca6-133">System.String</span></span>

## <span data-ttu-id="67ca6-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67ca6-134">OUTPUTS</span></span>

### <span data-ttu-id="67ca6-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="67ca6-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="67ca6-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="67ca6-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="67ca6-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67ca6-137">NOTES</span></span>

## <span data-ttu-id="67ca6-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67ca6-138">RELATED LINKS</span></span>
