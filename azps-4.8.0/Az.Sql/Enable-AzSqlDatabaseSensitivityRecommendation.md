---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235842"
---
# <span data-ttu-id="0159a-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="0159a-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="0159a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0159a-102">SYNOPSIS</span></span>
<span data-ttu-id="0159a-103">Включает рекомендации по пометкам для столбцов (рекомендации включены по умолчанию во всех столбцах) в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0159a-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="0159a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0159a-104">SYNTAX</span></span>

### <span data-ttu-id="0159a-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0159a-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0159a-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0159a-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0159a-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0159a-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0159a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0159a-108">DESCRIPTION</span></span>
<span data-ttu-id="0159a-109">Командлет Enable-AzSqlDatabaseSensitivityRecommendation включает рекомендации по отметкам для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0159a-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="0159a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0159a-110">EXAMPLES</span></span>

### <span data-ttu-id="0159a-111">Пример 1: включение рекомендаций по чувствительности для определенного столбца в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0159a-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="0159a-112">Пример 2: Включите рекомендации по чувствительности для заданной гистограммы базы данных Azure SQL с использованием конвейера.</span><span class="sxs-lookup"><span data-stu-id="0159a-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="0159a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0159a-113">PARAMETERS</span></span>

### <span data-ttu-id="0159a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0159a-114">-AsJob</span></span>
<span data-ttu-id="0159a-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0159a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0159a-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0159a-116">-ColumnName</span></span>
<span data-ttu-id="0159a-117">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="0159a-117">Name of column.</span></span>

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

### <span data-ttu-id="0159a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0159a-118">-DatabaseName</span></span>
<span data-ttu-id="0159a-119">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0159a-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="0159a-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0159a-120">-DatabaseObject</span></span>
<span data-ttu-id="0159a-121">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0159a-121">The SQL database object.</span></span>

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

### <span data-ttu-id="0159a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0159a-122">-DefaultProfile</span></span>
<span data-ttu-id="0159a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0159a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0159a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0159a-124">-InputObject</span></span>
<span data-ttu-id="0159a-125">Объект, представляющий классификацию чувствительности базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0159a-125">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="0159a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0159a-126">-PassThru</span></span>
<span data-ttu-id="0159a-127">Указывает, следует ли выводить модель классификации чувствительности при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="0159a-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="0159a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0159a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0159a-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0159a-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="0159a-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0159a-130">-SchemaName</span></span>
<span data-ttu-id="0159a-131">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="0159a-131">Name of schema.</span></span>

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

### <span data-ttu-id="0159a-132">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0159a-132">-ServerName</span></span>
<span data-ttu-id="0159a-133">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0159a-133">SQL server name.</span></span>

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

### <span data-ttu-id="0159a-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="0159a-134">-TableName</span></span>
<span data-ttu-id="0159a-135">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="0159a-135">Name of table.</span></span>

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

### <span data-ttu-id="0159a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0159a-136">-Confirm</span></span>
<span data-ttu-id="0159a-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0159a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0159a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0159a-138">-WhatIf</span></span>
<span data-ttu-id="0159a-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0159a-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0159a-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0159a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0159a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0159a-141">CommonParameters</span></span>
<span data-ttu-id="0159a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0159a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0159a-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0159a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0159a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0159a-144">INPUTS</span></span>

### <span data-ttu-id="0159a-145">Microsoft. Azure. Commands. SQL. Classification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="0159a-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="0159a-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0159a-146">OUTPUTS</span></span>

### <span data-ttu-id="0159a-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0159a-147">System.Boolean</span></span>

## <span data-ttu-id="0159a-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="0159a-148">NOTES</span></span>

## <span data-ttu-id="0159a-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0159a-149">RELATED LINKS</span></span>

[<span data-ttu-id="0159a-150">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="0159a-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)