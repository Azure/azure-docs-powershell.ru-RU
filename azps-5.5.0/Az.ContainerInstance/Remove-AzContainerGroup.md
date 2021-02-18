---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215556"
---
# <span data-ttu-id="6459a-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="6459a-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="6459a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6459a-102">SYNOPSIS</span></span>
<span data-ttu-id="6459a-103">Удаляет группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="6459a-103">Removes a container group.</span></span>

## <span data-ttu-id="6459a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6459a-104">SYNTAX</span></span>

### <span data-ttu-id="6459a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6459a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6459a-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="6459a-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6459a-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="6459a-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6459a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6459a-108">DESCRIPTION</span></span>
<span data-ttu-id="6459a-109">При **этом удаляется** группа контейнеров.</span><span class="sxs-lookup"><span data-stu-id="6459a-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="6459a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6459a-110">EXAMPLES</span></span>

### <span data-ttu-id="6459a-111">Пример 1. Удаление группы контейнеров</span><span class="sxs-lookup"><span data-stu-id="6459a-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="6459a-112">Эта команда удаляет указанную группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="6459a-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="6459a-113">Пример 2. Удаляет группу контейнеров с помощью piping</span><span class="sxs-lookup"><span data-stu-id="6459a-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="6459a-114">Эта команда удаляет группу контейнеров путем прокайки.</span><span class="sxs-lookup"><span data-stu-id="6459a-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="6459a-115">Пример 3. Удаляет группу контейнеров по ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6459a-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="6459a-116">Эта команда удаляет группу контейнеров по ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6459a-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="6459a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6459a-117">PARAMETERS</span></span>

### <span data-ttu-id="6459a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6459a-118">-DefaultProfile</span></span>
<span data-ttu-id="6459a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6459a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6459a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6459a-120">-InputObject</span></span>
<span data-ttu-id="6459a-121">Группа контейнеров, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6459a-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6459a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6459a-122">-Name</span></span>
<span data-ttu-id="6459a-123">Имя группы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="6459a-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6459a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6459a-124">-PassThru</span></span>
<span data-ttu-id="6459a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6459a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6459a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6459a-126">-ResourceGroupName</span></span>
<span data-ttu-id="6459a-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6459a-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6459a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6459a-128">-ResourceId</span></span>
<span data-ttu-id="6459a-129">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="6459a-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6459a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6459a-130">-Confirm</span></span>
<span data-ttu-id="6459a-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6459a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6459a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6459a-132">-WhatIf</span></span>
<span data-ttu-id="6459a-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6459a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6459a-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6459a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6459a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6459a-135">CommonParameters</span></span>
<span data-ttu-id="6459a-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6459a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6459a-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6459a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6459a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6459a-138">INPUTS</span></span>

### <span data-ttu-id="6459a-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="6459a-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="6459a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6459a-140">System.String</span></span>

## <span data-ttu-id="6459a-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6459a-141">OUTPUTS</span></span>

### <span data-ttu-id="6459a-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="6459a-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="6459a-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6459a-143">NOTES</span></span>

## <span data-ttu-id="6459a-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6459a-144">RELATED LINKS</span></span>
