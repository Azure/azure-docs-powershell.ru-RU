---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230580"
---
# <span data-ttu-id="debeb-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="debeb-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="debeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="debeb-102">SYNOPSIS</span></span>
<span data-ttu-id="debeb-103">Создает топологию службы.</span><span class="sxs-lookup"><span data-stu-id="debeb-103">Creates a service topology.</span></span>

## <span data-ttu-id="debeb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="debeb-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="debeb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="debeb-105">DESCRIPTION</span></span>
<span data-ttu-id="debeb-106">Для создания топологии службы будет создаваться **cmdlet New-AzDeploymentManagerServiceTopology.**</span><span class="sxs-lookup"><span data-stu-id="debeb-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="debeb-107">Вы можете изменить возвращенный объект ServiceTopology локально, а затем применить изменения к топологии с помощью Set-AzDeploymentManagerServiceTopology-топологии.</span><span class="sxs-lookup"><span data-stu-id="debeb-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="debeb-108">Возвращенный объект</span><span class="sxs-lookup"><span data-stu-id="debeb-108">The returned object</span></span> 

<span data-ttu-id="debeb-109">У возвращаемого объекта есть поле ResourceId, на которое можно ссылаться в ресурсе развертывания, чтобы указать, что в развертывании будут развернуты службы, объявленные в этой топологии службы.</span><span class="sxs-lookup"><span data-stu-id="debeb-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="debeb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="debeb-110">EXAMPLES</span></span>

### <span data-ttu-id="debeb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="debeb-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="debeb-112">Этот cmdlet создает новую топологию службы в группе ресурсов ContosoResourceGroup с именем ContosoServiceTopology и расположением Central US.</span><span class="sxs-lookup"><span data-stu-id="debeb-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="debeb-113">Источник артефакта ResourceId указывает на то, что артефакты, необходимые для определений единицы обслуживания в данной топологии, должны быть прочитано из указанного источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="debeb-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="debeb-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="debeb-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="debeb-115">Этот cmdlet создает новую топологию службы в группе ресурсов ContosoResourceGroup с именем ContosoServiceTopology и расположением Central US.</span><span class="sxs-lookup"><span data-stu-id="debeb-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="debeb-116">Отсутствие ссылки на источник артефакта указывает на то, что артефакты, необходимые для определений единицы обслуживания в данной топологии, должны быть предоставлены как абсолютные ЮРИС SAS в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="debeb-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="debeb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="debeb-117">PARAMETERS</span></span>

### <span data-ttu-id="debeb-118">-АртефактSourceId</span><span class="sxs-lookup"><span data-stu-id="debeb-118">-ArtifactSourceId</span></span>
<span data-ttu-id="debeb-119">Идентификатор источника артефакта, в котором хранятся артефакты, которые составляют топологию.</span><span class="sxs-lookup"><span data-stu-id="debeb-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debeb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debeb-120">-DefaultProfile</span></span>
<span data-ttu-id="debeb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="debeb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="debeb-122">-Location</span><span class="sxs-lookup"><span data-stu-id="debeb-122">-Location</span></span>
<span data-ttu-id="debeb-123">Расположение топологии.</span><span class="sxs-lookup"><span data-stu-id="debeb-123">The location of the topology.</span></span>

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

### <span data-ttu-id="debeb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="debeb-124">-Name</span></span>
<span data-ttu-id="debeb-125">Имя топологии.</span><span class="sxs-lookup"><span data-stu-id="debeb-125">The name of the topology.</span></span>

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

### <span data-ttu-id="debeb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="debeb-126">-ResourceGroupName</span></span>
<span data-ttu-id="debeb-127">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="debeb-127">The resource group.</span></span>

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

### <span data-ttu-id="debeb-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="debeb-128">-Tag</span></span>
<span data-ttu-id="debeb-129">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="debeb-129">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debeb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="debeb-130">-Confirm</span></span>
<span data-ttu-id="debeb-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="debeb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="debeb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="debeb-132">-WhatIf</span></span>
<span data-ttu-id="debeb-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="debeb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="debeb-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="debeb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="debeb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debeb-135">CommonParameters</span></span>
<span data-ttu-id="debeb-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="debeb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debeb-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="debeb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debeb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="debeb-138">INPUTS</span></span>

### <span data-ttu-id="debeb-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="debeb-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="debeb-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="debeb-140">OUTPUTS</span></span>

### <span data-ttu-id="debeb-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="debeb-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="debeb-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="debeb-142">NOTES</span></span>

## <span data-ttu-id="debeb-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="debeb-143">RELATED LINKS</span></span>
