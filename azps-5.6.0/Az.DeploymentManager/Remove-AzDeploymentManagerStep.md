---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 96f5f9e3dd0390d714b0ee7a74b3f585b46dcc1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966307"
---
# <span data-ttu-id="6bb13-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6bb13-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="6bb13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb13-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb13-103">Удаляет шаг.</span><span class="sxs-lookup"><span data-stu-id="6bb13-103">Deletes the step.</span></span>

## <span data-ttu-id="6bb13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6bb13-104">SYNTAX</span></span>

### <span data-ttu-id="6bb13-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6bb13-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bb13-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bb13-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bb13-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6bb13-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb13-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb13-108">DESCRIPTION</span></span>
<span data-ttu-id="6bb13-109">Выполнение шага удаляется с учетом выполнения **cmdlet Remove-AzDeploymentManagerStep.**</span><span class="sxs-lookup"><span data-stu-id="6bb13-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="6bb13-110">Укажите шаг по имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bb13-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="6bb13-111">Кроме того, вы можете уступить шаг или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6bb13-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="6bb13-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6bb13-112">EXAMPLES</span></span>

### <span data-ttu-id="6bb13-113">Пример 1. Удаление шага</span><span class="sxs-lookup"><span data-stu-id="6bb13-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="6bb13-114">Эта команда удаляет шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6bb13-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6bb13-115">Пример 2. Удаление шага с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="6bb13-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="6bb13-116">Эта команда удаляет шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6bb13-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6bb13-117">Пример 3. Удаление шага с помощью объекта, New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6bb13-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="6bb13-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bb13-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="6bb13-119">Эта команда удаляет шаг, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="6bb13-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="6bb13-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bb13-120">PARAMETERS</span></span>

### <span data-ttu-id="6bb13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb13-121">-DefaultProfile</span></span>
<span data-ttu-id="6bb13-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bb13-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bb13-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bb13-123">-InputObject</span></span>
<span data-ttu-id="6bb13-124">Удаляемая пошаговая пошаго</span><span class="sxs-lookup"><span data-stu-id="6bb13-124">The step to be removed.</span></span>

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

### <span data-ttu-id="6bb13-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6bb13-125">-Name</span></span>
<span data-ttu-id="6bb13-126">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="6bb13-126">The name of the step.</span></span>

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

### <span data-ttu-id="6bb13-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bb13-127">-PassThru</span></span>
<span data-ttu-id="6bb13-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6bb13-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6bb13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb13-129">-ResourceGroupName</span></span>
<span data-ttu-id="6bb13-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bb13-130">The resource group.</span></span>

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

### <span data-ttu-id="6bb13-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bb13-131">-ResourceId</span></span>
<span data-ttu-id="6bb13-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6bb13-132">The resource identifier.</span></span>

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

### <span data-ttu-id="6bb13-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bb13-133">-Confirm</span></span>
<span data-ttu-id="6bb13-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6bb13-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bb13-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb13-135">-WhatIf</span></span>
<span data-ttu-id="6bb13-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bb13-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bb13-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6bb13-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bb13-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb13-138">CommonParameters</span></span>
<span data-ttu-id="6bb13-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb13-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb13-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bb13-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb13-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bb13-141">INPUTS</span></span>

### <span data-ttu-id="6bb13-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6bb13-142">System.String</span></span>

### <span data-ttu-id="6bb13-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="6bb13-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="6bb13-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6bb13-144">OUTPUTS</span></span>

### <span data-ttu-id="6bb13-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6bb13-145">System.Boolean</span></span>

## <span data-ttu-id="6bb13-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6bb13-146">NOTES</span></span>

## <span data-ttu-id="6bb13-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bb13-147">RELATED LINKS</span></span>
