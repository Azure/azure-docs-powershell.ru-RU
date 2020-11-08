---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079612"
---
# <span data-ttu-id="b4258-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="b4258-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="b4258-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4258-102">SYNOPSIS</span></span>
<span data-ttu-id="b4258-103">Удаление маршрута в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="b4258-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="b4258-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4258-104">SYNTAX</span></span>

### <span data-ttu-id="b4258-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4258-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4258-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4258-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4258-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b4258-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4258-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4258-108">DESCRIPTION</span></span>
<span data-ttu-id="b4258-109">Удаление маршрутов к конечной точке</span><span class="sxs-lookup"><span data-stu-id="b4258-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="b4258-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4258-110">EXAMPLES</span></span>

### <span data-ttu-id="b4258-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4258-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="b4258-112">Удалить маршрут "R1" из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="b4258-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="b4258-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4258-113">PARAMETERS</span></span>

### <span data-ttu-id="b4258-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4258-114">-DefaultProfile</span></span>
<span data-ttu-id="b4258-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4258-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4258-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4258-116">-InputObject</span></span>
<span data-ttu-id="b4258-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="b4258-117">IotHub Object</span></span>

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

### <span data-ttu-id="b4258-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4258-118">-Name</span></span>
<span data-ttu-id="b4258-119">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="b4258-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b4258-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4258-120">-PassThru</span></span>
<span data-ttu-id="b4258-121">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="b4258-121">Allows to return the boolean object.</span></span> <span data-ttu-id="b4258-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b4258-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4258-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4258-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4258-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b4258-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b4258-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4258-125">-ResourceId</span></span>
<span data-ttu-id="b4258-126">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="b4258-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b4258-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="b4258-127">-RouteName</span></span>
<span data-ttu-id="b4258-128">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="b4258-128">Name of the Route</span></span>

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

### <span data-ttu-id="b4258-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4258-129">-Confirm</span></span>
<span data-ttu-id="b4258-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4258-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4258-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4258-131">-WhatIf</span></span>
<span data-ttu-id="b4258-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4258-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4258-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4258-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4258-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4258-134">CommonParameters</span></span>
<span data-ttu-id="b4258-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4258-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4258-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4258-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4258-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4258-137">INPUTS</span></span>

### <span data-ttu-id="b4258-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b4258-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b4258-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4258-139">System.String</span></span>

## <span data-ttu-id="b4258-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4258-140">OUTPUTS</span></span>

### <span data-ttu-id="b4258-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4258-141">System.Boolean</span></span>

## <span data-ttu-id="b4258-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4258-142">NOTES</span></span>

## <span data-ttu-id="b4258-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4258-143">RELATED LINKS</span></span>