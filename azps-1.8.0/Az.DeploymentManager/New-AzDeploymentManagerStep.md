---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730991"
---
# <span data-ttu-id="bc5f5-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="bc5f5-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="bc5f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5f5-103">Создание шага.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-103">Creates a step.</span></span>

## <span data-ttu-id="bc5f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc5f5-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc5f5-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5f5-106">Командлет **New-AzDeploymentManagerStep** создает шаг развертывания, на который можно ссылаться при развертывании.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="bc5f5-107">Укажите *имя* , *ResourceGroupName* и необходимые свойства.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="bc5f5-108">Вы можете изменить возвращаемый объект на локальном компьютере, а затем применить изменения к шагу с помощью командлета Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="bc5f5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc5f5-109">EXAMPLES</span></span>

### <span data-ttu-id="bc5f5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc5f5-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="bc5f5-111">Создает шаг в ContosoResourceGroup с именем ContosoService1WaitStep, где в качестве местоположения ресурса будет указана Центральная часть US.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="bc5f5-112">Свойство Duration (длительность) — это время, в течение которого развертывание будет ожидать перед выполнением следующего этапа.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="bc5f5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc5f5-113">PARAMETERS</span></span>

### <span data-ttu-id="bc5f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5f5-114">-DefaultProfile</span></span>
<span data-ttu-id="bc5f5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc5f5-116">-Duration</span><span class="sxs-lookup"><span data-stu-id="bc5f5-116">-Duration</span></span>
<span data-ttu-id="bc5f5-117">Продолжительность ожидания в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="bc5f5-118">Например: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="bc5f5-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="bc5f5-119">-Location</span><span class="sxs-lookup"><span data-stu-id="bc5f5-119">-Location</span></span>
<span data-ttu-id="bc5f5-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-120">The location of the resource.</span></span>

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

### <span data-ttu-id="bc5f5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc5f5-121">-Name</span></span>
<span data-ttu-id="bc5f5-122">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-122">The name of the step.</span></span>

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

### <span data-ttu-id="bc5f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc5f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc5f5-124">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-124">The resource group.</span></span>

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

### <span data-ttu-id="bc5f5-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="bc5f5-125">-Tag</span></span>
<span data-ttu-id="bc5f5-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-126">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="bc5f5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc5f5-127">-Confirm</span></span>
<span data-ttu-id="bc5f5-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc5f5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5f5-129">-WhatIf</span></span>
<span data-ttu-id="bc5f5-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc5f5-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc5f5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5f5-132">CommonParameters</span></span>
<span data-ttu-id="bc5f5-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc5f5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5f5-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc5f5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5f5-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc5f5-135">INPUTS</span></span>

### <span data-ttu-id="bc5f5-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc5f5-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bc5f5-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc5f5-137">OUTPUTS</span></span>

### <span data-ttu-id="bc5f5-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="bc5f5-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="bc5f5-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc5f5-139">NOTES</span></span>

## <span data-ttu-id="bc5f5-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc5f5-140">RELATED LINKS</span></span>
