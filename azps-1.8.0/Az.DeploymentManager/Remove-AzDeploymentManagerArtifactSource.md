---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 1977fca9843c00d80d398a1dcd0bb967883cb5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730990"
---
# <span data-ttu-id="dc94b-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dc94b-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="dc94b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc94b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc94b-103">Удаляет указанный источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="dc94b-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="dc94b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc94b-104">SYNTAX</span></span>

### <span data-ttu-id="dc94b-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc94b-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc94b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc94b-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc94b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dc94b-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc94b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc94b-108">DESCRIPTION</span></span>
<span data-ttu-id="dc94b-109">Командлет **Remove-AzDeploymentManagerArtifactSource** удаляет источник артефакта, указав его имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc94b-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="dc94b-110">Кроме того, можно предоставить объект ArtifactSource или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="dc94b-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="dc94b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc94b-111">EXAMPLES</span></span>

### <span data-ttu-id="dc94b-112">Пример 1: удаление источника артефактов</span><span class="sxs-lookup"><span data-stu-id="dc94b-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="dc94b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc94b-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="dc94b-114">Эта команда удаляет источник артефакта с именем ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dc94b-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="dc94b-115">Пример 2: удаление источника артефакта с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="dc94b-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="dc94b-116">Эта команда удаляет источник артефакта с именем ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dc94b-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="dc94b-117">Пример 3: удаление источника артефакта с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="dc94b-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="dc94b-118">Эта команда удаляет источник артефакта, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="dc94b-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="dc94b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc94b-119">PARAMETERS</span></span>

### <span data-ttu-id="dc94b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc94b-120">-DefaultProfile</span></span>
<span data-ttu-id="dc94b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc94b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc94b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc94b-122">-InputObject</span></span>
<span data-ttu-id="dc94b-123">Удаляемый источник артефактов.</span><span class="sxs-lookup"><span data-stu-id="dc94b-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="dc94b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc94b-124">-Name</span></span>
<span data-ttu-id="dc94b-125">Имя источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="dc94b-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="dc94b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc94b-126">-PassThru</span></span>
<span data-ttu-id="dc94b-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="dc94b-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dc94b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc94b-128">-ResourceGroupName</span></span>
<span data-ttu-id="dc94b-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc94b-129">The resource group.</span></span>

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

### <span data-ttu-id="dc94b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc94b-130">-ResourceId</span></span>
<span data-ttu-id="dc94b-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="dc94b-131">The resource identifier.</span></span>

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

### <span data-ttu-id="dc94b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc94b-132">-Confirm</span></span>
<span data-ttu-id="dc94b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc94b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc94b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc94b-134">-WhatIf</span></span>
<span data-ttu-id="dc94b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc94b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc94b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc94b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc94b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc94b-137">CommonParameters</span></span>
<span data-ttu-id="dc94b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc94b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc94b-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc94b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc94b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc94b-140">INPUTS</span></span>

### <span data-ttu-id="dc94b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dc94b-141">System.String</span></span>

### <span data-ttu-id="dc94b-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dc94b-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="dc94b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc94b-143">OUTPUTS</span></span>

### <span data-ttu-id="dc94b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc94b-144">System.Boolean</span></span>

## <span data-ttu-id="dc94b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc94b-145">NOTES</span></span>

## <span data-ttu-id="dc94b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc94b-146">RELATED LINKS</span></span>
