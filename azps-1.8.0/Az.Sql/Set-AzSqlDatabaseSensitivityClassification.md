---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 3b3bc7b98bd4325eda075e24220f88c6e5874aaf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728787"
---
# <span data-ttu-id="d4497-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="d4497-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="d4497-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4497-102">SYNOPSIS</span></span>
<span data-ttu-id="d4497-103">Задает типы данных и метки чувствительности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d4497-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="d4497-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4497-104">SYNTAX</span></span>

### <span data-ttu-id="d4497-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4497-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4497-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4497-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4497-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4497-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4497-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4497-108">DESCRIPTION</span></span>
<span data-ttu-id="d4497-109">Командлет Set-AzSqlDatabaseSensitivityClassification задает типы данных и метки чувствительности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d4497-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="d4497-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4497-110">EXAMPLES</span></span>

### <span data-ttu-id="d4497-111">Пример 1: Настройка типа сведений и метки чувствительности для столбца в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d4497-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="d4497-112">Пример 2: Настройка рекомендуемых типов данных и меток чувствительности для столбцов в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d4497-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="d4497-113">Пример 3: Настройка типа данных и метки чувствительности столбца в базе данных SQL Azure с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="d4497-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="d4497-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4497-114">PARAMETERS</span></span>

### <span data-ttu-id="d4497-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4497-115">-AsJob</span></span>
<span data-ttu-id="d4497-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d4497-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4497-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="d4497-117">-ClassificationObject</span></span>
<span data-ttu-id="d4497-118">Объект, представляющий классификацию чувствительности базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d4497-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4497-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="d4497-119">-ColumnName</span></span>
<span data-ttu-id="d4497-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="d4497-120">Name of column.</span></span>

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

### <span data-ttu-id="d4497-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4497-121">-DatabaseName</span></span>
<span data-ttu-id="d4497-122">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d4497-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="d4497-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d4497-123">-DatabaseObject</span></span>
<span data-ttu-id="d4497-124">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d4497-124">The SQL database object.</span></span>

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

### <span data-ttu-id="d4497-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4497-125">-DefaultProfile</span></span>
<span data-ttu-id="d4497-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4497-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4497-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="d4497-127">-InformationType</span></span>
<span data-ttu-id="d4497-128">Имя, описывающее тип данных, хранящихся в столбце.</span><span class="sxs-lookup"><span data-stu-id="d4497-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4497-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4497-129">-PassThru</span></span>
<span data-ttu-id="d4497-130">Указывает, следует ли выводить модель классификации чувствительности при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="d4497-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="d4497-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4497-131">-ResourceGroupName</span></span>
<span data-ttu-id="d4497-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4497-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4497-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d4497-133">-SchemaName</span></span>
<span data-ttu-id="d4497-134">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="d4497-134">Name of schema.</span></span>

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

### <span data-ttu-id="d4497-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="d4497-135">-SensitivityLabel</span></span>
<span data-ttu-id="d4497-136">Имя, которое описывает чувствительность данных, хранящихся в столбце.</span><span class="sxs-lookup"><span data-stu-id="d4497-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4497-137">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d4497-137">-ServerName</span></span>
<span data-ttu-id="d4497-138">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d4497-138">SQL server name.</span></span>

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

### <span data-ttu-id="d4497-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="d4497-139">-TableName</span></span>
<span data-ttu-id="d4497-140">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4497-140">Name of table.</span></span>

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

### <span data-ttu-id="d4497-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4497-141">-Confirm</span></span>
<span data-ttu-id="d4497-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4497-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4497-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4497-143">-WhatIf</span></span>
<span data-ttu-id="d4497-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4497-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4497-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4497-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4497-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4497-146">CommonParameters</span></span>
<span data-ttu-id="d4497-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4497-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4497-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4497-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4497-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4497-149">INPUTS</span></span>

### <span data-ttu-id="d4497-150">Microsoft. Azure. Commands. SQL. Classification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="d4497-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="d4497-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4497-151">OUTPUTS</span></span>

### <span data-ttu-id="d4497-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4497-152">System.Boolean</span></span>

## <span data-ttu-id="d4497-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4497-153">NOTES</span></span>

## <span data-ttu-id="d4497-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4497-154">RELATED LINKS</span></span>

[<span data-ttu-id="d4497-155">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="d4497-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
