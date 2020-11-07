---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 61cbe1ef1fc18ba9c2d6455c6cf56b4f951fdfd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900290"
---
# <span data-ttu-id="dc473-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="dc473-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="dc473-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc473-102">SYNOPSIS</span></span>
<span data-ttu-id="dc473-103">Удаление маршрута в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="dc473-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="dc473-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc473-104">SYNTAX</span></span>

### <span data-ttu-id="dc473-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc473-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc473-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc473-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc473-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dc473-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc473-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc473-108">DESCRIPTION</span></span>
<span data-ttu-id="dc473-109">Удаление маршрутов к конечной точке</span><span class="sxs-lookup"><span data-stu-id="dc473-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="dc473-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc473-110">EXAMPLES</span></span>

### <span data-ttu-id="dc473-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc473-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="dc473-112">Удалить маршрут "R1" из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="dc473-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="dc473-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc473-113">PARAMETERS</span></span>

### <span data-ttu-id="dc473-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc473-114">-DefaultProfile</span></span>
<span data-ttu-id="dc473-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc473-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc473-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc473-116">-InputObject</span></span>
<span data-ttu-id="dc473-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="dc473-117">IotHub Object</span></span>

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

### <span data-ttu-id="dc473-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc473-118">-Name</span></span>
<span data-ttu-id="dc473-119">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="dc473-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dc473-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc473-120">-PassThru</span></span>
<span data-ttu-id="dc473-121">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="dc473-121">Allows to return the boolean object.</span></span> <span data-ttu-id="dc473-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dc473-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc473-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc473-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc473-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dc473-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dc473-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc473-125">-ResourceId</span></span>
<span data-ttu-id="dc473-126">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="dc473-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dc473-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="dc473-127">-RouteName</span></span>
<span data-ttu-id="dc473-128">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="dc473-128">Name of the Route</span></span>

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

### <span data-ttu-id="dc473-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc473-129">-Confirm</span></span>
<span data-ttu-id="dc473-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc473-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc473-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc473-131">-WhatIf</span></span>
<span data-ttu-id="dc473-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc473-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc473-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc473-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc473-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc473-134">CommonParameters</span></span>
<span data-ttu-id="dc473-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc473-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc473-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc473-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc473-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc473-137">INPUTS</span></span>

### <span data-ttu-id="dc473-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dc473-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dc473-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc473-139">System.String</span></span>

## <span data-ttu-id="dc473-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc473-140">OUTPUTS</span></span>

### <span data-ttu-id="dc473-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc473-141">System.Boolean</span></span>

## <span data-ttu-id="dc473-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc473-142">NOTES</span></span>

## <span data-ttu-id="dc473-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc473-143">RELATED LINKS</span></span>
