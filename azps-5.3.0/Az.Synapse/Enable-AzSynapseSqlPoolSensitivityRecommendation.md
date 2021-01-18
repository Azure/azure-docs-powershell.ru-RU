---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 52abddf2db18a6e70a1b876629feff0761bed014
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505578"
---
# <span data-ttu-id="a2fe5-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="a2fe5-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="a2fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fe5-103">Включает рекомендации по конфиденциальности для столбцов (они включены по умолчанию для всех столбцов) в SQL столбцах.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="a2fe5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2fe5-104">SYNTAX</span></span>

### <span data-ttu-id="a2fe5-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2fe5-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2fe5-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2fe5-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2fe5-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2fe5-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2fe5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2fe5-108">DESCRIPTION</span></span>
<span data-ttu-id="a2fe5-109">Этот Enable-AzSynapseSqlPoolSensitivityRecommendation позволяет использовать рекомендации по конфиденциальности для столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="a2fe5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2fe5-110">EXAMPLES</span></span>

### <span data-ttu-id="a2fe5-111">Пример 1. Включить рекомендации по конфиденциальности для данного столбца в SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="a2fe5-112">Пример 2. В качестве рекомендации по конфиденциальности для столбца Azure Synapse SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="a2fe5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2fe5-113">PARAMETERS</span></span>

### <span data-ttu-id="a2fe5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2fe5-114">-AsJob</span></span>
<span data-ttu-id="a2fe5-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a2fe5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2fe5-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a2fe5-116">-ColumnName</span></span>
<span data-ttu-id="a2fe5-117">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-117">Name of column.</span></span>

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

### <span data-ttu-id="a2fe5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2fe5-118">-DefaultProfile</span></span>
<span data-ttu-id="a2fe5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2fe5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2fe5-120">-InputObject</span></span>
<span data-ttu-id="a2fe5-121">Объект, представляющий классификацию SQL пула.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2fe5-122">-PassThru</span></span>
<span data-ttu-id="a2fe5-123">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a2fe5-124">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a2fe5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2fe5-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2fe5-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-126">Resource group name.</span></span>

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

### <span data-ttu-id="a2fe5-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a2fe5-127">-SchemaName</span></span>
<span data-ttu-id="a2fe5-128">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-128">Name of schema.</span></span>

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

### <span data-ttu-id="a2fe5-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="a2fe5-129">-SqlPoolName</span></span>
<span data-ttu-id="a2fe5-130">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a2fe5-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="a2fe5-131">-SqlPoolObject</span></span>
<span data-ttu-id="a2fe5-132">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-132">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a2fe5-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="a2fe5-133">-TableName</span></span>
<span data-ttu-id="a2fe5-134">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-134">Name of table.</span></span>

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

### <span data-ttu-id="a2fe5-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2fe5-135">-WorkspaceName</span></span>
<span data-ttu-id="a2fe5-136">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2fe5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2fe5-137">-Confirm</span></span>
<span data-ttu-id="a2fe5-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2fe5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2fe5-139">-WhatIf</span></span>
<span data-ttu-id="a2fe5-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2fe5-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2fe5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fe5-142">CommonParameters</span></span>
<span data-ttu-id="a2fe5-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2fe5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fe5-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2fe5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fe5-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2fe5-145">INPUTS</span></span>

### <span data-ttu-id="a2fe5-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="a2fe5-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="a2fe5-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a2fe5-147">System.String</span></span>

### <span data-ttu-id="a2fe5-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a2fe5-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a2fe5-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2fe5-149">OUTPUTS</span></span>

### <span data-ttu-id="a2fe5-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2fe5-150">System.Boolean</span></span>

## <span data-ttu-id="a2fe5-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2fe5-151">NOTES</span></span>

## <span data-ttu-id="a2fe5-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2fe5-152">RELATED LINKS</span></span>
