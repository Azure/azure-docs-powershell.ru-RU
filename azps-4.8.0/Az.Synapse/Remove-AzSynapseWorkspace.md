---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: dcc73c78334fba9823ddc1d26463422bcc388bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243463"
---
# <span data-ttu-id="ca180-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ca180-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="ca180-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca180-102">SYNOPSIS</span></span>
<span data-ttu-id="ca180-103">Удаляет рабочую область Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ca180-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="ca180-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca180-104">SYNTAX</span></span>

### <span data-ttu-id="ca180-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca180-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca180-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca180-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca180-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca180-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca180-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca180-108">DESCRIPTION</span></span>
<span data-ttu-id="ca180-109">Командлет **Remove-AzSynapseWorkspace** окончательно удаляет рабочую область Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ca180-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="ca180-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca180-110">EXAMPLES</span></span>

### <span data-ttu-id="ca180-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca180-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="ca180-112">Эта команда удаляет рабочую область Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ca180-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="ca180-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ca180-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="ca180-114">Эта команда удаляет рабочую область Azure Synapse Analytics с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="ca180-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="ca180-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ca180-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="ca180-116">Эта команда удаляет рабочую область Azure Synapse Analytics через конвейер с указанным ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="ca180-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="ca180-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca180-117">PARAMETERS</span></span>

### <span data-ttu-id="ca180-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca180-118">-AsJob</span></span>
<span data-ttu-id="ca180-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ca180-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca180-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca180-120">-DefaultProfile</span></span>
<span data-ttu-id="ca180-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca180-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca180-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca180-122">-InputObject</span></span>
<span data-ttu-id="ca180-123">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ca180-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca180-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca180-124">-Name</span></span>
<span data-ttu-id="ca180-125">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ca180-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca180-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca180-126">-PassThru</span></span>
<span data-ttu-id="ca180-127">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ca180-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ca180-128">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="ca180-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ca180-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca180-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca180-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca180-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca180-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca180-131">-ResourceId</span></span>
<span data-ttu-id="ca180-132">Идентификатор ресурса Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ca180-132">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca180-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca180-133">-Confirm</span></span>
<span data-ttu-id="ca180-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca180-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca180-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca180-135">-WhatIf</span></span>
<span data-ttu-id="ca180-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca180-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca180-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca180-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca180-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca180-138">CommonParameters</span></span>
<span data-ttu-id="ca180-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca180-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca180-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca180-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca180-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca180-141">INPUTS</span></span>

### <span data-ttu-id="ca180-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ca180-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ca180-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca180-143">OUTPUTS</span></span>

### <span data-ttu-id="ca180-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca180-144">System.Boolean</span></span>

## <span data-ttu-id="ca180-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca180-145">NOTES</span></span>

## <span data-ttu-id="ca180-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca180-146">RELATED LINKS</span></span>