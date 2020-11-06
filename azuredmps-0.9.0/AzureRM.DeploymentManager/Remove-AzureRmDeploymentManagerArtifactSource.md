---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555312"
---
# <span data-ttu-id="f99b0-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f99b0-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="f99b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f99b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f99b0-103">Удаляет источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="f99b0-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="f99b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f99b0-104">SYNTAX</span></span>

### <span data-ttu-id="f99b0-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f99b0-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99b0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f99b0-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99b0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f99b0-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f99b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f99b0-108">DESCRIPTION</span></span>
<span data-ttu-id="f99b0-109">Командлет **Remove-AzureRmDeploymentManagerArtifactSource** удаляет источник артефакта, указав его имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f99b0-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="f99b0-110">Кроме того, можно предоставить объект ArtifactSource или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f99b0-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="f99b0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f99b0-111">EXAMPLES</span></span>

### <span data-ttu-id="f99b0-112">Пример 1: удаление источника артефактов</span><span class="sxs-lookup"><span data-stu-id="f99b0-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="f99b0-113">Эта команда удаляет источник артефакта с именем ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f99b0-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f99b0-114">Пример 2: удаление источника артефакта с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="f99b0-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="f99b0-115">Эта команда удаляет источник артефакта с именем ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f99b0-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f99b0-116">Пример 3: удаление источника артефакта с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="f99b0-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="f99b0-117">Эта команда удаляет источник артефакта, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="f99b0-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="f99b0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f99b0-118">PARAMETERS</span></span>

### <span data-ttu-id="f99b0-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f99b0-119">-ArtifactSource</span></span>
<span data-ttu-id="f99b0-120">Удаляемое хранилище артефактов.</span><span class="sxs-lookup"><span data-stu-id="f99b0-120">The artifact store to be removed.</span></span>

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

### <span data-ttu-id="f99b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99b0-121">-DefaultProfile</span></span>
<span data-ttu-id="f99b0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f99b0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f99b0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f99b0-123">-Force</span></span>
<span data-ttu-id="f99b0-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f99b0-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f99b0-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f99b0-125">-Name</span></span>
<span data-ttu-id="f99b0-126">Имя источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="f99b0-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="f99b0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f99b0-127">-PassThru</span></span>
<span data-ttu-id="f99b0-128">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="f99b0-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f99b0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f99b0-129">-ResourceGroupName</span></span>
<span data-ttu-id="f99b0-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f99b0-130">The resource group.</span></span>

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

### <span data-ttu-id="f99b0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f99b0-131">-ResourceId</span></span>
<span data-ttu-id="f99b0-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f99b0-132">The resource identifier.</span></span>

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

### <span data-ttu-id="f99b0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f99b0-133">-Confirm</span></span>
<span data-ttu-id="f99b0-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f99b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f99b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99b0-135">-WhatIf</span></span>
<span data-ttu-id="f99b0-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f99b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f99b0-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f99b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f99b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99b0-138">CommonParameters</span></span>
<span data-ttu-id="f99b0-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f99b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99b0-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f99b0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99b0-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f99b0-141">INPUTS</span></span>

### <span data-ttu-id="f99b0-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f99b0-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="f99b0-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f99b0-143">OUTPUTS</span></span>

### <span data-ttu-id="f99b0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f99b0-144">System.Boolean</span></span>

## <span data-ttu-id="f99b0-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f99b0-145">NOTES</span></span>

## <span data-ttu-id="f99b0-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f99b0-146">RELATED LINKS</span></span>

[<span data-ttu-id="f99b0-147">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f99b0-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="f99b0-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f99b0-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="f99b0-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f99b0-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)