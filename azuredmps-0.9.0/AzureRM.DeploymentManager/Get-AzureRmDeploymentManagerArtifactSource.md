---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731782"
---
# <span data-ttu-id="1e3e5-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1e3e5-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="1e3e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3e5-103">Возвращает источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-103">Gets an artifact source.</span></span>

## <span data-ttu-id="1e3e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e3e5-104">SYNTAX</span></span>

### <span data-ttu-id="1e3e5-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e3e5-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e3e5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e3e5-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e3e5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1e3e5-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e3e5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e3e5-108">DESCRIPTION</span></span>
<span data-ttu-id="1e3e5-109">Командлет **Get-AzureRmDeploymentManagerArtifactSource** получает источник артефактов и возвращает объект, представляющий этот источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="1e3e5-110">Укажите источник артефактов, указав его имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="1e3e5-111">Кроме того, можно предоставить объект ArtifactSource или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="1e3e5-112">Вы можете локально изменить этот объект, а затем применить изменения к источнику артефакта с помощью командлета Set-AzureRmDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="1e3e5-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e3e5-113">EXAMPLES</span></span>

### <span data-ttu-id="1e3e5-114">Пример 1: получение источника артефактов</span><span class="sxs-lookup"><span data-stu-id="1e3e5-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="1e3e5-115">Эта команда получает источник артефакта с именем ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="1e3e5-116">Пример 2: получение источника артефактов с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="1e3e5-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="1e3e5-117">Эта команда получает источник артефакта с именем ContosoArtifactSource в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="1e3e5-118">Пример 3: получение источника артефактов с помощью объекта, возвращаемого New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1e3e5-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="1e3e5-119">Эта команда получает источник артефакта, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="1e3e5-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e3e5-120">PARAMETERS</span></span>

### <span data-ttu-id="1e3e5-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1e3e5-121">-ArtifactSource</span></span>
<span data-ttu-id="1e3e5-122">Объект источника артефактов.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-122">Artifact Source object.</span></span>

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

### <span data-ttu-id="1e3e5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3e5-123">-DefaultProfile</span></span>
<span data-ttu-id="1e3e5-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e3e5-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e3e5-125">-Name</span></span>
<span data-ttu-id="1e3e5-126">Имя источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="1e3e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="1e3e5-128">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-128">The resource group.</span></span>

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

### <span data-ttu-id="1e3e5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e3e5-129">-ResourceId</span></span>
<span data-ttu-id="1e3e5-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-130">The resource identifier.</span></span>

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

### <span data-ttu-id="1e3e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3e5-131">CommonParameters</span></span>
<span data-ttu-id="1e3e5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e3e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3e5-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e3e5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3e5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e3e5-134">INPUTS</span></span>

### <span data-ttu-id="1e3e5-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="1e3e5-135">None</span></span>

## <span data-ttu-id="1e3e5-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e3e5-136">OUTPUTS</span></span>

### <span data-ttu-id="1e3e5-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1e3e5-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="1e3e5-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e3e5-138">NOTES</span></span>

## <span data-ttu-id="1e3e5-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e3e5-139">RELATED LINKS</span></span>

[<span data-ttu-id="1e3e5-140">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1e3e5-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="1e3e5-141">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1e3e5-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="1e3e5-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1e3e5-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)