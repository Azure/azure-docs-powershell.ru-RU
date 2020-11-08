---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073822"
---
# <span data-ttu-id="87755-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="87755-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="87755-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87755-102">SYNOPSIS</span></span>
<span data-ttu-id="87755-103">Получение сведений о маршруте в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="87755-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="87755-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87755-104">SYNTAX</span></span>

### <span data-ttu-id="87755-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87755-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87755-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87755-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87755-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="87755-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87755-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87755-108">DESCRIPTION</span></span>
<span data-ttu-id="87755-109">Получение сведений о маршруте. Вы можете получить все маршруты от центра Интернета вещей, получить маршруты к типу конечной точки или получить маршруты к определенной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="87755-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="87755-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87755-110">EXAMPLES</span></span>

### <span data-ttu-id="87755-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87755-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="87755-112">Получить весь маршрут от центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="87755-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="87755-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="87755-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="87755-114">Получение сведений о маршруте из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="87755-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="87755-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87755-115">PARAMETERS</span></span>

### <span data-ttu-id="87755-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87755-116">-DefaultProfile</span></span>
<span data-ttu-id="87755-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87755-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87755-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87755-118">-InputObject</span></span>
<span data-ttu-id="87755-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="87755-119">IotHub Object</span></span>

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

### <span data-ttu-id="87755-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87755-120">-Name</span></span>
<span data-ttu-id="87755-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="87755-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="87755-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87755-122">-ResourceGroupName</span></span>
<span data-ttu-id="87755-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="87755-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="87755-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87755-124">-ResourceId</span></span>
<span data-ttu-id="87755-125">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="87755-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="87755-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="87755-126">-RouteName</span></span>
<span data-ttu-id="87755-127">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="87755-127">Name of the Route</span></span>

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

### <span data-ttu-id="87755-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87755-128">CommonParameters</span></span>
<span data-ttu-id="87755-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87755-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87755-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87755-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87755-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87755-131">INPUTS</span></span>

### <span data-ttu-id="87755-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="87755-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="87755-133">System. String</span><span class="sxs-lookup"><span data-stu-id="87755-133">System.String</span></span>

## <span data-ttu-id="87755-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87755-134">OUTPUTS</span></span>

### <span data-ttu-id="87755-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="87755-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="87755-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="87755-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="87755-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="87755-137">NOTES</span></span>

## <span data-ttu-id="87755-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87755-138">RELATED LINKS</span></span>
