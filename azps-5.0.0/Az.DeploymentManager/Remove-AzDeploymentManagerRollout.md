---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312689"
---
# <span data-ttu-id="511fe-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="511fe-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="511fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="511fe-102">SYNOPSIS</span></span>
<span data-ttu-id="511fe-103">Удаляет выпуск.</span><span class="sxs-lookup"><span data-stu-id="511fe-103">Deletes the rollout.</span></span>

## <span data-ttu-id="511fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="511fe-104">SYNTAX</span></span>

### <span data-ttu-id="511fe-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="511fe-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511fe-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="511fe-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511fe-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="511fe-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511fe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="511fe-108">DESCRIPTION</span></span>
<span data-ttu-id="511fe-109">Командлет **Remove-AzDeploymentManagerRollout** удаляет выпуск в состоянии терминала.</span><span class="sxs-lookup"><span data-stu-id="511fe-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="511fe-110">Укажите имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="511fe-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="511fe-111">Кроме того, можно предоставить объект выпуска или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="511fe-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="511fe-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="511fe-112">EXAMPLES</span></span>

### <span data-ttu-id="511fe-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="511fe-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="511fe-114">Эта команда удаляет выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="511fe-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="511fe-115">Пример 2: удаление выпуска с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="511fe-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="511fe-116">Эта команда удаляет выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="511fe-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="511fe-117">Пример 3: удаление выпуска с помощью объекта выпуска.</span><span class="sxs-lookup"><span data-stu-id="511fe-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="511fe-118">Эта команда удаляет выпуску, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName в $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="511fe-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="511fe-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="511fe-119">PARAMETERS</span></span>

### <span data-ttu-id="511fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511fe-120">-DefaultProfile</span></span>
<span data-ttu-id="511fe-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="511fe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="511fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="511fe-122">-InputObject</span></span>
<span data-ttu-id="511fe-123">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="511fe-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="511fe-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="511fe-124">-Name</span></span>
<span data-ttu-id="511fe-125">Имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="511fe-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="511fe-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="511fe-126">-PassThru</span></span>
<span data-ttu-id="511fe-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="511fe-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="511fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="511fe-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="511fe-129">The resource group.</span></span>

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

### <span data-ttu-id="511fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="511fe-130">-ResourceId</span></span>
<span data-ttu-id="511fe-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="511fe-131">The resource identifier.</span></span>

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

### <span data-ttu-id="511fe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="511fe-132">-Confirm</span></span>
<span data-ttu-id="511fe-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="511fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511fe-134">-WhatIf</span></span>
<span data-ttu-id="511fe-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="511fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="511fe-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="511fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511fe-137">CommonParameters</span></span>
<span data-ttu-id="511fe-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="511fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511fe-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="511fe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511fe-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="511fe-140">INPUTS</span></span>

### <span data-ttu-id="511fe-141">System. String</span><span class="sxs-lookup"><span data-stu-id="511fe-141">System.String</span></span>

### <span data-ttu-id="511fe-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="511fe-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="511fe-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="511fe-143">OUTPUTS</span></span>

### <span data-ttu-id="511fe-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="511fe-144">System.Boolean</span></span>

## <span data-ttu-id="511fe-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="511fe-145">NOTES</span></span>

## <span data-ttu-id="511fe-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="511fe-146">RELATED LINKS</span></span>
