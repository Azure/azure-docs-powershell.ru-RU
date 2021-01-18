---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505571"
---
# <span data-ttu-id="b930a-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b930a-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="b930a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b930a-102">SYNOPSIS</span></span>
<span data-ttu-id="b930a-103">Сведения о ресурсах интеграции и времени работы.</span><span class="sxs-lookup"><span data-stu-id="b930a-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="b930a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b930a-104">SYNTAX</span></span>

### <span data-ttu-id="b930a-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b930a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b930a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b930a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b930a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b930a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b930a-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b930a-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b930a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b930a-109">DESCRIPTION</span></span>
<span data-ttu-id="b930a-110">Cmdlet **Get-AzSynapseIntegrationRuntime** получает сведения об интеграции runtime в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b930a-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="b930a-111">Если указать имя времени запуска интеграции, этот cmdlet получит сведения об этом времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="b930a-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="b930a-112">Если имя не указано, этот cmdlet получает сведения обо всех процессах интеграции в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b930a-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="b930a-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b930a-113">EXAMPLES</span></span>

### <span data-ttu-id="b930a-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b930a-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b930a-115">Перечислите все время интеграции в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b930a-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b930a-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b930a-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="b930a-117">Эта команда отображает сведения об интегрированной рабочей области с именем Test-selfhost-ir в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b930a-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b930a-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b930a-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="b930a-119">Эта команда отображает подробное состояние времени интеграции с именем test-selfhost-ir в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b930a-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b930a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b930a-120">PARAMETERS</span></span>

### <span data-ttu-id="b930a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b930a-121">-DefaultProfile</span></span>
<span data-ttu-id="b930a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b930a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b930a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b930a-123">-InputObject</span></span>
<span data-ttu-id="b930a-124">Объект интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="b930a-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="b930a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b930a-125">-Name</span></span>
<span data-ttu-id="b930a-126">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="b930a-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="b930a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b930a-127">-ResourceGroupName</span></span>
<span data-ttu-id="b930a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b930a-128">Resource group name.</span></span>

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

### <span data-ttu-id="b930a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b930a-129">-ResourceId</span></span>
<span data-ttu-id="b930a-130">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="b930a-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="b930a-131">-Status</span><span class="sxs-lookup"><span data-stu-id="b930a-131">-Status</span></span>
<span data-ttu-id="b930a-132">Состояние подробных подробностей об интеграции.</span><span class="sxs-lookup"><span data-stu-id="b930a-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="b930a-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b930a-133">-WorkspaceName</span></span>
<span data-ttu-id="b930a-134">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="b930a-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b930a-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b930a-135">-WorkspaceObject</span></span>
<span data-ttu-id="b930a-136">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b930a-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b930a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b930a-137">CommonParameters</span></span>
<span data-ttu-id="b930a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b930a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b930a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b930a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b930a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b930a-140">INPUTS</span></span>

### <span data-ttu-id="b930a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b930a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b930a-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b930a-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b930a-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b930a-143">OUTPUTS</span></span>

### <span data-ttu-id="b930a-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b930a-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b930a-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b930a-145">NOTES</span></span>

## <span data-ttu-id="b930a-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b930a-146">RELATED LINKS</span></span>
