---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731704"
---
# <span data-ttu-id="c4e55-101">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c4e55-101">Stop-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="c4e55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4e55-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e55-103">Останавливает процесс развертывания.</span><span class="sxs-lookup"><span data-stu-id="c4e55-103">Stops a rollout in progress.</span></span>

## <span data-ttu-id="c4e55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4e55-104">SYNTAX</span></span>

### <span data-ttu-id="c4e55-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4e55-105">Interactive (Default)</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e55-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e55-106">ResourceId</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e55-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c4e55-107">InputObject</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4e55-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4e55-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e55-109">Командлет **Stop-AzureRmDeploymentManagerRollout** останавливает процесс развертывания и возвращает объект, который представляет текущее состояние выпуска.</span><span class="sxs-lookup"><span data-stu-id="c4e55-109">The **Stop-AzureRmDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="c4e55-110">Укажите имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4e55-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="c4e55-111">Кроме того, можно предоставить объект выпуска или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="c4e55-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="c4e55-112">Обратите внимание на то, что после прекращения выпуска приложение не может быть возобновлено или перезапущено.</span><span class="sxs-lookup"><span data-stu-id="c4e55-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="c4e55-113">Вы можете создать только новый выпуск.</span><span class="sxs-lookup"><span data-stu-id="c4e55-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="c4e55-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4e55-114">EXAMPLES</span></span>

### <span data-ttu-id="c4e55-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4e55-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="c4e55-116">Эта команда останавливает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c4e55-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="c4e55-117">Пример 2: прекращение выпуска с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="c4e55-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="c4e55-118">Эта команда останавливает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c4e55-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c4e55-119">Пример 3: прекращение выпуска с помощью объекта выпуска.</span><span class="sxs-lookup"><span data-stu-id="c4e55-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="c4e55-120">Эта команда останавливает выгрузку, имя и значение ResourceGroup которой соответствуют свойствам Name и ResourceGroupName для $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="c4e55-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="c4e55-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4e55-121">PARAMETERS</span></span>

### <span data-ttu-id="c4e55-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e55-122">-DefaultProfile</span></span>
<span data-ttu-id="c4e55-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4e55-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e55-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c4e55-124">-Force</span></span>
<span data-ttu-id="c4e55-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c4e55-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c4e55-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4e55-126">-Name</span></span>
<span data-ttu-id="c4e55-127">Имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="c4e55-127">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e55-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e55-128">-ResourceGroupName</span></span>
<span data-ttu-id="c4e55-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4e55-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e55-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e55-130">-ResourceId</span></span>
<span data-ttu-id="c4e55-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c4e55-131">The resource identifier.</span></span>

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

### <span data-ttu-id="c4e55-132">-Выпуск</span><span class="sxs-lookup"><span data-stu-id="c4e55-132">-Rollout</span></span>
<span data-ttu-id="c4e55-133">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c4e55-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="c4e55-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4e55-134">-Confirm</span></span>
<span data-ttu-id="c4e55-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4e55-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e55-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e55-136">-WhatIf</span></span>
<span data-ttu-id="c4e55-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c4e55-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4e55-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4e55-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e55-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e55-139">CommonParameters</span></span>
<span data-ttu-id="c4e55-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4e55-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e55-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e55-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e55-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4e55-142">INPUTS</span></span>

### <span data-ttu-id="c4e55-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="c4e55-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="c4e55-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4e55-144">OUTPUTS</span></span>

### <span data-ttu-id="c4e55-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="c4e55-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="c4e55-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4e55-146">NOTES</span></span>

## <span data-ttu-id="c4e55-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4e55-147">RELATED LINKS</span></span>

[<span data-ttu-id="c4e55-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c4e55-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="c4e55-149">Restarting-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c4e55-149">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="c4e55-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c4e55-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)