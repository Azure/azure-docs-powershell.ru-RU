---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312752"
---
# <span data-ttu-id="b4f47-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b4f47-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b4f47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4f47-102">SYNOPSIS</span></span>

<span data-ttu-id="b4f47-103">Возвращает источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="b4f47-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="b4f47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4f47-104">SYNTAX</span></span>

### <span data-ttu-id="b4f47-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4f47-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4f47-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4f47-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f47-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4f47-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4f47-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4f47-108">DESCRIPTION</span></span>
<span data-ttu-id="b4f47-109">Командлет **Get-AzDeploymentManagerArtifactSource** получает источник артефактов и возвращает объект, представляющий этот источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="b4f47-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="b4f47-110">Укажите источник артефактов, указав его имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4f47-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="b4f47-111">Кроме того, можно предоставить объект ArtifactSource или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b4f47-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="b4f47-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4f47-112">EXAMPLES</span></span>

### <span data-ttu-id="b4f47-113">Пример 1: получение источника артефактов</span><span class="sxs-lookup"><span data-stu-id="b4f47-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="b4f47-114">Эта команда получает источник артефакта с именем ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b4f47-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4f47-115">Пример 2: получение источника артефактов с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="b4f47-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="b4f47-116">Эта команда получает источник артефакта с именем ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b4f47-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4f47-117">Пример 3: получение источника артефактов с помощью объекта, возвращаемого New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b4f47-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="b4f47-118">Эта команда получает источник артефакта, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="b4f47-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="b4f47-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4f47-119">PARAMETERS</span></span>

### <span data-ttu-id="b4f47-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f47-120">-DefaultProfile</span></span>
<span data-ttu-id="b4f47-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4f47-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4f47-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4f47-122">-InputObject</span></span>
<span data-ttu-id="b4f47-123">Объект источника артефактов.</span><span class="sxs-lookup"><span data-stu-id="b4f47-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="b4f47-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4f47-124">-Name</span></span>
<span data-ttu-id="b4f47-125">Имя источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="b4f47-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="b4f47-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f47-126">-ResourceGroupName</span></span>
<span data-ttu-id="b4f47-127">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4f47-127">The resource group.</span></span>

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

### <span data-ttu-id="b4f47-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4f47-128">-ResourceId</span></span>
<span data-ttu-id="b4f47-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4f47-129">The resource identifier.</span></span>

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

### <span data-ttu-id="b4f47-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f47-130">CommonParameters</span></span>
<span data-ttu-id="b4f47-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4f47-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f47-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4f47-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f47-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4f47-133">INPUTS</span></span>

### <span data-ttu-id="b4f47-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b4f47-134">System.String</span></span>

### <span data-ttu-id="b4f47-135">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b4f47-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b4f47-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4f47-136">OUTPUTS</span></span>

### <span data-ttu-id="b4f47-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b4f47-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b4f47-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4f47-138">NOTES</span></span>

## <span data-ttu-id="b4f47-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4f47-139">RELATED LINKS</span></span>
