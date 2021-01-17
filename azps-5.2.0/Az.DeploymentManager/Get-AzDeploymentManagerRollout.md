---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324243"
---
# <span data-ttu-id="16310-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="16310-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="16310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16310-102">SYNOPSIS</span></span>
<span data-ttu-id="16310-103">Получает разкат.</span><span class="sxs-lookup"><span data-stu-id="16310-103">Gets the rollout.</span></span>

## <span data-ttu-id="16310-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16310-104">SYNTAX</span></span>

### <span data-ttu-id="16310-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16310-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16310-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="16310-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16310-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="16310-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16310-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16310-108">DESCRIPTION</span></span>
<span data-ttu-id="16310-109">**Cmdlet Get-AzDeploymentManagerRollout** получает сведение и возвращает объект, который представляет это сведение со всеми подробными сведениями о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="16310-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="16310-110">Укажите имя и группу ресурсов для разката.</span><span class="sxs-lookup"><span data-stu-id="16310-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="16310-111">Кроме того, вы можете предоставить объект rollout или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="16310-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="16310-112">В возвращаемом объекте развертывания содержатся службы, единицы обслуживания и этапы развертывания, которые были развернуты, а также те из них, которые уже развернуты.</span><span class="sxs-lookup"><span data-stu-id="16310-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="16310-113">Пока не будут развернуты те из них, которые нужно развернуть.</span><span class="sxs-lookup"><span data-stu-id="16310-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="16310-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16310-114">EXAMPLES</span></span>

### <span data-ttu-id="16310-115">Пример 1. Получить разкат</span><span class="sxs-lookup"><span data-stu-id="16310-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="16310-116">Эта команда получает раздатку ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="16310-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="16310-117">Пример 2. Получить и отобразить сведения о сведении о разкате</span><span class="sxs-lookup"><span data-stu-id="16310-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="16310-118">Эта команда получает раздатку ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="16310-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="16310-119">Переключатель -Verbose (Подробный) отображает все сведения о сведении с иерархической структурой; Показаны Службы,units и действия для каждого этапа и контекстная информация для каждого этапа, в котором показана целостная часть сведений.</span><span class="sxs-lookup"><span data-stu-id="16310-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="16310-120">Пример 3. Разкат с использованием идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="16310-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="16310-121">Эта команда получает раздатку ContosoRollout в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="16310-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="16310-122">Пример 4. Получить разкат с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="16310-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="16310-123">Эта команда получает разкат, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="16310-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="16310-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16310-124">PARAMETERS</span></span>

### <span data-ttu-id="16310-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16310-125">-DefaultProfile</span></span>
<span data-ttu-id="16310-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16310-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16310-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16310-127">-InputObject</span></span>
<span data-ttu-id="16310-128">Объект разката.</span><span class="sxs-lookup"><span data-stu-id="16310-128">Rollout object.</span></span>

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

### <span data-ttu-id="16310-129">-Name</span><span class="sxs-lookup"><span data-stu-id="16310-129">-Name</span></span>
<span data-ttu-id="16310-130">Имя разката.</span><span class="sxs-lookup"><span data-stu-id="16310-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="16310-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16310-131">-ResourceGroupName</span></span>
<span data-ttu-id="16310-132">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16310-132">The resource group.</span></span>

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

### <span data-ttu-id="16310-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16310-133">-ResourceId</span></span>
<span data-ttu-id="16310-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="16310-134">The resource identifier.</span></span>

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

### <span data-ttu-id="16310-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="16310-135">-RetryAttempt</span></span>
<span data-ttu-id="16310-136">Попытка повторного разката.</span><span class="sxs-lookup"><span data-stu-id="16310-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16310-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16310-137">CommonParameters</span></span>
<span data-ttu-id="16310-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16310-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16310-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16310-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16310-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16310-140">INPUTS</span></span>

### <span data-ttu-id="16310-141">System.String</span><span class="sxs-lookup"><span data-stu-id="16310-141">System.String</span></span>

### <span data-ttu-id="16310-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="16310-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="16310-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="16310-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="16310-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16310-144">OUTPUTS</span></span>

### <span data-ttu-id="16310-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="16310-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="16310-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16310-146">NOTES</span></span>

## <span data-ttu-id="16310-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16310-147">RELATED LINKS</span></span>
