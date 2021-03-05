---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: a60bcb20610449b9f76ff3e62684da43a2a792c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959976"
---
# <span data-ttu-id="64e1a-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="64e1a-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="64e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="64e1a-103">Удаляет базу данных Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="64e1a-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="64e1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64e1a-104">SYNTAX</span></span>

### <span data-ttu-id="64e1a-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64e1a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64e1a-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64e1a-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64e1a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64e1a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64e1a-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64e1a-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64e1a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64e1a-109">DESCRIPTION</span></span>
<span data-ttu-id="64e1a-110">Cmdlet **Remove-AzSynapseSqlPool** окончательно удаляет базу данных Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="64e1a-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="64e1a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64e1a-111">EXAMPLES</span></span>

### <span data-ttu-id="64e1a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64e1a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="64e1a-113">Эта команда удаляет базу данных Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="64e1a-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="64e1a-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="64e1a-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="64e1a-115">Эта команда удаляет базу данных Azure Synapse Analytics SQL по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="64e1a-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="64e1a-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="64e1a-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="64e1a-117">Эта команда удаляет базу данных Azure Synapse Analytics SQL по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="64e1a-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="64e1a-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="64e1a-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="64e1a-119">Эта команда удаляет базу данных Azure Synapse Analytics SQL с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="64e1a-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="64e1a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64e1a-120">PARAMETERS</span></span>

### <span data-ttu-id="64e1a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64e1a-121">-AsJob</span></span>
<span data-ttu-id="64e1a-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="64e1a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64e1a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64e1a-123">-DefaultProfile</span></span>
<span data-ttu-id="64e1a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64e1a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64e1a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="64e1a-125">-Force</span></span>
<span data-ttu-id="64e1a-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="64e1a-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="64e1a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64e1a-127">-InputObject</span></span>
<span data-ttu-id="64e1a-128">SQL ввода базы данных обычно передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="64e1a-128">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="64e1a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="64e1a-129">-Name</span></span>
<span data-ttu-id="64e1a-130">Имя базы данных Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="64e1a-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="64e1a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64e1a-131">-PassThru</span></span>
<span data-ttu-id="64e1a-132">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64e1a-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="64e1a-133">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="64e1a-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="64e1a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64e1a-134">-ResourceGroupName</span></span>
<span data-ttu-id="64e1a-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64e1a-135">Resource group name.</span></span>

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

### <span data-ttu-id="64e1a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64e1a-136">-ResourceId</span></span>
<span data-ttu-id="64e1a-137">Идентификатор ресурса базы данных Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="64e1a-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="64e1a-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64e1a-138">-WorkspaceName</span></span>
<span data-ttu-id="64e1a-139">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="64e1a-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="64e1a-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="64e1a-140">-WorkspaceObject</span></span>
<span data-ttu-id="64e1a-141">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="64e1a-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="64e1a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64e1a-142">-Confirm</span></span>
<span data-ttu-id="64e1a-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64e1a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64e1a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64e1a-144">-WhatIf</span></span>
<span data-ttu-id="64e1a-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64e1a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64e1a-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="64e1a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64e1a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e1a-147">CommonParameters</span></span>
<span data-ttu-id="64e1a-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64e1a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e1a-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64e1a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e1a-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64e1a-150">INPUTS</span></span>

### <span data-ttu-id="64e1a-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="64e1a-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="64e1a-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="64e1a-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="64e1a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="64e1a-153">System.String</span></span>

## <span data-ttu-id="64e1a-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64e1a-154">OUTPUTS</span></span>

### <span data-ttu-id="64e1a-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64e1a-155">System.Boolean</span></span>

## <span data-ttu-id="64e1a-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64e1a-156">NOTES</span></span>

## <span data-ttu-id="64e1a-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64e1a-157">RELATED LINKS</span></span>
