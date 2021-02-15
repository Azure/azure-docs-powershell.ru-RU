---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230585"
---
# <span data-ttu-id="7732e-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="7732e-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="7732e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7732e-102">SYNOPSIS</span></span>
<span data-ttu-id="7732e-103">Получает шаг.</span><span class="sxs-lookup"><span data-stu-id="7732e-103">Gets the step.</span></span>

## <span data-ttu-id="7732e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7732e-104">SYNTAX</span></span>

### <span data-ttu-id="7732e-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7732e-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7732e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7732e-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7732e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7732e-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7732e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7732e-108">DESCRIPTION</span></span>
<span data-ttu-id="7732e-109">**Cmdlet Get-AzDeploymentManagerStep** получает шаг и возвращает объект, который представляет его.</span><span class="sxs-lookup"><span data-stu-id="7732e-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="7732e-110">Укажите шаг по имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7732e-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="7732e-111">Кроме того, вы можете уступить шаг или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7732e-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="7732e-112">Вы можете изменить этот объект локально, а затем применить изменения к источнику артефакта с помощью Set-AzDeploymentManagerStep..</span><span class="sxs-lookup"><span data-stu-id="7732e-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="7732e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7732e-113">EXAMPLES</span></span>

### <span data-ttu-id="7732e-114">Пример 1. Получите шаг</span><span class="sxs-lookup"><span data-stu-id="7732e-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="7732e-115">Эта команда получает шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7732e-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="7732e-116">Пример 2. Шаг с использованием идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="7732e-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="7732e-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7732e-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="7732e-118">Эта команда получает шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7732e-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="7732e-119">Пример 3. Пошаговая поNew-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="7732e-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="7732e-120">Эта команда возвращает шаг, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="7732e-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="7732e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7732e-121">PARAMETERS</span></span>

### <span data-ttu-id="7732e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7732e-122">-DefaultProfile</span></span>
<span data-ttu-id="7732e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7732e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7732e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7732e-124">-InputObject</span></span>
<span data-ttu-id="7732e-125">Шаг объекта ресурса.</span><span class="sxs-lookup"><span data-stu-id="7732e-125">The step resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7732e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7732e-126">-Name</span></span>
<span data-ttu-id="7732e-127">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="7732e-127">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7732e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7732e-128">-ResourceGroupName</span></span>
<span data-ttu-id="7732e-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7732e-129">The resource group.</span></span>

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

### <span data-ttu-id="7732e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7732e-130">-ResourceId</span></span>
<span data-ttu-id="7732e-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="7732e-131">The resource identifier.</span></span>

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

### <span data-ttu-id="7732e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7732e-132">CommonParameters</span></span>
<span data-ttu-id="7732e-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7732e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7732e-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7732e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7732e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7732e-135">INPUTS</span></span>

### <span data-ttu-id="7732e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7732e-136">System.String</span></span>

### <span data-ttu-id="7732e-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="7732e-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="7732e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7732e-138">OUTPUTS</span></span>

### <span data-ttu-id="7732e-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="7732e-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="7732e-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7732e-140">NOTES</span></span>

## <span data-ttu-id="7732e-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7732e-141">RELATED LINKS</span></span>
