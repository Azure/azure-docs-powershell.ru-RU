---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232081"
---
# <span data-ttu-id="848ce-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="848ce-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="848ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="848ce-102">SYNOPSIS</span></span>
<span data-ttu-id="848ce-103">Удаляет шаг.</span><span class="sxs-lookup"><span data-stu-id="848ce-103">Deletes the step.</span></span>

## <span data-ttu-id="848ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="848ce-104">SYNTAX</span></span>

### <span data-ttu-id="848ce-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="848ce-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848ce-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="848ce-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848ce-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="848ce-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="848ce-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="848ce-108">DESCRIPTION</span></span>
<span data-ttu-id="848ce-109">Выполнение шага удаляется с учетом выполнения **cmdlet Remove-AzDeploymentManagerStep.**</span><span class="sxs-lookup"><span data-stu-id="848ce-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="848ce-110">Укажите шаг по имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="848ce-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="848ce-111">Кроме того, вы можете уступить объект Step или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="848ce-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="848ce-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="848ce-112">EXAMPLES</span></span>

### <span data-ttu-id="848ce-113">Пример 1. Удаление шага</span><span class="sxs-lookup"><span data-stu-id="848ce-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="848ce-114">Эта команда удаляет шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="848ce-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="848ce-115">Пример 2. Удаление шага с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="848ce-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="848ce-116">Эта команда удаляет шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="848ce-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="848ce-117">Пример 3. Удаление шага с помощью объекта, New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="848ce-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="848ce-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="848ce-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="848ce-119">Эта команда удаляет шаг, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="848ce-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="848ce-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="848ce-120">PARAMETERS</span></span>

### <span data-ttu-id="848ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848ce-121">-DefaultProfile</span></span>
<span data-ttu-id="848ce-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="848ce-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="848ce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="848ce-123">-InputObject</span></span>
<span data-ttu-id="848ce-124">Удаляемая пошаговая пошаго</span><span class="sxs-lookup"><span data-stu-id="848ce-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="848ce-125">-Name</span><span class="sxs-lookup"><span data-stu-id="848ce-125">-Name</span></span>
<span data-ttu-id="848ce-126">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="848ce-126">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="848ce-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="848ce-127">-PassThru</span></span>
<span data-ttu-id="848ce-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="848ce-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="848ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="848ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="848ce-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="848ce-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="848ce-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="848ce-131">-ResourceId</span></span>
<span data-ttu-id="848ce-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="848ce-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848ce-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="848ce-133">-Confirm</span></span>
<span data-ttu-id="848ce-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="848ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="848ce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="848ce-135">-WhatIf</span></span>
<span data-ttu-id="848ce-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="848ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="848ce-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="848ce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="848ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848ce-138">CommonParameters</span></span>
<span data-ttu-id="848ce-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="848ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848ce-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="848ce-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848ce-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="848ce-141">INPUTS</span></span>

### <span data-ttu-id="848ce-142">System.String</span><span class="sxs-lookup"><span data-stu-id="848ce-142">System.String</span></span>

### <span data-ttu-id="848ce-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="848ce-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="848ce-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="848ce-144">OUTPUTS</span></span>

### <span data-ttu-id="848ce-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="848ce-145">System.Boolean</span></span>

## <span data-ttu-id="848ce-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="848ce-146">NOTES</span></span>

## <span data-ttu-id="848ce-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="848ce-147">RELATED LINKS</span></span>
