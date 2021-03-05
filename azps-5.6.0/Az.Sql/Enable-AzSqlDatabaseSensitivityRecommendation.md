---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e7e13e62407018559835f4703d0b94edeced930b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986373"
---
# <span data-ttu-id="3bb97-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3bb97-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="3bb97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bb97-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb97-103">Включает рекомендации по конфиденциальности для столбцов (они включены по умолчанию для всех столбцов) в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3bb97-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="3bb97-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3bb97-104">SYNTAX</span></span>

### <span data-ttu-id="3bb97-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3bb97-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb97-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bb97-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb97-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bb97-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bb97-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bb97-108">DESCRIPTION</span></span>
<span data-ttu-id="3bb97-109">Этот Enable-AzSqlDatabaseSensitivityRecommendation обеспечивает рекомендации по конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3bb97-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="3bb97-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3bb97-110">EXAMPLES</span></span>

### <span data-ttu-id="3bb97-111">Пример 1. Рекомендации по конфиденциальности для данного столбца в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3bb97-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="3bb97-112">Пример 2. В качестве рекомендации по конфиденциальности для столбца Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="3bb97-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="3bb97-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bb97-113">PARAMETERS</span></span>

### <span data-ttu-id="3bb97-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bb97-114">-AsJob</span></span>
<span data-ttu-id="3bb97-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3bb97-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3bb97-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3bb97-116">-ColumnName</span></span>
<span data-ttu-id="3bb97-117">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="3bb97-117">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb97-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3bb97-118">-DatabaseName</span></span>
<span data-ttu-id="3bb97-119">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3bb97-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="3bb97-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="3bb97-120">-DatabaseObject</span></span>
<span data-ttu-id="3bb97-121">Объект SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="3bb97-121">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb97-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb97-122">-DefaultProfile</span></span>
<span data-ttu-id="3bb97-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb97-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb97-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb97-124">-InputObject</span></span>
<span data-ttu-id="3bb97-125">Объект, представляющий SQL классификации конфиденциальности базы данных.</span><span class="sxs-lookup"><span data-stu-id="3bb97-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb97-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bb97-126">-PassThru</span></span>
<span data-ttu-id="3bb97-127">Указывает, нужно ли выводить модель классификации конфиденциальности в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb97-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="3bb97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb97-128">-ResourceGroupName</span></span>
<span data-ttu-id="3bb97-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3bb97-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3bb97-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3bb97-130">-SchemaName</span></span>
<span data-ttu-id="3bb97-131">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="3bb97-131">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb97-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3bb97-132">-ServerName</span></span>
<span data-ttu-id="3bb97-133">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3bb97-133">SQL server name.</span></span>

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

### <span data-ttu-id="3bb97-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="3bb97-134">-TableName</span></span>
<span data-ttu-id="3bb97-135">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="3bb97-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb97-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bb97-136">-Confirm</span></span>
<span data-ttu-id="3bb97-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb97-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb97-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb97-138">-WhatIf</span></span>
<span data-ttu-id="3bb97-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb97-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bb97-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3bb97-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb97-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb97-141">CommonParameters</span></span>
<span data-ttu-id="3bb97-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb97-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb97-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bb97-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb97-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bb97-144">INPUTS</span></span>

### <span data-ttu-id="3bb97-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="3bb97-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="3bb97-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3bb97-146">OUTPUTS</span></span>

### <span data-ttu-id="3bb97-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3bb97-147">System.Boolean</span></span>

## <span data-ttu-id="3bb97-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3bb97-148">NOTES</span></span>

## <span data-ttu-id="3bb97-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bb97-149">RELATED LINKS</span></span>

[<span data-ttu-id="3bb97-150">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="3bb97-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)