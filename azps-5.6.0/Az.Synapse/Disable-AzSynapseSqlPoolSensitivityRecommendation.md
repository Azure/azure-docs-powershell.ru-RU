---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: a9085433bb888fa8e37405881a20a55a4f08b96d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961107"
---
# <span data-ttu-id="bdcec-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="bdcec-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="bdcec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdcec-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcec-103">Отключает (отключает) рекомендации по конфиденциальности для столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="bdcec-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="bdcec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bdcec-104">SYNTAX</span></span>

### <span data-ttu-id="bdcec-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bdcec-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdcec-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdcec-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdcec-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdcec-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdcec-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdcec-108">DESCRIPTION</span></span>
<span data-ttu-id="bdcec-109">Этот Disable-AzSynapseSqlPoolSensitivityRecommendation отключает (отключает) рекомендации по конфиденциальности для столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="bdcec-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="bdcec-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bdcec-110">EXAMPLES</span></span>

### <span data-ttu-id="bdcec-111">Пример 1. Отключать рекомендации по конфиденциальности для данного столбца в SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="bdcec-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="bdcec-112">Пример 2. Отключать рекомендации по конфиденциальности для столбцов, которые имеют рекомендации по конфиденциальности в пуле Azure Synapse SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="bdcec-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="bdcec-113">Пример 3. Отключать рекомендации по конфиденциальности для данного столбца в пуле Azure Synapse SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="bdcec-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="bdcec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdcec-114">PARAMETERS</span></span>

### <span data-ttu-id="bdcec-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdcec-115">-AsJob</span></span>
<span data-ttu-id="bdcec-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bdcec-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdcec-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="bdcec-117">-ColumnName</span></span>
<span data-ttu-id="bdcec-118">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="bdcec-118">Name of column.</span></span>

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

### <span data-ttu-id="bdcec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcec-119">-DefaultProfile</span></span>
<span data-ttu-id="bdcec-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdcec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdcec-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdcec-121">-InputObject</span></span>
<span data-ttu-id="bdcec-122">Объект, представляющий классификацию SQL пула.</span><span class="sxs-lookup"><span data-stu-id="bdcec-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="bdcec-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdcec-123">-PassThru</span></span>
<span data-ttu-id="bdcec-124">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bdcec-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bdcec-125">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="bdcec-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bdcec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdcec-126">-ResourceGroupName</span></span>
<span data-ttu-id="bdcec-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bdcec-127">Resource group name.</span></span>

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

### <span data-ttu-id="bdcec-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="bdcec-128">-SchemaName</span></span>
<span data-ttu-id="bdcec-129">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="bdcec-129">Name of schema.</span></span>

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

### <span data-ttu-id="bdcec-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="bdcec-130">-SqlPoolName</span></span>
<span data-ttu-id="bdcec-131">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="bdcec-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="bdcec-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="bdcec-132">-SqlPoolObject</span></span>
<span data-ttu-id="bdcec-133">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="bdcec-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bdcec-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="bdcec-134">-TableName</span></span>
<span data-ttu-id="bdcec-135">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="bdcec-135">Name of table.</span></span>

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

### <span data-ttu-id="bdcec-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bdcec-136">-WorkspaceName</span></span>
<span data-ttu-id="bdcec-137">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="bdcec-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bdcec-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdcec-138">-Confirm</span></span>
<span data-ttu-id="bdcec-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdcec-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdcec-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdcec-140">-WhatIf</span></span>
<span data-ttu-id="bdcec-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdcec-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdcec-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bdcec-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdcec-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcec-143">CommonParameters</span></span>
<span data-ttu-id="bdcec-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdcec-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcec-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdcec-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcec-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdcec-146">INPUTS</span></span>

### <span data-ttu-id="bdcec-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="bdcec-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="bdcec-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bdcec-148">System.String</span></span>

### <span data-ttu-id="bdcec-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bdcec-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bdcec-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bdcec-150">OUTPUTS</span></span>

### <span data-ttu-id="bdcec-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdcec-151">System.Boolean</span></span>

## <span data-ttu-id="bdcec-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bdcec-152">NOTES</span></span>

## <span data-ttu-id="bdcec-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdcec-153">RELATED LINKS</span></span>
