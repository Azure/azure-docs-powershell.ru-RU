---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 1cc1bb46909260bd23cfa3f72e675251a011072d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900333"
---
# <span data-ttu-id="3f8b0-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="3f8b0-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="3f8b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8b0-103">Получение сведений о маршруте в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="3f8b0-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="3f8b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f8b0-104">SYNTAX</span></span>

### <span data-ttu-id="3f8b0-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f8b0-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f8b0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f8b0-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f8b0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3f8b0-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f8b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f8b0-108">DESCRIPTION</span></span>
<span data-ttu-id="3f8b0-109">Получение сведений о маршруте. Вы можете получить все маршруты от центра Интернета вещей, получить маршруты к типу конечной точки или получить маршруты к определенной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3f8b0-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="3f8b0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f8b0-110">EXAMPLES</span></span>

### <span data-ttu-id="3f8b0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f8b0-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="3f8b0-112">Получить весь маршрут от центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="3f8b0-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="3f8b0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f8b0-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="3f8b0-114">Получение сведений о маршруте из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="3f8b0-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="3f8b0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f8b0-115">PARAMETERS</span></span>

### <span data-ttu-id="3f8b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8b0-116">-DefaultProfile</span></span>
<span data-ttu-id="3f8b0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f8b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f8b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f8b0-118">-InputObject</span></span>
<span data-ttu-id="3f8b0-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="3f8b0-119">IotHub Object</span></span>

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

### <span data-ttu-id="3f8b0-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f8b0-120">-Name</span></span>
<span data-ttu-id="3f8b0-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="3f8b0-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3f8b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f8b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f8b0-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f8b0-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3f8b0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f8b0-124">-ResourceId</span></span>
<span data-ttu-id="3f8b0-125">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="3f8b0-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3f8b0-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="3f8b0-126">-RouteName</span></span>
<span data-ttu-id="3f8b0-127">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="3f8b0-127">Name of the Route</span></span>

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

### <span data-ttu-id="3f8b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8b0-128">CommonParameters</span></span>
<span data-ttu-id="3f8b0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f8b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8b0-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f8b0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8b0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f8b0-131">INPUTS</span></span>

### <span data-ttu-id="3f8b0-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3f8b0-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3f8b0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3f8b0-133">System.String</span></span>

## <span data-ttu-id="3f8b0-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f8b0-134">OUTPUTS</span></span>

### <span data-ttu-id="3f8b0-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="3f8b0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="3f8b0-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="3f8b0-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="3f8b0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f8b0-137">NOTES</span></span>

## <span data-ttu-id="3f8b0-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f8b0-138">RELATED LINKS</span></span>
