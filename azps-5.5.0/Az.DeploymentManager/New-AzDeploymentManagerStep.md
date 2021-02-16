---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242688"
---
# <span data-ttu-id="8bec2-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="8bec2-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="8bec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bec2-102">SYNOPSIS</span></span>
<span data-ttu-id="8bec2-103">Создает шаг.</span><span class="sxs-lookup"><span data-stu-id="8bec2-103">Creates a step.</span></span>

## <span data-ttu-id="8bec2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8bec2-104">SYNTAX</span></span>

### <span data-ttu-id="8bec2-105">Подождите (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bec2-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bec2-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="8bec2-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bec2-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="8bec2-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bec2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bec2-108">DESCRIPTION</span></span>
<span data-ttu-id="8bec2-109">Для выполнения развертывания создается этап **развертывания,** на который можно ссылаться в развертываниях.</span><span class="sxs-lookup"><span data-stu-id="8bec2-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="8bec2-110">Укажите *имя,* *имя группы ресурсов и* необходимые свойства.</span><span class="sxs-lookup"><span data-stu-id="8bec2-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="8bec2-111">Вы можете изменить возвращенный объект локально, а затем применить изменения к шагу с помощью Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="8bec2-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="8bec2-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8bec2-112">EXAMPLES</span></span>

### <span data-ttu-id="8bec2-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bec2-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="8bec2-114">Создает шаг в группе ContosoResourceGroup с именем ContosoService1WaitStep, в качестве расположения которого находится центр США.</span><span class="sxs-lookup"><span data-stu-id="8bec2-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="8bec2-115">Свойство Duration (Длительность) предоставляет длительность, которая будет выждать, прежде чем запускать следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="8bec2-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="8bec2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bec2-116">PARAMETERS</span></span>

### <span data-ttu-id="8bec2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bec2-117">-DefaultProfile</span></span>
<span data-ttu-id="8bec2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bec2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bec2-119">-Duration</span><span class="sxs-lookup"><span data-stu-id="8bec2-119">-Duration</span></span>
<span data-ttu-id="8bec2-120">Длительность ожидания в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="8bec2-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="8bec2-121">Например: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="8bec2-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="8bec2-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="8bec2-122">-HealthCheckProperties</span></span>
<span data-ttu-id="8bec2-123">Свойства проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="8bec2-123">The health check properties.</span></span>

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

### <span data-ttu-id="8bec2-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="8bec2-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="8bec2-125">Путь к файлу, в котором определены свойства проверки.</span><span class="sxs-lookup"><span data-stu-id="8bec2-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="8bec2-126">-Location</span><span class="sxs-lookup"><span data-stu-id="8bec2-126">-Location</span></span>
<span data-ttu-id="8bec2-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8bec2-127">The location of the resource.</span></span>

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

### <span data-ttu-id="8bec2-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8bec2-128">-Name</span></span>
<span data-ttu-id="8bec2-129">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="8bec2-129">The name of the step.</span></span>

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

### <span data-ttu-id="8bec2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bec2-130">-ResourceGroupName</span></span>
<span data-ttu-id="8bec2-131">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8bec2-131">The resource group.</span></span>

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

### <span data-ttu-id="8bec2-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="8bec2-132">-Tag</span></span>
<span data-ttu-id="8bec2-133">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="8bec2-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="8bec2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bec2-134">-Confirm</span></span>
<span data-ttu-id="8bec2-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8bec2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bec2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bec2-136">-WhatIf</span></span>
<span data-ttu-id="8bec2-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bec2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bec2-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8bec2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bec2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bec2-139">CommonParameters</span></span>
<span data-ttu-id="8bec2-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bec2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bec2-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bec2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bec2-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bec2-142">INPUTS</span></span>

### <span data-ttu-id="8bec2-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8bec2-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8bec2-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8bec2-144">OUTPUTS</span></span>

### <span data-ttu-id="8bec2-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="8bec2-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="8bec2-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8bec2-146">NOTES</span></span>

## <span data-ttu-id="8bec2-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bec2-147">RELATED LINKS</span></span>
