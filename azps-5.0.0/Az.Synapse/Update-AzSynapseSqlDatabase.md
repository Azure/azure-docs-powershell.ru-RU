---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246159"
---
# <span data-ttu-id="d2c46-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d2c46-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="d2c46-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2c46-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c46-103">Обновляет базу данных SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="d2c46-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d2c46-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2c46-104">SYNTAX</span></span>

### <span data-ttu-id="d2c46-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2c46-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2c46-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2c46-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2c46-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2c46-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2c46-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2c46-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c46-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2c46-109">DESCRIPTION</span></span>
<span data-ttu-id="d2c46-110">Командлет **Update-AzSynapseSqlDatabase** обновляет базу данных SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d2c46-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d2c46-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2c46-111">EXAMPLES</span></span>

### <span data-ttu-id="d2c46-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2c46-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="d2c46-113">Эта команда обновляет базу данных SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d2c46-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d2c46-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2c46-114">PARAMETERS</span></span>

### <span data-ttu-id="d2c46-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2c46-115">-AsJob</span></span>
<span data-ttu-id="d2c46-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d2c46-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2c46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c46-117">-DefaultProfile</span></span>
<span data-ttu-id="d2c46-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c46-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2c46-119">-InputObject</span></span>
<span data-ttu-id="d2c46-120">Объект ввода базы данных SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="d2c46-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d2c46-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="d2c46-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="d2c46-122">Указывает максимальный размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="d2c46-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="d2c46-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2c46-123">-Name</span></span>
<span data-ttu-id="d2c46-124">Имя базы данных SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d2c46-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="d2c46-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2c46-125">-PassThru</span></span>
<span data-ttu-id="d2c46-126">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2c46-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d2c46-127">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="d2c46-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d2c46-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c46-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2c46-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2c46-129">Resource group name.</span></span>

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

### <span data-ttu-id="d2c46-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2c46-130">-ResourceId</span></span>
<span data-ttu-id="d2c46-131">Идентификатор ресурса Synapse базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d2c46-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="d2c46-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="d2c46-132">-Tag</span></span>
<span data-ttu-id="d2c46-133">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="d2c46-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="d2c46-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2c46-134">-WorkspaceName</span></span>
<span data-ttu-id="d2c46-135">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d2c46-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d2c46-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d2c46-136">-WorkspaceObject</span></span>
<span data-ttu-id="d2c46-137">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="d2c46-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d2c46-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2c46-138">-Confirm</span></span>
<span data-ttu-id="d2c46-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2c46-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c46-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c46-140">-WhatIf</span></span>
<span data-ttu-id="d2c46-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2c46-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c46-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2c46-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c46-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c46-143">CommonParameters</span></span>
<span data-ttu-id="d2c46-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2c46-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c46-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2c46-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c46-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2c46-146">INPUTS</span></span>

### <span data-ttu-id="d2c46-147">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2c46-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d2c46-148">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d2c46-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="d2c46-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2c46-149">OUTPUTS</span></span>

### <span data-ttu-id="d2c46-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d2c46-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="d2c46-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2c46-151">NOTES</span></span>

## <span data-ttu-id="d2c46-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2c46-152">RELATED LINKS</span></span>
