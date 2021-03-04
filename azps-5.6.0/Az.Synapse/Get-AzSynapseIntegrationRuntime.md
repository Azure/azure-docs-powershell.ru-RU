---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 168a19c6e3900b395841aabbc19359d9fa4858f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981811"
---
# <span data-ttu-id="e8690-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e8690-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="e8690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8690-102">SYNOPSIS</span></span>
<span data-ttu-id="e8690-103">Сведения о ресурсах интеграции и времени работы.</span><span class="sxs-lookup"><span data-stu-id="e8690-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="e8690-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e8690-104">SYNTAX</span></span>

### <span data-ttu-id="e8690-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8690-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8690-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8690-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8690-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8690-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8690-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8690-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8690-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8690-109">DESCRIPTION</span></span>
<span data-ttu-id="e8690-110">Cmdlet **Get-AzSynapseIntegrationRuntime** получает сведения о времени интеграции в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e8690-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="e8690-111">Если указать имя времени запуска интеграции, этот cmdlet получит сведения об этом времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="e8690-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="e8690-112">Если имя не указано, этот cmdlet получает сведения обо всех процессах интеграции в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e8690-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="e8690-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e8690-113">EXAMPLES</span></span>

### <span data-ttu-id="e8690-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8690-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e8690-115">Перечислите все время интеграции в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e8690-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e8690-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e8690-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="e8690-117">Эта команда отображает сведения об интегрированной рабочей области с именем Test-selfhost-ir в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e8690-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e8690-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e8690-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="e8690-119">Эта команда отображает подробные состояния интеграции с именем test-selfhost-ir в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e8690-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e8690-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8690-120">PARAMETERS</span></span>

### <span data-ttu-id="e8690-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8690-121">-DefaultProfile</span></span>
<span data-ttu-id="e8690-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8690-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8690-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8690-123">-InputObject</span></span>
<span data-ttu-id="e8690-124">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="e8690-124">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8690-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e8690-125">-Name</span></span>
<span data-ttu-id="e8690-126">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="e8690-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8690-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8690-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8690-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8690-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8690-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8690-129">-ResourceId</span></span>
<span data-ttu-id="e8690-130">Идентификатор ресурса для времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="e8690-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8690-131">-Status</span><span class="sxs-lookup"><span data-stu-id="e8690-131">-Status</span></span>
<span data-ttu-id="e8690-132">Состояние подробных подробностей об интеграции.</span><span class="sxs-lookup"><span data-stu-id="e8690-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="e8690-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e8690-133">-WorkspaceName</span></span>
<span data-ttu-id="e8690-134">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="e8690-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8690-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e8690-135">-WorkspaceObject</span></span>
<span data-ttu-id="e8690-136">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="e8690-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8690-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8690-137">CommonParameters</span></span>
<span data-ttu-id="e8690-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8690-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8690-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8690-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8690-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8690-140">INPUTS</span></span>

### <span data-ttu-id="e8690-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8690-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e8690-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e8690-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e8690-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8690-143">OUTPUTS</span></span>

### <span data-ttu-id="e8690-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e8690-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e8690-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e8690-145">NOTES</span></span>

## <span data-ttu-id="e8690-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8690-146">RELATED LINKS</span></span>
