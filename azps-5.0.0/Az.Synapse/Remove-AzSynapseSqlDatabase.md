---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247136"
---
# <span data-ttu-id="f4c89-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f4c89-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="f4c89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4c89-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c89-103">Удаляет базу данных SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="f4c89-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f4c89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4c89-104">SYNTAX</span></span>

### <span data-ttu-id="f4c89-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4c89-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c89-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4c89-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c89-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4c89-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c89-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4c89-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c89-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4c89-109">DESCRIPTION</span></span>
<span data-ttu-id="f4c89-110">Командлет **Remove-AzSynapseSqlPool** окончательно удаляет базу данных SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f4c89-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="f4c89-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4c89-111">EXAMPLES</span></span>

### <span data-ttu-id="f4c89-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4c89-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="f4c89-113">Эта команда удаляет базу данных SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f4c89-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="f4c89-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f4c89-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="f4c89-115">Эта команда удаляет базу данных SQL Azure Synapse Analytics с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="f4c89-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="f4c89-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f4c89-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="f4c89-117">Эта команда удаляет базу данных SQL Azure Synapse Analytics с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="f4c89-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="f4c89-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="f4c89-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="f4c89-119">Эта команда удаляет базу данных SQL Azure Synapse Analytics с указанным ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="f4c89-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="f4c89-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4c89-120">PARAMETERS</span></span>

### <span data-ttu-id="f4c89-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4c89-121">-AsJob</span></span>
<span data-ttu-id="f4c89-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f4c89-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4c89-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c89-123">-DefaultProfile</span></span>
<span data-ttu-id="f4c89-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4c89-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4c89-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4c89-125">-InputObject</span></span>
<span data-ttu-id="f4c89-126">Объект ввода базы данных SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f4c89-126">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c89-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4c89-127">-Name</span></span>
<span data-ttu-id="f4c89-128">Имя базы данных SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f4c89-128">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c89-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4c89-129">-PassThru</span></span>
<span data-ttu-id="f4c89-130">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4c89-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f4c89-131">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="f4c89-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f4c89-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c89-132">-ResourceGroupName</span></span>
<span data-ttu-id="f4c89-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4c89-133">Resource group name.</span></span>

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

### <span data-ttu-id="f4c89-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4c89-134">-ResourceId</span></span>
<span data-ttu-id="f4c89-135">Идентификатор ресурса Synapse базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f4c89-135">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c89-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f4c89-136">-WorkspaceName</span></span>
<span data-ttu-id="f4c89-137">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f4c89-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c89-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f4c89-138">-WorkspaceObject</span></span>
<span data-ttu-id="f4c89-139">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f4c89-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c89-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4c89-140">-Confirm</span></span>
<span data-ttu-id="f4c89-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4c89-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c89-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c89-142">-WhatIf</span></span>
<span data-ttu-id="f4c89-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4c89-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4c89-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4c89-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c89-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c89-145">CommonParameters</span></span>
<span data-ttu-id="f4c89-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4c89-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c89-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4c89-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c89-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4c89-148">INPUTS</span></span>

### <span data-ttu-id="f4c89-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f4c89-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f4c89-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f4c89-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="f4c89-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f4c89-151">System.String</span></span>

## <span data-ttu-id="f4c89-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4c89-152">OUTPUTS</span></span>

### <span data-ttu-id="f4c89-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4c89-153">System.Boolean</span></span>

## <span data-ttu-id="f4c89-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4c89-154">NOTES</span></span>

## <span data-ttu-id="f4c89-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4c89-155">RELATED LINKS</span></span>
