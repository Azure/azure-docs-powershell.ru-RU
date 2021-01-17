---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426447"
---
# <span data-ttu-id="ba3c2-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="ba3c2-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="ba3c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3c2-103">Удаляет указанный источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="ba3c2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba3c2-104">SYNTAX</span></span>

### <span data-ttu-id="ba3c2-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba3c2-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba3c2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba3c2-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba3c2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ba3c2-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba3c2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba3c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ba3c2-109">С **помощью cmdlet Remove-AzDeploymentManagerArtifactSource** можно удалить источник артефакта, указав его имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="ba3c2-110">Кроме того, вы можете предоставить объект ArtifactSource или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="ba3c2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba3c2-111">EXAMPLES</span></span>

### <span data-ttu-id="ba3c2-112">Пример 1. Удаление источника артефакта</span><span class="sxs-lookup"><span data-stu-id="ba3c2-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="ba3c2-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba3c2-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="ba3c2-114">Эта команда удаляет источник артефакта ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="ba3c2-115">Пример 2. Удаление источника артефакта с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="ba3c2-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="ba3c2-116">Эта команда удаляет источник артефакта ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="ba3c2-117">Пример 3. Удаление источника артефакта с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="ba3c2-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="ba3c2-118">Эта команда удаляет источник артефакта, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="ba3c2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba3c2-119">PARAMETERS</span></span>

### <span data-ttu-id="ba3c2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3c2-120">-DefaultProfile</span></span>
<span data-ttu-id="ba3c2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba3c2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba3c2-122">-InputObject</span></span>
<span data-ttu-id="ba3c2-123">Источник артефакта, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-123">The artifact source to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba3c2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ba3c2-124">-Name</span></span>
<span data-ttu-id="ba3c2-125">Имя источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="ba3c2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba3c2-126">-PassThru</span></span>
<span data-ttu-id="ba3c2-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ba3c2-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ba3c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba3c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="ba3c2-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-129">The resource group.</span></span>

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

### <span data-ttu-id="ba3c2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba3c2-130">-ResourceId</span></span>
<span data-ttu-id="ba3c2-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-131">The resource identifier.</span></span>

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

### <span data-ttu-id="ba3c2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba3c2-132">-Confirm</span></span>
<span data-ttu-id="ba3c2-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba3c2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba3c2-134">-WhatIf</span></span>
<span data-ttu-id="ba3c2-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba3c2-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba3c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3c2-137">CommonParameters</span></span>
<span data-ttu-id="ba3c2-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3c2-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba3c2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3c2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba3c2-140">INPUTS</span></span>

### <span data-ttu-id="ba3c2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ba3c2-141">System.String</span></span>

### <span data-ttu-id="ba3c2-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="ba3c2-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="ba3c2-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba3c2-143">OUTPUTS</span></span>

### <span data-ttu-id="ba3c2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba3c2-144">System.Boolean</span></span>

## <span data-ttu-id="ba3c2-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba3c2-145">NOTES</span></span>

## <span data-ttu-id="ba3c2-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba3c2-146">RELATED LINKS</span></span>
