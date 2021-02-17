---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216716"
---
# <span data-ttu-id="ce4c0-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce4c0-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="ce4c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4c0-103">Обновляет базу данных Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ce4c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ce4c0-104">SYNTAX</span></span>

### <span data-ttu-id="ce4c0-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce4c0-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce4c0-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce4c0-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce4c0-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce4c0-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce4c0-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce4c0-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce4c0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce4c0-109">DESCRIPTION</span></span>
<span data-ttu-id="ce4c0-110">С **его** SQL azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ce4c0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ce4c0-111">EXAMPLES</span></span>

### <span data-ttu-id="ce4c0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce4c0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="ce4c0-113">Эта команда обновляет базу данных Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ce4c0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce4c0-114">PARAMETERS</span></span>

### <span data-ttu-id="ce4c0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce4c0-115">-AsJob</span></span>
<span data-ttu-id="ce4c0-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ce4c0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce4c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4c0-117">-DefaultProfile</span></span>
<span data-ttu-id="ce4c0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce4c0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce4c0-119">-InputObject</span></span>
<span data-ttu-id="ce4c0-120">SQL ввода базы данных обычно передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c0-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="ce4c0-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="ce4c0-122">Максимальный размер базы данных в этихбайтах.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ce4c0-123">-Name</span></span>
<span data-ttu-id="ce4c0-124">Имя базы данных Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce4c0-125">-PassThru</span></span>
<span data-ttu-id="ce4c0-126">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ce4c0-127">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ce4c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce4c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="ce4c0-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce4c0-130">-ResourceId</span></span>
<span data-ttu-id="ce4c0-131">Идентификатор ресурса базы данных Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-131">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c0-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce4c0-132">-Tag</span></span>
<span data-ttu-id="ce4c0-133">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c0-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce4c0-134">-WorkspaceName</span></span>
<span data-ttu-id="ce4c0-135">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-135">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c0-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ce4c0-136">-WorkspaceObject</span></span>
<span data-ttu-id="ce4c0-137">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-137">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce4c0-138">-Confirm</span></span>
<span data-ttu-id="ce4c0-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce4c0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce4c0-140">-WhatIf</span></span>
<span data-ttu-id="ce4c0-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce4c0-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce4c0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4c0-143">CommonParameters</span></span>
<span data-ttu-id="ce4c0-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce4c0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4c0-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce4c0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4c0-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce4c0-146">INPUTS</span></span>

### <span data-ttu-id="ce4c0-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce4c0-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ce4c0-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce4c0-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="ce4c0-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ce4c0-149">OUTPUTS</span></span>

### <span data-ttu-id="ce4c0-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce4c0-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="ce4c0-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ce4c0-151">NOTES</span></span>

## <span data-ttu-id="ce4c0-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce4c0-152">RELATED LINKS</span></span>
