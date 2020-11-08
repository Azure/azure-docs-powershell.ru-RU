---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242804"
---
# <span data-ttu-id="4a8f2-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="4a8f2-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="4a8f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8f2-103">Прекращение выпуска.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-103">Stops the rollout.</span></span>

## <span data-ttu-id="4a8f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a8f2-104">SYNTAX</span></span>

### <span data-ttu-id="4a8f2-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a8f2-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a8f2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a8f2-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a8f2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4a8f2-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a8f2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a8f2-108">DESCRIPTION</span></span>
<span data-ttu-id="4a8f2-109">Командлет **Stop-AzDeploymentManagerRollout** останавливает процесс развертывания и возвращает объект, который представляет текущее состояние выпуска.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="4a8f2-110">Укажите имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="4a8f2-111">Кроме того, можно предоставить объект выпуска или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="4a8f2-112">Обратите внимание на то, что после прекращения выпуска приложение не может быть возобновлено или перезапущено.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="4a8f2-113">Вы можете создать только новый выпуск.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="4a8f2-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a8f2-114">EXAMPLES</span></span>

### <span data-ttu-id="4a8f2-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a8f2-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="4a8f2-116">Эта команда останавливает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="4a8f2-117">Пример 2: прекращение выпуска с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="4a8f2-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="4a8f2-118">Эта команда останавливает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4a8f2-119">Пример 3: прекращение выпуска с помощью объекта выпуска.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="4a8f2-120">Эта команда останавливает выгрузку, имя и значение ResourceGroup которой соответствуют свойствам Name и ResourceGroupName для $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="4a8f2-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a8f2-121">PARAMETERS</span></span>

### <span data-ttu-id="4a8f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8f2-122">-DefaultProfile</span></span>
<span data-ttu-id="4a8f2-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a8f2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4a8f2-124">-Force</span></span>
<span data-ttu-id="4a8f2-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4a8f2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a8f2-126">-InputObject</span></span>
<span data-ttu-id="4a8f2-127">Удаляемый выпуск.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="4a8f2-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a8f2-128">-Name</span></span>
<span data-ttu-id="4a8f2-129">Имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="4a8f2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8f2-130">-ResourceGroupName</span></span>
<span data-ttu-id="4a8f2-131">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-131">The resource group.</span></span>

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

### <span data-ttu-id="4a8f2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a8f2-132">-ResourceId</span></span>
<span data-ttu-id="4a8f2-133">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-133">The resource identifier.</span></span>

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

### <span data-ttu-id="4a8f2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a8f2-134">-Confirm</span></span>
<span data-ttu-id="4a8f2-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a8f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a8f2-136">-WhatIf</span></span>
<span data-ttu-id="4a8f2-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a8f2-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a8f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8f2-139">CommonParameters</span></span>
<span data-ttu-id="4a8f2-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a8f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8f2-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a8f2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8f2-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a8f2-142">INPUTS</span></span>

### <span data-ttu-id="4a8f2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4a8f2-143">System.String</span></span>

### <span data-ttu-id="4a8f2-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="4a8f2-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="4a8f2-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a8f2-145">OUTPUTS</span></span>

### <span data-ttu-id="4a8f2-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="4a8f2-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="4a8f2-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a8f2-147">NOTES</span></span>

## <span data-ttu-id="4a8f2-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a8f2-148">RELATED LINKS</span></span>
