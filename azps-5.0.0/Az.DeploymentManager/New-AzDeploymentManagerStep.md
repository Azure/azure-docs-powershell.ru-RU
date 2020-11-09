---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312692"
---
# <span data-ttu-id="f75ff-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f75ff-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f75ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f75ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f75ff-103">Создание шага.</span><span class="sxs-lookup"><span data-stu-id="f75ff-103">Creates a step.</span></span>

## <span data-ttu-id="f75ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f75ff-104">SYNTAX</span></span>

### <span data-ttu-id="f75ff-105">Ожидание (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f75ff-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f75ff-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="f75ff-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f75ff-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="f75ff-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f75ff-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f75ff-108">DESCRIPTION</span></span>
<span data-ttu-id="f75ff-109">Командлет **New-AzDeploymentManagerStep** создает шаг развертывания, на который можно ссылаться при развертывании.</span><span class="sxs-lookup"><span data-stu-id="f75ff-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="f75ff-110">Укажите *имя* , *ResourceGroupName* и необходимые свойства.</span><span class="sxs-lookup"><span data-stu-id="f75ff-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="f75ff-111">Вы можете изменить возвращаемый объект на локальном компьютере, а затем применить изменения к шагу с помощью командлета Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="f75ff-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f75ff-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f75ff-112">EXAMPLES</span></span>

### <span data-ttu-id="f75ff-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f75ff-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="f75ff-114">Создает шаг в ContosoResourceGroup с именем ContosoService1WaitStep, где в качестве местоположения ресурса будет указана Центральная часть US.</span><span class="sxs-lookup"><span data-stu-id="f75ff-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="f75ff-115">Свойство Duration (длительность) — это время, в течение которого развертывание будет ожидать перед выполнением следующего этапа.</span><span class="sxs-lookup"><span data-stu-id="f75ff-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="f75ff-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f75ff-116">PARAMETERS</span></span>

### <span data-ttu-id="f75ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75ff-117">-DefaultProfile</span></span>
<span data-ttu-id="f75ff-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f75ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f75ff-119">-Duration</span><span class="sxs-lookup"><span data-stu-id="f75ff-119">-Duration</span></span>
<span data-ttu-id="f75ff-120">Продолжительность ожидания в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="f75ff-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="f75ff-121">Например: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="f75ff-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="f75ff-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="f75ff-122">-HealthCheckProperties</span></span>
<span data-ttu-id="f75ff-123">Свойства проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="f75ff-123">The health check properties.</span></span>

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

### <span data-ttu-id="f75ff-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="f75ff-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="f75ff-125">Путь к файлу, в котором определены свойства проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="f75ff-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="f75ff-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f75ff-126">-Location</span></span>
<span data-ttu-id="f75ff-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f75ff-127">The location of the resource.</span></span>

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

### <span data-ttu-id="f75ff-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f75ff-128">-Name</span></span>
<span data-ttu-id="f75ff-129">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="f75ff-129">The name of the step.</span></span>

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

### <span data-ttu-id="f75ff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f75ff-130">-ResourceGroupName</span></span>
<span data-ttu-id="f75ff-131">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f75ff-131">The resource group.</span></span>

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

### <span data-ttu-id="f75ff-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="f75ff-132">-Tag</span></span>
<span data-ttu-id="f75ff-133">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f75ff-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f75ff-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f75ff-134">-Confirm</span></span>
<span data-ttu-id="f75ff-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f75ff-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75ff-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75ff-136">-WhatIf</span></span>
<span data-ttu-id="f75ff-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f75ff-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f75ff-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f75ff-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75ff-139">CommonParameters</span></span>
<span data-ttu-id="f75ff-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f75ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75ff-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f75ff-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75ff-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f75ff-142">INPUTS</span></span>

### <span data-ttu-id="f75ff-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f75ff-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f75ff-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f75ff-144">OUTPUTS</span></span>

### <span data-ttu-id="f75ff-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f75ff-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f75ff-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="f75ff-146">NOTES</span></span>

## <span data-ttu-id="f75ff-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f75ff-147">RELATED LINKS</span></span>
