---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: d11a19ed5189220c8f6c327c9483e0e11e671ed8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980632"
---
# <span data-ttu-id="0b772-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="0b772-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="0b772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b772-102">SYNOPSIS</span></span>
<span data-ttu-id="0b772-103">Перезапуск сбойного раздатки.</span><span class="sxs-lookup"><span data-stu-id="0b772-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="0b772-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0b772-104">SYNTAX</span></span>

### <span data-ttu-id="0b772-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b772-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b772-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b772-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b772-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0b772-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b772-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b772-108">DESCRIPTION</span></span>
<span data-ttu-id="0b772-109">С помощью **cmdlet Restart-AzDeploymentManagerRollout** можно перезапустить процесс сбоя и вернуть объект, который представляет этот развернутый проект со всеми подробными сведениями о ходе его выполнения.</span><span class="sxs-lookup"><span data-stu-id="0b772-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="0b772-110">Укажите имя и группу ресурсов для разката.</span><span class="sxs-lookup"><span data-stu-id="0b772-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="0b772-111">Кроме того, вы можете предоставить объект rollout или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0b772-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="0b772-112">Необязательный параметр SkipSucceed позволяет пропустить все последующие действия, которые были пропущены в предыдущем запуске.</span><span class="sxs-lookup"><span data-stu-id="0b772-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="0b772-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0b772-113">EXAMPLES</span></span>

### <span data-ttu-id="0b772-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b772-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="0b772-115">Эта команда перезапустит раздатку ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0b772-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="0b772-116">Флаг SkipSucceed указывает на то, что все шаги, которые уже успешно выполнились, следует пропустить, а разкат должен продолжить выполнение, начиная с последнего сбойного действия.</span><span class="sxs-lookup"><span data-stu-id="0b772-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="0b772-117">Пример 2. Перезапустите разкат с использованием идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="0b772-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="0b772-118">Эта команда перезапустит раздатку ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0b772-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0b772-119">Пример 3. Перезапустите разкат с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="0b772-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="0b772-120">Эта команда перезапустит разкат, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="0b772-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="0b772-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b772-121">PARAMETERS</span></span>

### <span data-ttu-id="0b772-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b772-122">-DefaultProfile</span></span>
<span data-ttu-id="0b772-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b772-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b772-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b772-124">-InputObject</span></span>
<span data-ttu-id="0b772-125">Удаляемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="0b772-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="0b772-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0b772-126">-Name</span></span>
<span data-ttu-id="0b772-127">Имя разката.</span><span class="sxs-lookup"><span data-stu-id="0b772-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="0b772-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b772-128">-ResourceGroupName</span></span>
<span data-ttu-id="0b772-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b772-129">The resource group.</span></span>

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

### <span data-ttu-id="0b772-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b772-130">-ResourceId</span></span>
<span data-ttu-id="0b772-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b772-131">The resource identifier.</span></span>

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

### <span data-ttu-id="0b772-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="0b772-132">-SkipSucceeded</span></span>
<span data-ttu-id="0b772-133">Пропустите шаги, которые удалось выполнить на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="0b772-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="0b772-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b772-134">-Confirm</span></span>
<span data-ttu-id="0b772-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b772-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b772-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b772-136">-WhatIf</span></span>
<span data-ttu-id="0b772-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b772-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b772-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0b772-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b772-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b772-139">CommonParameters</span></span>
<span data-ttu-id="0b772-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b772-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b772-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b772-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b772-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b772-142">INPUTS</span></span>

### <span data-ttu-id="0b772-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0b772-143">System.String</span></span>

### <span data-ttu-id="0b772-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="0b772-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="0b772-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b772-145">OUTPUTS</span></span>

### <span data-ttu-id="0b772-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="0b772-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="0b772-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0b772-147">NOTES</span></span>

## <span data-ttu-id="0b772-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b772-148">RELATED LINKS</span></span>
