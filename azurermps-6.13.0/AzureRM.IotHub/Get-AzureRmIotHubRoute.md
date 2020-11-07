---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
ms.openlocfilehash: 0711bd1d6290191c2d5311a7375e6f81c4ecd573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734387"
---
# <span data-ttu-id="c690a-101">Get-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="c690a-101">Get-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="c690a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c690a-102">SYNOPSIS</span></span>
<span data-ttu-id="c690a-103">Получение сведений о маршруте в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="c690a-103">Get information about the route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c690a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c690a-104">SYNTAX</span></span>

### <span data-ttu-id="c690a-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c690a-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c690a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c690a-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c690a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c690a-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c690a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c690a-108">DESCRIPTION</span></span>
<span data-ttu-id="c690a-109">Получение сведений о маршруте. Вы можете получить все маршруты от центра Интернета вещей, получить маршруты к типу конечной точки или получить маршруты к определенной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c690a-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="c690a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c690a-110">EXAMPLES</span></span>

### <span data-ttu-id="c690a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c690a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="c690a-112">Получить весь маршрут от центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="c690a-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="c690a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c690a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="c690a-114">Получение сведений о маршруте из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="c690a-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="c690a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c690a-115">PARAMETERS</span></span>

### <span data-ttu-id="c690a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c690a-116">-DefaultProfile</span></span>
<span data-ttu-id="c690a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c690a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c690a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c690a-118">-InputObject</span></span>
<span data-ttu-id="c690a-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="c690a-119">IotHub Object</span></span>

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

### <span data-ttu-id="c690a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c690a-120">-Name</span></span>
<span data-ttu-id="c690a-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="c690a-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c690a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c690a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c690a-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c690a-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c690a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c690a-124">-ResourceId</span></span>
<span data-ttu-id="c690a-125">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="c690a-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c690a-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c690a-126">-RouteName</span></span>
<span data-ttu-id="c690a-127">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="c690a-127">Name of the Route</span></span>

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

### <span data-ttu-id="c690a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c690a-128">CommonParameters</span></span>
<span data-ttu-id="c690a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c690a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c690a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c690a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c690a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c690a-131">INPUTS</span></span>

### <span data-ttu-id="c690a-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c690a-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="c690a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c690a-133">System.String</span></span>

## <span data-ttu-id="c690a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c690a-134">OUTPUTS</span></span>

### <span data-ttu-id="c690a-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="c690a-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>
<span data-ttu-id="c690a-136">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. IotHub., Version = 3.1.3.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="c690a-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c690a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c690a-137">NOTES</span></span>

## <span data-ttu-id="c690a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c690a-138">RELATED LINKS</span></span>
