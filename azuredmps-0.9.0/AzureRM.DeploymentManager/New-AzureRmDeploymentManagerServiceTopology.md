---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: d7e3055c6443faa2c85d63e6cfdb611cb7d2eb41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556044"
---
# <span data-ttu-id="998a7-101">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="998a7-101">New-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="998a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="998a7-102">SYNOPSIS</span></span>
<span data-ttu-id="998a7-103">Создает новую топологию службы.</span><span class="sxs-lookup"><span data-stu-id="998a7-103">Creates a new service topology.</span></span>

## <span data-ttu-id="998a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="998a7-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="998a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="998a7-105">DESCRIPTION</span></span>
<span data-ttu-id="998a7-106">Командлет **New-AzureRmDeploymentManagerServiceTopology** создает топологию службы.</span><span class="sxs-lookup"><span data-stu-id="998a7-106">The **New-AzureRmDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="998a7-107">Вы можете изменить возвращаемый объект ServiceTopology на локальном компьютере, а затем применить изменения к топологии с помощью командлета Set-AzureRmDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="998a7-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="998a7-108">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="998a7-108">The returned object</span></span> 

<span data-ttu-id="998a7-109">Возвращенный объект содержит поле ResourceId, на которое можно ссылаться в ресурсе выпуска, чтобы указать, что службы, объявленные в этой топологии службы, будут развернуты в выпуске.</span><span class="sxs-lookup"><span data-stu-id="998a7-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="998a7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="998a7-110">EXAMPLES</span></span>

### <span data-ttu-id="998a7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="998a7-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="998a7-112">Этот командлет создает новую топологию службы в группе ресурсов ContosoResourceGroup с именем ContosoServiceTopology и в центральной области США.</span><span class="sxs-lookup"><span data-stu-id="998a7-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="998a7-113">Источник артефакта "ResourceId" указывает на то, что артефакты, необходимые для определений сервисных единиц в этой топологии, должны быть считаны из указанного источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="998a7-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="998a7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="998a7-114">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="998a7-115">Этот командлет создает новую топологию службы в группе ресурсов ContosoResourceGroup с именем ContosoServiceTopology и в центральной области США.</span><span class="sxs-lookup"><span data-stu-id="998a7-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="998a7-116">Отсутствие ссылки на источник артефакта указывает на то, что артефакты, необходимые для определений сервисных единиц в этой топологии, будут предоставляться как абсолютные URI SAS в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="998a7-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="998a7-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="998a7-117">PARAMETERS</span></span>

### <span data-ttu-id="998a7-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="998a7-118">-ArtifactSourceId</span></span>
<span data-ttu-id="998a7-119">Идентификатор источника артефактов, в котором хранятся артефакты, составляющие топологию.</span><span class="sxs-lookup"><span data-stu-id="998a7-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="998a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998a7-120">-DefaultProfile</span></span>
<span data-ttu-id="998a7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="998a7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="998a7-122">-Location</span><span class="sxs-lookup"><span data-stu-id="998a7-122">-Location</span></span>
<span data-ttu-id="998a7-123">Расположение топологии.</span><span class="sxs-lookup"><span data-stu-id="998a7-123">The location of the topology.</span></span>

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

### <span data-ttu-id="998a7-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="998a7-124">-Name</span></span>
<span data-ttu-id="998a7-125">Имя топологии.</span><span class="sxs-lookup"><span data-stu-id="998a7-125">The name of the topology.</span></span>

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

### <span data-ttu-id="998a7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998a7-126">-ResourceGroupName</span></span>
<span data-ttu-id="998a7-127">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="998a7-127">The resource group.</span></span>

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

### <span data-ttu-id="998a7-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="998a7-128">-Tag</span></span>
<span data-ttu-id="998a7-129">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="998a7-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="998a7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="998a7-130">-Confirm</span></span>
<span data-ttu-id="998a7-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="998a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="998a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998a7-132">-WhatIf</span></span>
<span data-ttu-id="998a7-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="998a7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="998a7-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="998a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="998a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998a7-135">CommonParameters</span></span>
<span data-ttu-id="998a7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="998a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998a7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998a7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998a7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="998a7-138">INPUTS</span></span>

### <span data-ttu-id="998a7-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="998a7-139">None</span></span>

## <span data-ttu-id="998a7-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="998a7-140">OUTPUTS</span></span>

### <span data-ttu-id="998a7-141">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="998a7-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="998a7-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="998a7-142">NOTES</span></span>

## <span data-ttu-id="998a7-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="998a7-143">RELATED LINKS</span></span>

[<span data-ttu-id="998a7-144">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="998a7-144">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="998a7-145">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="998a7-145">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="998a7-146">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="998a7-146">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)