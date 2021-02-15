---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230588"
---
# <span data-ttu-id="1918b-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1918b-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="1918b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1918b-102">SYNOPSIS</span></span>

<span data-ttu-id="1918b-103">Возвращает источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="1918b-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="1918b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1918b-104">SYNTAX</span></span>

### <span data-ttu-id="1918b-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1918b-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1918b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1918b-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1918b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1918b-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1918b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1918b-108">DESCRIPTION</span></span>
<span data-ttu-id="1918b-109">**Cmdlet Get-AzDeploymentManagerArtifactSource** получает источник артефакта и возвращает объект, который представляет этот источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="1918b-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="1918b-110">Укажите источник артефакта по имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1918b-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="1918b-111">Кроме того, вы можете предоставить объект ArtifactSource или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1918b-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="1918b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1918b-112">EXAMPLES</span></span>

### <span data-ttu-id="1918b-113">Пример 1. Получить источник артефакта</span><span class="sxs-lookup"><span data-stu-id="1918b-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="1918b-114">Эта команда получает источник артефакта ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1918b-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="1918b-115">Пример 2. Получить источник артефакта с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="1918b-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="1918b-116">Эта команда получает источник артефакта ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1918b-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="1918b-117">Пример 3. Получить источник артефакта с помощью объекта, New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1918b-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="1918b-118">Эта команда возвращает источник артефакта, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="1918b-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="1918b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1918b-119">PARAMETERS</span></span>

### <span data-ttu-id="1918b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1918b-120">-DefaultProfile</span></span>
<span data-ttu-id="1918b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1918b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1918b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1918b-122">-InputObject</span></span>
<span data-ttu-id="1918b-123">Объект "Источник артефакта".</span><span class="sxs-lookup"><span data-stu-id="1918b-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="1918b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1918b-124">-Name</span></span>
<span data-ttu-id="1918b-125">Имя источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="1918b-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="1918b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1918b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1918b-127">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1918b-127">The resource group.</span></span>

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

### <span data-ttu-id="1918b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1918b-128">-ResourceId</span></span>
<span data-ttu-id="1918b-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="1918b-129">The resource identifier.</span></span>

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

### <span data-ttu-id="1918b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1918b-130">CommonParameters</span></span>
<span data-ttu-id="1918b-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1918b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1918b-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1918b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1918b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1918b-133">INPUTS</span></span>

### <span data-ttu-id="1918b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1918b-134">System.String</span></span>

### <span data-ttu-id="1918b-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1918b-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="1918b-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1918b-136">OUTPUTS</span></span>

### <span data-ttu-id="1918b-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1918b-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="1918b-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1918b-138">NOTES</span></span>

## <span data-ttu-id="1918b-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1918b-139">RELATED LINKS</span></span>
