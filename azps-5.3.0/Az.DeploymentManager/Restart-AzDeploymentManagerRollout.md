---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516898"
---
# <span data-ttu-id="fc6f1-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="fc6f1-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="fc6f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc6f1-103">Перезапуск сбойного раздатки.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="fc6f1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc6f1-104">SYNTAX</span></span>

### <span data-ttu-id="fc6f1-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc6f1-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc6f1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc6f1-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc6f1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc6f1-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc6f1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc6f1-108">DESCRIPTION</span></span>
<span data-ttu-id="fc6f1-109">С помощью **cmdlet Restart-AzDeploymentManagerRollout** можно перезапустить сбойный процесс и вернуть объект, который представляет этот процесс со всеми подробными сведениями о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="fc6f1-110">Укажите имя и группу ресурсов для разката.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="fc6f1-111">Кроме того, вы можете предоставить объект rollout или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="fc6f1-112">Необязательный параметр SkipSucceeded позволяет пропустить все предыдущие этапы.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="fc6f1-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc6f1-113">EXAMPLES</span></span>

### <span data-ttu-id="fc6f1-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc6f1-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="fc6f1-115">Эта команда перезапустит раздатку ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="fc6f1-116">Флаг SkipSucceed указывает на то, что все шаги, которые уже успешно выполнились, следует пропустить, а разкат должен продолжить выполнение, начиная с последнего сбойного действия.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="fc6f1-117">Пример 2. Перезапустите разкат с использованием идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="fc6f1-118">Эта команда перезапустит раздатку ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fc6f1-119">Пример 3. Перезапустите разкат с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="fc6f1-120">Эта команда перезапустит разкат, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="fc6f1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc6f1-121">PARAMETERS</span></span>

### <span data-ttu-id="fc6f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc6f1-122">-DefaultProfile</span></span>
<span data-ttu-id="fc6f1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc6f1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc6f1-124">-InputObject</span></span>
<span data-ttu-id="fc6f1-125">Удаляемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="fc6f1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fc6f1-126">-Name</span></span>
<span data-ttu-id="fc6f1-127">Имя разката.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="fc6f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc6f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc6f1-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-129">The resource group.</span></span>

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

### <span data-ttu-id="fc6f1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc6f1-130">-ResourceId</span></span>
<span data-ttu-id="fc6f1-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-131">The resource identifier.</span></span>

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

### <span data-ttu-id="fc6f1-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="fc6f1-132">-SkipSucceeded</span></span>
<span data-ttu-id="fc6f1-133">Пропустите шаги, которые удалось выполнить на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="fc6f1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc6f1-134">-Confirm</span></span>
<span data-ttu-id="fc6f1-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc6f1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc6f1-136">-WhatIf</span></span>
<span data-ttu-id="fc6f1-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc6f1-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc6f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc6f1-139">CommonParameters</span></span>
<span data-ttu-id="fc6f1-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc6f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc6f1-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc6f1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc6f1-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc6f1-142">INPUTS</span></span>

### <span data-ttu-id="fc6f1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fc6f1-143">System.String</span></span>

### <span data-ttu-id="fc6f1-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="fc6f1-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="fc6f1-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc6f1-145">OUTPUTS</span></span>

### <span data-ttu-id="fc6f1-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="fc6f1-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="fc6f1-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc6f1-147">NOTES</span></span>

## <span data-ttu-id="fc6f1-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc6f1-148">RELATED LINKS</span></span>
