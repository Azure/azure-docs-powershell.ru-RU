---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: e53f2e72a10befb126bc9cc20dc12bf8990b1553
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730980"
---
# <span data-ttu-id="608e4-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="608e4-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="608e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="608e4-102">SYNOPSIS</span></span>
<span data-ttu-id="608e4-103">Перезапускает сбой.</span><span class="sxs-lookup"><span data-stu-id="608e4-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="608e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="608e4-104">SYNTAX</span></span>

### <span data-ttu-id="608e4-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="608e4-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608e4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="608e4-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608e4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="608e4-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="608e4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="608e4-108">DESCRIPTION</span></span>
<span data-ttu-id="608e4-109">Командлет **restarting-AzDeploymentManagerRollout** перезапускает сбой и возвращает объект, который представляет собой все подробные сведения о ходе выпуска.</span><span class="sxs-lookup"><span data-stu-id="608e4-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="608e4-110">Укажите имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="608e4-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="608e4-111">Кроме того, можно предоставить объект выпуска или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="608e4-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="608e4-112">Необязательный параметр SkipSucceeded позволяет пропустить все этапы, успешно описанные в предыдущем запуске выпуска.</span><span class="sxs-lookup"><span data-stu-id="608e4-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="608e4-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="608e4-113">EXAMPLES</span></span>

### <span data-ttu-id="608e4-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="608e4-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="608e4-115">Эта команда перезапускает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="608e4-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="608e4-116">Флаг SkipSucceeded указывает на то, что все шаги, которые уже выполнялись успешно, должны быть пропущены, а выпуск должен продолжить выполнение с того места, на котором он завершился последним сбоем.</span><span class="sxs-lookup"><span data-stu-id="608e4-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="608e4-117">Пример 2: перезапуск выпуска с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="608e4-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="608e4-118">Эта команда перезапускает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="608e4-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="608e4-119">Пример 3. Перезапустите развертывание с помощью объекта выпуска.</span><span class="sxs-lookup"><span data-stu-id="608e4-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="608e4-120">Эта команда перезапускает выгрузку, имя и значение ResourceGroup которой совпадают со свойствами Name и ResourceGroupName в $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="608e4-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="608e4-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="608e4-121">PARAMETERS</span></span>

### <span data-ttu-id="608e4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608e4-122">-DefaultProfile</span></span>
<span data-ttu-id="608e4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="608e4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="608e4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="608e4-124">-InputObject</span></span>
<span data-ttu-id="608e4-125">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="608e4-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="608e4-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="608e4-126">-Name</span></span>
<span data-ttu-id="608e4-127">Имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="608e4-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="608e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="608e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="608e4-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="608e4-129">The resource group.</span></span>

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

### <span data-ttu-id="608e4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="608e4-130">-ResourceId</span></span>
<span data-ttu-id="608e4-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="608e4-131">The resource identifier.</span></span>

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

### <span data-ttu-id="608e4-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="608e4-132">-SkipSucceeded</span></span>
<span data-ttu-id="608e4-133">Пропустите шаги, которые были выполнены в предыдущем запуске выпуска.</span><span class="sxs-lookup"><span data-stu-id="608e4-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="608e4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="608e4-134">-Confirm</span></span>
<span data-ttu-id="608e4-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="608e4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="608e4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="608e4-136">-WhatIf</span></span>
<span data-ttu-id="608e4-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="608e4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="608e4-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="608e4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="608e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608e4-139">CommonParameters</span></span>
<span data-ttu-id="608e4-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="608e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608e4-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="608e4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608e4-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="608e4-142">INPUTS</span></span>

### <span data-ttu-id="608e4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="608e4-143">System.String</span></span>

### <span data-ttu-id="608e4-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="608e4-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="608e4-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="608e4-145">OUTPUTS</span></span>

### <span data-ttu-id="608e4-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="608e4-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="608e4-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="608e4-147">NOTES</span></span>

## <span data-ttu-id="608e4-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="608e4-148">RELATED LINKS</span></span>
