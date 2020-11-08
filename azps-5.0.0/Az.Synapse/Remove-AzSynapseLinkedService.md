---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247913"
---
# <span data-ttu-id="e0780-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="e0780-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="e0780-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0780-102">SYNOPSIS</span></span>
<span data-ttu-id="e0780-103">Удаляет связанную службу из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e0780-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="e0780-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0780-104">SYNTAX</span></span>

### <span data-ttu-id="e0780-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0780-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0780-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e0780-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0780-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0780-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0780-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0780-108">DESCRIPTION</span></span>
<span data-ttu-id="e0780-109">Командлет **Remove-AzSynapseLinkedService** Удаляет связанную службу из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e0780-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="e0780-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0780-110">EXAMPLES</span></span>

### <span data-ttu-id="e0780-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0780-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="e0780-112">Эта команда удаляет связанную службу с именем ContosoLinkedService из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e0780-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e0780-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e0780-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="e0780-114">Эта команда удаляет связанную службу с именем ContosoLinkedService из рабочей области с именем ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="e0780-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="e0780-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e0780-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="e0780-116">Эта команда удаляет связанную службу с именем ContosoLinkedService из рабочей области с именем ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="e0780-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e0780-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0780-117">PARAMETERS</span></span>

### <span data-ttu-id="e0780-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0780-118">-AsJob</span></span>
<span data-ttu-id="e0780-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e0780-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0780-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0780-120">-DefaultProfile</span></span>
<span data-ttu-id="e0780-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0780-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0780-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0780-122">-InputObject</span></span>
<span data-ttu-id="e0780-123">Объект связанной службы.</span><span class="sxs-lookup"><span data-stu-id="e0780-123">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0780-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0780-124">-Name</span></span>
<span data-ttu-id="e0780-125">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="e0780-125">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0780-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0780-126">-PassThru</span></span>
<span data-ttu-id="e0780-127">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0780-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e0780-128">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="e0780-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e0780-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0780-129">-WorkspaceName</span></span>
<span data-ttu-id="e0780-130">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e0780-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0780-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e0780-131">-WorkspaceObject</span></span>
<span data-ttu-id="e0780-132">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e0780-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0780-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0780-133">-Confirm</span></span>
<span data-ttu-id="e0780-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e0780-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0780-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0780-135">-WhatIf</span></span>
<span data-ttu-id="e0780-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e0780-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0780-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e0780-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0780-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0780-138">CommonParameters</span></span>
<span data-ttu-id="e0780-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0780-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0780-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0780-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0780-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0780-141">INPUTS</span></span>

### <span data-ttu-id="e0780-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0780-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e0780-143">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="e0780-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="e0780-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0780-144">OUTPUTS</span></span>

### <span data-ttu-id="e0780-145">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="e0780-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="e0780-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0780-146">NOTES</span></span>

## <span data-ttu-id="e0780-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0780-147">RELATED LINKS</span></span>
