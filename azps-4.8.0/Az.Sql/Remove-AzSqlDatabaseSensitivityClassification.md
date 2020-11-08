---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235789"
---
# <span data-ttu-id="0ad16-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="0ad16-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="0ad16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ad16-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad16-103">Удаляет типы данных и метки чувствительности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0ad16-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="0ad16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ad16-104">SYNTAX</span></span>

### <span data-ttu-id="0ad16-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ad16-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad16-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ad16-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad16-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ad16-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad16-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad16-108">DESCRIPTION</span></span>
<span data-ttu-id="0ad16-109">Командлет Remove-AzSqlDatabaseSensitivityClassification удаляет типы данных и метки чувствительности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0ad16-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="0ad16-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ad16-110">EXAMPLES</span></span>

### <span data-ttu-id="0ad16-111">Пример 1: Удаление типа данных и метки чувствительности для столбца в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0ad16-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="0ad16-112">Пример 2: Удаление текущих типов данных и меток секретности столбцов в базе данных Azure SQL с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="0ad16-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="0ad16-113">Пример 3: Удаление типа данных и метки чувствительности столбца в базе данных Azure SQL с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="0ad16-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="0ad16-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ad16-114">PARAMETERS</span></span>

### <span data-ttu-id="0ad16-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ad16-115">-AsJob</span></span>
<span data-ttu-id="0ad16-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0ad16-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ad16-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="0ad16-117">-ClassificationObject</span></span>
<span data-ttu-id="0ad16-118">Объект, представляющий классификацию чувствительности базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0ad16-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="0ad16-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0ad16-119">-ColumnName</span></span>
<span data-ttu-id="0ad16-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="0ad16-120">Name of column.</span></span>

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

### <span data-ttu-id="0ad16-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0ad16-121">-DatabaseName</span></span>
<span data-ttu-id="0ad16-122">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad16-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="0ad16-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0ad16-123">-DatabaseObject</span></span>
<span data-ttu-id="0ad16-124">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0ad16-124">The SQL database object.</span></span>

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

### <span data-ttu-id="0ad16-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad16-125">-DefaultProfile</span></span>
<span data-ttu-id="0ad16-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad16-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ad16-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ad16-127">-PassThru</span></span>
<span data-ttu-id="0ad16-128">Указывает, следует ли выводить модель классификации чувствительности при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="0ad16-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="0ad16-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad16-129">-ResourceGroupName</span></span>
<span data-ttu-id="0ad16-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ad16-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="0ad16-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0ad16-131">-SchemaName</span></span>
<span data-ttu-id="0ad16-132">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="0ad16-132">Name of schema.</span></span>

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

### <span data-ttu-id="0ad16-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0ad16-133">-ServerName</span></span>
<span data-ttu-id="0ad16-134">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0ad16-134">SQL server name.</span></span>

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

### <span data-ttu-id="0ad16-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="0ad16-135">-TableName</span></span>
<span data-ttu-id="0ad16-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="0ad16-136">Name of table.</span></span>

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

### <span data-ttu-id="0ad16-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ad16-137">-Confirm</span></span>
<span data-ttu-id="0ad16-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ad16-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad16-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad16-139">-WhatIf</span></span>
<span data-ttu-id="0ad16-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ad16-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ad16-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ad16-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad16-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad16-142">CommonParameters</span></span>
<span data-ttu-id="0ad16-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ad16-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad16-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ad16-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad16-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ad16-145">INPUTS</span></span>

### <span data-ttu-id="0ad16-146">Microsoft. Azure. Commands. SQL. Classification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="0ad16-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="0ad16-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad16-147">OUTPUTS</span></span>

### <span data-ttu-id="0ad16-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ad16-148">System.Boolean</span></span>

## <span data-ttu-id="0ad16-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ad16-149">NOTES</span></span>

## <span data-ttu-id="0ad16-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ad16-150">RELATED LINKS</span></span>

[<span data-ttu-id="0ad16-151">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="0ad16-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
