---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: f053adcd90b013df6f1678ed6468b2efa26d3ff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962083"
---
# <span data-ttu-id="47b79-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="47b79-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="47b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b79-102">SYNOPSIS</span></span>
<span data-ttu-id="47b79-103">Остановка разката.</span><span class="sxs-lookup"><span data-stu-id="47b79-103">Stops the rollout.</span></span>

## <span data-ttu-id="47b79-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47b79-104">SYNTAX</span></span>

### <span data-ttu-id="47b79-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47b79-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b79-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="47b79-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b79-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="47b79-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b79-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47b79-108">DESCRIPTION</span></span>
<span data-ttu-id="47b79-109">**Cmdlet Stop-AzDeploymentManagerRollout** останавливает процесс выполнения и возвращает объект, который представляет текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="47b79-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="47b79-110">Укажите имя и группу ресурсов для разката.</span><span class="sxs-lookup"><span data-stu-id="47b79-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="47b79-111">Кроме того, вы можете предоставить объект rollout или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="47b79-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="47b79-112">Обратите внимание на то, что после того как он будет остановлен, его нельзя будет возобновить или перезапустить.</span><span class="sxs-lookup"><span data-stu-id="47b79-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="47b79-113">Вы можете создать только новый разкат.</span><span class="sxs-lookup"><span data-stu-id="47b79-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="47b79-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47b79-114">EXAMPLES</span></span>

### <span data-ttu-id="47b79-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47b79-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="47b79-116">Эта команда останавливает разкат ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="47b79-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="47b79-117">Пример 2. Остановка разката с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="47b79-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="47b79-118">Эта команда останавливает разбитие ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="47b79-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="47b79-119">Пример 3. Остановка разката с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="47b79-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="47b79-120">Эта команда останавливает разкат, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="47b79-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="47b79-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47b79-121">PARAMETERS</span></span>

### <span data-ttu-id="47b79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b79-122">-DefaultProfile</span></span>
<span data-ttu-id="47b79-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47b79-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b79-124">-Force</span><span class="sxs-lookup"><span data-stu-id="47b79-124">-Force</span></span>
<span data-ttu-id="47b79-125">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="47b79-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47b79-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47b79-126">-InputObject</span></span>
<span data-ttu-id="47b79-127">Удаляемая разетка.</span><span class="sxs-lookup"><span data-stu-id="47b79-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="47b79-128">-Name</span><span class="sxs-lookup"><span data-stu-id="47b79-128">-Name</span></span>
<span data-ttu-id="47b79-129">Имя разката.</span><span class="sxs-lookup"><span data-stu-id="47b79-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="47b79-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b79-130">-ResourceGroupName</span></span>
<span data-ttu-id="47b79-131">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47b79-131">The resource group.</span></span>

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

### <span data-ttu-id="47b79-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47b79-132">-ResourceId</span></span>
<span data-ttu-id="47b79-133">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="47b79-133">The resource identifier.</span></span>

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

### <span data-ttu-id="47b79-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47b79-134">-Confirm</span></span>
<span data-ttu-id="47b79-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b79-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b79-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b79-136">-WhatIf</span></span>
<span data-ttu-id="47b79-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b79-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b79-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47b79-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b79-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b79-139">CommonParameters</span></span>
<span data-ttu-id="47b79-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b79-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b79-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47b79-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b79-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47b79-142">INPUTS</span></span>

### <span data-ttu-id="47b79-143">System.String</span><span class="sxs-lookup"><span data-stu-id="47b79-143">System.String</span></span>

### <span data-ttu-id="47b79-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="47b79-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="47b79-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47b79-145">OUTPUTS</span></span>

### <span data-ttu-id="47b79-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="47b79-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="47b79-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47b79-147">NOTES</span></span>

## <span data-ttu-id="47b79-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47b79-148">RELATED LINKS</span></span>
