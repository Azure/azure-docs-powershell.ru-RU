---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 2eec7ea6f89bea726cdbee483162ec455e5722aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992102"
---
# <span data-ttu-id="8a456-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="8a456-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="8a456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a456-102">SYNOPSIS</span></span>
<span data-ttu-id="8a456-103">Задает типы данных и метки конфиденциальности столбцов в SQL столбцов.</span><span class="sxs-lookup"><span data-stu-id="8a456-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="8a456-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a456-104">SYNTAX</span></span>

### <span data-ttu-id="8a456-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a456-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a456-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a456-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a456-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a456-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a456-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a456-108">DESCRIPTION</span></span>
<span data-ttu-id="8a456-109">Этот Set-AzSynapseSqlPoolSensitivityClassification задает типы информации и метки конфиденциальности столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="8a456-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="8a456-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a456-110">EXAMPLES</span></span>

### <span data-ttu-id="8a456-111">Пример 1. Настройка типа информации и метки конфиденциальности столбца в пуле Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="8a456-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="8a456-112">Пример 2. Настройка рекомендуемых типов данных и меток конфиденциальности для столбцов в SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a456-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="8a456-113">Пример 3. Настройка типа информации и метки конфиденциальности столбца в SQL Azure Synapse с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="8a456-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="8a456-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a456-114">PARAMETERS</span></span>

### <span data-ttu-id="8a456-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a456-115">-AsJob</span></span>
<span data-ttu-id="8a456-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8a456-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a456-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="8a456-117">-ClassificationObject</span></span>
<span data-ttu-id="8a456-118">Объект, представляющий классификацию SQL пула.</span><span class="sxs-lookup"><span data-stu-id="8a456-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="8a456-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8a456-119">-ColumnName</span></span>
<span data-ttu-id="8a456-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="8a456-120">Name of column.</span></span>

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

### <span data-ttu-id="8a456-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a456-121">-DefaultProfile</span></span>
<span data-ttu-id="8a456-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a456-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a456-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="8a456-123">-InformationType</span></span>
<span data-ttu-id="8a456-124">Имя, описыва которое описывает тип данных, хранимых в столбце.</span><span class="sxs-lookup"><span data-stu-id="8a456-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a456-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a456-125">-PassThru</span></span>
<span data-ttu-id="8a456-126">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a456-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8a456-127">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="8a456-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8a456-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a456-128">-ResourceGroupName</span></span>
<span data-ttu-id="8a456-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a456-129">Resource group name.</span></span>

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

### <span data-ttu-id="8a456-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8a456-130">-SchemaName</span></span>
<span data-ttu-id="8a456-131">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="8a456-131">Name of schema.</span></span>

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

### <span data-ttu-id="8a456-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="8a456-132">-SensitivityLabel</span></span>
<span data-ttu-id="8a456-133">Имя, которое описывает конфиденциальность данных в столбце.</span><span class="sxs-lookup"><span data-stu-id="8a456-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a456-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="8a456-134">-SqlPoolName</span></span>
<span data-ttu-id="8a456-135">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a456-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="8a456-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="8a456-136">-SqlPoolObject</span></span>
<span data-ttu-id="8a456-137">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="8a456-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8a456-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="8a456-138">-TableName</span></span>
<span data-ttu-id="8a456-139">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="8a456-139">Name of table.</span></span>

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

### <span data-ttu-id="8a456-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8a456-140">-WorkspaceName</span></span>
<span data-ttu-id="8a456-141">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a456-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8a456-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a456-142">-Confirm</span></span>
<span data-ttu-id="8a456-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a456-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a456-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a456-144">-WhatIf</span></span>
<span data-ttu-id="8a456-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a456-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a456-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8a456-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a456-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a456-147">CommonParameters</span></span>
<span data-ttu-id="8a456-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a456-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a456-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a456-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a456-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a456-150">INPUTS</span></span>

### <span data-ttu-id="8a456-151">System.String</span><span class="sxs-lookup"><span data-stu-id="8a456-151">System.String</span></span>

### <span data-ttu-id="8a456-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="8a456-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="8a456-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8a456-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8a456-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a456-154">OUTPUTS</span></span>

### <span data-ttu-id="8a456-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a456-155">System.Boolean</span></span>

## <span data-ttu-id="8a456-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a456-156">NOTES</span></span>

## <span data-ttu-id="8a456-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a456-157">RELATED LINKS</span></span>
