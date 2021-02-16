---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242680"
---
# <span data-ttu-id="b4024-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="b4024-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="b4024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4024-102">SYNOPSIS</span></span>
<span data-ttu-id="b4024-103">Удаляет разетку.</span><span class="sxs-lookup"><span data-stu-id="b4024-103">Deletes the rollout.</span></span>

## <span data-ttu-id="b4024-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4024-104">SYNTAX</span></span>

### <span data-ttu-id="b4024-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4024-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4024-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4024-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4024-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4024-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4024-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4024-108">DESCRIPTION</span></span>
<span data-ttu-id="b4024-109">**Cmdlet Remove-AzDeploymentManagerRollout** удаляет разкат в состоянии терминала.</span><span class="sxs-lookup"><span data-stu-id="b4024-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="b4024-110">Укажите имя и группу ресурсов для разката.</span><span class="sxs-lookup"><span data-stu-id="b4024-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="b4024-111">Кроме того, вы можете предоставить объект rollout или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b4024-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="b4024-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4024-112">EXAMPLES</span></span>

### <span data-ttu-id="b4024-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4024-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="b4024-114">Эта команда удаляет раздатку с именем ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b4024-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4024-115">Пример 2. Удаление разката с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="b4024-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="b4024-116">Эта команда удаляет раздатку с именем ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b4024-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4024-117">Пример 3. Удаление разката с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="b4024-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="b4024-118">Эта команда удаляет разкат, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName соответствующего $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="b4024-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="b4024-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4024-119">PARAMETERS</span></span>

### <span data-ttu-id="b4024-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4024-120">-DefaultProfile</span></span>
<span data-ttu-id="b4024-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4024-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4024-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4024-122">-InputObject</span></span>
<span data-ttu-id="b4024-123">Удаляемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="b4024-123">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4024-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b4024-124">-Name</span></span>
<span data-ttu-id="b4024-125">Имя разката.</span><span class="sxs-lookup"><span data-stu-id="b4024-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="b4024-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4024-126">-PassThru</span></span>
<span data-ttu-id="b4024-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b4024-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b4024-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4024-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4024-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4024-129">The resource group.</span></span>

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

### <span data-ttu-id="b4024-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4024-130">-ResourceId</span></span>
<span data-ttu-id="b4024-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4024-131">The resource identifier.</span></span>

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

### <span data-ttu-id="b4024-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4024-132">-Confirm</span></span>
<span data-ttu-id="b4024-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b4024-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4024-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4024-134">-WhatIf</span></span>
<span data-ttu-id="b4024-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4024-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4024-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4024-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4024-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4024-137">CommonParameters</span></span>
<span data-ttu-id="b4024-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4024-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4024-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4024-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4024-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4024-140">INPUTS</span></span>

### <span data-ttu-id="b4024-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b4024-141">System.String</span></span>

### <span data-ttu-id="b4024-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="b4024-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b4024-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4024-143">OUTPUTS</span></span>

### <span data-ttu-id="b4024-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4024-144">System.Boolean</span></span>

## <span data-ttu-id="b4024-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4024-145">NOTES</span></span>

## <span data-ttu-id="b4024-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4024-146">RELATED LINKS</span></span>
