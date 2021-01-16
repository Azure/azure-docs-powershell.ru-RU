---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409020"
---
# <span data-ttu-id="edd41-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="edd41-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="edd41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edd41-102">SYNOPSIS</span></span>
<span data-ttu-id="edd41-103">Удаление маршрутов в центре IoT</span><span class="sxs-lookup"><span data-stu-id="edd41-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="edd41-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="edd41-104">SYNTAX</span></span>

### <span data-ttu-id="edd41-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="edd41-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edd41-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="edd41-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edd41-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="edd41-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edd41-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edd41-108">DESCRIPTION</span></span>
<span data-ttu-id="edd41-109">Удаление маршрутов в конечную точку</span><span class="sxs-lookup"><span data-stu-id="edd41-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="edd41-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="edd41-110">EXAMPLES</span></span>

### <span data-ttu-id="edd41-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="edd41-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="edd41-112">Удалить маршрут "R1" из IoT-концентратора Myiothub.</span><span class="sxs-lookup"><span data-stu-id="edd41-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="edd41-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edd41-113">PARAMETERS</span></span>

### <span data-ttu-id="edd41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd41-114">-DefaultProfile</span></span>
<span data-ttu-id="edd41-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edd41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edd41-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edd41-116">-InputObject</span></span>
<span data-ttu-id="edd41-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="edd41-117">IotHub Object</span></span>

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

### <span data-ttu-id="edd41-118">-Name</span><span class="sxs-lookup"><span data-stu-id="edd41-118">-Name</span></span>
<span data-ttu-id="edd41-119">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="edd41-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="edd41-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edd41-120">-PassThru</span></span>
<span data-ttu-id="edd41-121">Разрешает возвращать boolean object.</span><span class="sxs-lookup"><span data-stu-id="edd41-121">Allows to return the boolean object.</span></span> <span data-ttu-id="edd41-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="edd41-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="edd41-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd41-123">-ResourceGroupName</span></span>
<span data-ttu-id="edd41-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="edd41-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="edd41-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edd41-125">-ResourceId</span></span>
<span data-ttu-id="edd41-126">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="edd41-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="edd41-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="edd41-127">-RouteName</span></span>
<span data-ttu-id="edd41-128">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="edd41-128">Name of the Route</span></span>

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

### <span data-ttu-id="edd41-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edd41-129">-Confirm</span></span>
<span data-ttu-id="edd41-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="edd41-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd41-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd41-131">-WhatIf</span></span>
<span data-ttu-id="edd41-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd41-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edd41-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="edd41-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd41-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd41-134">CommonParameters</span></span>
<span data-ttu-id="edd41-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd41-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd41-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd41-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd41-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edd41-137">INPUTS</span></span>

### <span data-ttu-id="edd41-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="edd41-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="edd41-139">System.String</span><span class="sxs-lookup"><span data-stu-id="edd41-139">System.String</span></span>

## <span data-ttu-id="edd41-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="edd41-140">OUTPUTS</span></span>

### <span data-ttu-id="edd41-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edd41-141">System.Boolean</span></span>

## <span data-ttu-id="edd41-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="edd41-142">NOTES</span></span>

## <span data-ttu-id="edd41-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edd41-143">RELATED LINKS</span></span>