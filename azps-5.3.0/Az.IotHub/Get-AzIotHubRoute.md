---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518605"
---
# <span data-ttu-id="01940-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="01940-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="01940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01940-102">SYNOPSIS</span></span>
<span data-ttu-id="01940-103">Сведения о маршруте в центре IoT</span><span class="sxs-lookup"><span data-stu-id="01940-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="01940-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01940-104">SYNTAX</span></span>

### <span data-ttu-id="01940-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01940-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01940-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="01940-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01940-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="01940-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01940-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01940-108">DESCRIPTION</span></span>
<span data-ttu-id="01940-109">Получите сведения о маршруте. Вы можете получить все маршруты из концентратора IoT, получить маршруты до определенной конечной точки или до конкретной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="01940-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="01940-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01940-110">EXAMPLES</span></span>

### <span data-ttu-id="01940-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01940-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="01940-112">Получите весь маршрут из концентратора IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="01940-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="01940-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="01940-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="01940-114">Сведения о маршруте можно получить из IoT Hub myiothub.</span><span class="sxs-lookup"><span data-stu-id="01940-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="01940-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01940-115">PARAMETERS</span></span>

### <span data-ttu-id="01940-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01940-116">-DefaultProfile</span></span>
<span data-ttu-id="01940-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01940-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01940-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01940-118">-InputObject</span></span>
<span data-ttu-id="01940-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="01940-119">IotHub Object</span></span>

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

### <span data-ttu-id="01940-120">-Name</span><span class="sxs-lookup"><span data-stu-id="01940-120">-Name</span></span>
<span data-ttu-id="01940-121">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="01940-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="01940-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01940-122">-ResourceGroupName</span></span>
<span data-ttu-id="01940-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="01940-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="01940-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01940-124">-ResourceId</span></span>
<span data-ttu-id="01940-125">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="01940-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="01940-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="01940-126">-RouteName</span></span>
<span data-ttu-id="01940-127">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="01940-127">Name of the Route</span></span>

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

### <span data-ttu-id="01940-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01940-128">CommonParameters</span></span>
<span data-ttu-id="01940-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01940-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01940-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01940-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01940-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01940-131">INPUTS</span></span>

### <span data-ttu-id="01940-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="01940-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="01940-133">System.String</span><span class="sxs-lookup"><span data-stu-id="01940-133">System.String</span></span>

## <span data-ttu-id="01940-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01940-134">OUTPUTS</span></span>

### <span data-ttu-id="01940-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="01940-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="01940-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="01940-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="01940-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01940-137">NOTES</span></span>

## <span data-ttu-id="01940-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01940-138">RELATED LINKS</span></span>
