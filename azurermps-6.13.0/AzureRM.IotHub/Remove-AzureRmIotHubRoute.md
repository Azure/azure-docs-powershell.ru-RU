---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
ms.openlocfilehash: 9af711bd449bc8c69808f30dc99ceea806dee00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568532"
---
# <span data-ttu-id="27348-101">Remove-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="27348-101">Remove-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="27348-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27348-102">SYNOPSIS</span></span>
<span data-ttu-id="27348-103">Удаление маршрута в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="27348-103">Delete a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27348-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27348-104">SYNTAX</span></span>

### <span data-ttu-id="27348-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27348-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27348-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27348-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27348-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27348-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27348-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27348-108">DESCRIPTION</span></span>
<span data-ttu-id="27348-109">Удаление маршрутов к конечной точке</span><span class="sxs-lookup"><span data-stu-id="27348-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="27348-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27348-110">EXAMPLES</span></span>

### <span data-ttu-id="27348-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27348-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="27348-112">Удалить маршрут "R1" из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="27348-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="27348-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27348-113">PARAMETERS</span></span>

### <span data-ttu-id="27348-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27348-114">-DefaultProfile</span></span>
<span data-ttu-id="27348-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27348-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27348-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27348-116">-InputObject</span></span>
<span data-ttu-id="27348-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="27348-117">IotHub Object</span></span>

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

### <span data-ttu-id="27348-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27348-118">-Name</span></span>
<span data-ttu-id="27348-119">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="27348-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="27348-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27348-120">-PassThru</span></span>
<span data-ttu-id="27348-121">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="27348-121">Allows to return the boolean object.</span></span> <span data-ttu-id="27348-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="27348-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27348-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27348-123">-ResourceGroupName</span></span>
<span data-ttu-id="27348-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="27348-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27348-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27348-125">-ResourceId</span></span>
<span data-ttu-id="27348-126">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="27348-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="27348-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="27348-127">-RouteName</span></span>
<span data-ttu-id="27348-128">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="27348-128">Name of the Route</span></span>

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

### <span data-ttu-id="27348-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27348-129">-Confirm</span></span>
<span data-ttu-id="27348-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27348-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27348-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27348-131">-WhatIf</span></span>
<span data-ttu-id="27348-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27348-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27348-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27348-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27348-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27348-134">CommonParameters</span></span>
<span data-ttu-id="27348-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27348-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27348-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27348-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27348-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27348-137">INPUTS</span></span>

### <span data-ttu-id="27348-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="27348-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="27348-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27348-139">System.String</span></span>

## <span data-ttu-id="27348-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27348-140">OUTPUTS</span></span>

### <span data-ttu-id="27348-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27348-141">System.Boolean</span></span>

## <span data-ttu-id="27348-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="27348-142">NOTES</span></span>

## <span data-ttu-id="27348-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27348-143">RELATED LINKS</span></span>
