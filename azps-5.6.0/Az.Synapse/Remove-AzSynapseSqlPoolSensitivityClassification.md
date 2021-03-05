---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 58ef691f5f109f301ffae2636d739405000754ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959971"
---
# <span data-ttu-id="7316f-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="7316f-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="7316f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7316f-102">SYNOPSIS</span></span>
<span data-ttu-id="7316f-103">Удаляет типы данных и метки конфиденциальности столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="7316f-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="7316f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7316f-104">SYNTAX</span></span>

### <span data-ttu-id="7316f-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7316f-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7316f-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7316f-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7316f-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7316f-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7316f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7316f-108">DESCRIPTION</span></span>
<span data-ttu-id="7316f-109">Этот Remove-AzSynapseSqlPoolSensitivityClassification удаляет типы информации и метки конфиденциальности столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="7316f-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="7316f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7316f-110">EXAMPLES</span></span>

### <span data-ttu-id="7316f-111">Пример 1. Удаление метки типа данных и конфиденциальности столбца в SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="7316f-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7316f-112">Пример 2. Удаление текущих типов данных и меток конфиденциальности столбцов в пуле Azure Synapse SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="7316f-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="7316f-113">Пример 3. Удаление типа информации и метки конфиденциальности столбца в пуле Azure Synapse SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="7316f-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7316f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7316f-114">PARAMETERS</span></span>

### <span data-ttu-id="7316f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7316f-115">-AsJob</span></span>
<span data-ttu-id="7316f-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7316f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7316f-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="7316f-117">-ClassificationObject</span></span>
<span data-ttu-id="7316f-118">Объект, представляющий классификацию SQL пула.</span><span class="sxs-lookup"><span data-stu-id="7316f-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7316f-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7316f-119">-ColumnName</span></span>
<span data-ttu-id="7316f-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="7316f-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7316f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7316f-121">-DefaultProfile</span></span>
<span data-ttu-id="7316f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7316f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7316f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7316f-123">-PassThru</span></span>
<span data-ttu-id="7316f-124">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7316f-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7316f-125">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="7316f-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7316f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7316f-126">-ResourceGroupName</span></span>
<span data-ttu-id="7316f-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7316f-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7316f-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7316f-128">-SchemaName</span></span>
<span data-ttu-id="7316f-129">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="7316f-129">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7316f-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="7316f-130">-SqlPoolName</span></span>
<span data-ttu-id="7316f-131">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7316f-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7316f-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7316f-132">-SqlPoolObject</span></span>
<span data-ttu-id="7316f-133">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="7316f-133">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7316f-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="7316f-134">-TableName</span></span>
<span data-ttu-id="7316f-135">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="7316f-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7316f-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7316f-136">-WorkspaceName</span></span>
<span data-ttu-id="7316f-137">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="7316f-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7316f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7316f-138">-Confirm</span></span>
<span data-ttu-id="7316f-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7316f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7316f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7316f-140">-WhatIf</span></span>
<span data-ttu-id="7316f-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7316f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7316f-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7316f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7316f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7316f-143">CommonParameters</span></span>
<span data-ttu-id="7316f-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7316f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7316f-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7316f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7316f-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7316f-146">INPUTS</span></span>

### <span data-ttu-id="7316f-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7316f-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="7316f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7316f-148">System.String</span></span>

### <span data-ttu-id="7316f-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7316f-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7316f-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7316f-150">OUTPUTS</span></span>

### <span data-ttu-id="7316f-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7316f-151">System.Boolean</span></span>

## <span data-ttu-id="7316f-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7316f-152">NOTES</span></span>

## <span data-ttu-id="7316f-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7316f-153">RELATED LINKS</span></span>
