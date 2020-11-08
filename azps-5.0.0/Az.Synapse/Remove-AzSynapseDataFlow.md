---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: dcfcd391d1103b0755a3ffae481e4f1bd5fde2c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249290"
---
# <span data-ttu-id="2d1cb-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="2d1cb-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="2d1cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d1cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2d1cb-103">Удаляет поток данных из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="2d1cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d1cb-104">SYNTAX</span></span>

### <span data-ttu-id="2d1cb-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d1cb-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d1cb-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="2d1cb-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d1cb-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="2d1cb-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d1cb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d1cb-108">DESCRIPTION</span></span>
<span data-ttu-id="2d1cb-109">Командлет **Remove-AzSynapseDataFlow** удаляет поток данных из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="2d1cb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d1cb-110">EXAMPLES</span></span>

### <span data-ttu-id="2d1cb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d1cb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="2d1cb-112">Эта команда удаляет поток данных с именем ContosoDataFlow из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2d1cb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d1cb-113">PARAMETERS</span></span>

### <span data-ttu-id="2d1cb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d1cb-114">-AsJob</span></span>
<span data-ttu-id="2d1cb-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2d1cb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d1cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d1cb-116">-DefaultProfile</span></span>
<span data-ttu-id="2d1cb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d1cb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d1cb-118">-InputObject</span></span>
<span data-ttu-id="2d1cb-119">Объект потока данных.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-119">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d1cb-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d1cb-120">-Name</span></span>
<span data-ttu-id="2d1cb-121">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d1cb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d1cb-122">-PassThru</span></span>
<span data-ttu-id="2d1cb-123">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2d1cb-124">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2d1cb-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d1cb-125">-WorkspaceName</span></span>
<span data-ttu-id="2d1cb-126">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2d1cb-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2d1cb-127">-WorkspaceObject</span></span>
<span data-ttu-id="2d1cb-128">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2d1cb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d1cb-129">-Confirm</span></span>
<span data-ttu-id="2d1cb-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d1cb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d1cb-131">-WhatIf</span></span>
<span data-ttu-id="2d1cb-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d1cb-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d1cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d1cb-134">CommonParameters</span></span>
<span data-ttu-id="2d1cb-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d1cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d1cb-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d1cb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d1cb-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d1cb-137">INPUTS</span></span>

### <span data-ttu-id="2d1cb-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d1cb-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2d1cb-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="2d1cb-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="2d1cb-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d1cb-140">OUTPUTS</span></span>

### <span data-ttu-id="2d1cb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d1cb-141">System.Boolean</span></span>

## <span data-ttu-id="2d1cb-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d1cb-142">NOTES</span></span>

## <span data-ttu-id="2d1cb-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d1cb-143">RELATED LINKS</span></span>
