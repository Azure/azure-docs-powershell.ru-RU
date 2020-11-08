---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247964"
---
# <span data-ttu-id="e26fa-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e26fa-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="e26fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e26fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e26fa-103">Получение сведений о ресурсах среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e26fa-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="e26fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e26fa-104">SYNTAX</span></span>

### <span data-ttu-id="e26fa-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e26fa-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26fa-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e26fa-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26fa-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e26fa-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e26fa-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e26fa-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e26fa-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e26fa-109">DESCRIPTION</span></span>
<span data-ttu-id="e26fa-110">Командлет **Get-AzSynapseIntegrationRuntime** получает сведения о средах выполнения интеграции в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e26fa-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="e26fa-111">Если вы задаете имя среды выполнения интеграции, этот командлет получает сведения о среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e26fa-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="e26fa-112">Если имя не задано, этот командлет получает сведения обо всех средах выполнения интеграции в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e26fa-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="e26fa-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e26fa-113">EXAMPLES</span></span>

### <span data-ttu-id="e26fa-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e26fa-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e26fa-115">Перечислите все среды выполнения интеграции в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e26fa-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e26fa-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e26fa-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="e26fa-117">Эта команда отображает сведения о среде выполнения интеграции с именем Test-SelfHost-IR в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e26fa-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e26fa-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e26fa-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="e26fa-119">Эта команда отображает сведения о состоянии среды выполнения интеграции с именем Test-SelfHost-IR в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e26fa-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e26fa-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e26fa-120">PARAMETERS</span></span>

### <span data-ttu-id="e26fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26fa-121">-DefaultProfile</span></span>
<span data-ttu-id="e26fa-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e26fa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e26fa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e26fa-123">-InputObject</span></span>
<span data-ttu-id="e26fa-124">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="e26fa-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="e26fa-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e26fa-125">-Name</span></span>
<span data-ttu-id="e26fa-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e26fa-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="e26fa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e26fa-127">-ResourceGroupName</span></span>
<span data-ttu-id="e26fa-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e26fa-128">Resource group name.</span></span>

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

### <span data-ttu-id="e26fa-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e26fa-129">-ResourceId</span></span>
<span data-ttu-id="e26fa-130">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="e26fa-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="e26fa-131">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="e26fa-131">-Status</span></span>
<span data-ttu-id="e26fa-132">Состояние сведений о среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e26fa-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="e26fa-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e26fa-133">-WorkspaceName</span></span>
<span data-ttu-id="e26fa-134">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e26fa-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e26fa-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e26fa-135">-WorkspaceObject</span></span>
<span data-ttu-id="e26fa-136">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e26fa-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e26fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26fa-137">CommonParameters</span></span>
<span data-ttu-id="e26fa-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e26fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26fa-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e26fa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26fa-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e26fa-140">INPUTS</span></span>

### <span data-ttu-id="e26fa-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e26fa-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e26fa-142">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e26fa-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e26fa-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e26fa-143">OUTPUTS</span></span>

### <span data-ttu-id="e26fa-144">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e26fa-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e26fa-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e26fa-145">NOTES</span></span>

## <span data-ttu-id="e26fa-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e26fa-146">RELATED LINKS</span></span>
