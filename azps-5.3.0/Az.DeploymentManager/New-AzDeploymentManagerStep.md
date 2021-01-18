---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506396"
---
# <span data-ttu-id="31744-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="31744-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="31744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31744-102">SYNOPSIS</span></span>
<span data-ttu-id="31744-103">Создает шаг.</span><span class="sxs-lookup"><span data-stu-id="31744-103">Creates a step.</span></span>

## <span data-ttu-id="31744-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31744-104">SYNTAX</span></span>

### <span data-ttu-id="31744-105">Подождите (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31744-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31744-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="31744-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31744-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="31744-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31744-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31744-108">DESCRIPTION</span></span>
<span data-ttu-id="31744-109">Для выполнения развертывания создается этап **развертывания,** на который можно ссылаться в развертываниях.</span><span class="sxs-lookup"><span data-stu-id="31744-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="31744-110">Укажите *имя,* *имя группы ресурсов и* необходимые свойства.</span><span class="sxs-lookup"><span data-stu-id="31744-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="31744-111">Вы можете изменить возвращенный объект локально, а затем применить изменения к шагу с помощью Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="31744-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="31744-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31744-112">EXAMPLES</span></span>

### <span data-ttu-id="31744-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31744-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="31744-114">Создает шаг в группе ContosoResourceGroup с именем ContosoService1WaitStep, в качестве расположения которого находится центр США.</span><span class="sxs-lookup"><span data-stu-id="31744-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="31744-115">Свойство Duration (Длительность) предоставляет длительность, которая будет выждать, прежде чем запускать следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="31744-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="31744-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31744-116">PARAMETERS</span></span>

### <span data-ttu-id="31744-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31744-117">-DefaultProfile</span></span>
<span data-ttu-id="31744-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31744-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31744-119">-Duration</span><span class="sxs-lookup"><span data-stu-id="31744-119">-Duration</span></span>
<span data-ttu-id="31744-120">Длительность ожидания в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="31744-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="31744-121">Например: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="31744-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31744-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="31744-122">-HealthCheckProperties</span></span>
<span data-ttu-id="31744-123">Свойства проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="31744-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31744-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="31744-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="31744-125">Путь к файлу, в котором определены свойства проверки.</span><span class="sxs-lookup"><span data-stu-id="31744-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31744-126">-Location</span><span class="sxs-lookup"><span data-stu-id="31744-126">-Location</span></span>
<span data-ttu-id="31744-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="31744-127">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31744-128">-Name</span><span class="sxs-lookup"><span data-stu-id="31744-128">-Name</span></span>
<span data-ttu-id="31744-129">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="31744-129">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31744-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31744-130">-ResourceGroupName</span></span>
<span data-ttu-id="31744-131">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31744-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31744-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="31744-132">-Tag</span></span>
<span data-ttu-id="31744-133">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="31744-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31744-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31744-134">-Confirm</span></span>
<span data-ttu-id="31744-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31744-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31744-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31744-136">-WhatIf</span></span>
<span data-ttu-id="31744-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31744-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31744-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="31744-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31744-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31744-139">CommonParameters</span></span>
<span data-ttu-id="31744-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31744-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31744-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31744-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31744-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31744-142">INPUTS</span></span>

### <span data-ttu-id="31744-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="31744-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="31744-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31744-144">OUTPUTS</span></span>

### <span data-ttu-id="31744-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="31744-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="31744-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31744-146">NOTES</span></span>

## <span data-ttu-id="31744-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31744-147">RELATED LINKS</span></span>
