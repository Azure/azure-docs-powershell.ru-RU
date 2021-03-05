---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 3cc73a3f359207db947c03bf42aafb3c7beff11e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961363"
---
# <span data-ttu-id="9f00b-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="9f00b-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="9f00b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f00b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f00b-103">Удаляет типы данных и метки конфиденциальности столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9f00b-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="9f00b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f00b-104">SYNTAX</span></span>

### <span data-ttu-id="9f00b-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f00b-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f00b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f00b-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f00b-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f00b-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f00b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f00b-108">DESCRIPTION</span></span>
<span data-ttu-id="9f00b-109">Этот Remove-AzSqlDatabaseSensitivityClassification удаляет типы данных и метки конфиденциальности столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9f00b-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="9f00b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f00b-110">EXAMPLES</span></span>

### <span data-ttu-id="9f00b-111">Пример 1. Удаление типа данных и метки конфиденциальности столбца в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9f00b-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="9f00b-112">Пример 2. Удаление текущих типов данных и меток конфиденциальности столбцов в базе данных Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="9f00b-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="9f00b-113">Пример 3. Удаление метки типа данных и конфиденциальности столбца в базе данных Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="9f00b-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="9f00b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f00b-114">PARAMETERS</span></span>

### <span data-ttu-id="9f00b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f00b-115">-AsJob</span></span>
<span data-ttu-id="9f00b-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9f00b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f00b-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="9f00b-117">-ClassificationObject</span></span>
<span data-ttu-id="9f00b-118">Объект, представляющий классификацию SQL конфиденциальности базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f00b-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="9f00b-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9f00b-119">-ColumnName</span></span>
<span data-ttu-id="9f00b-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="9f00b-120">Name of column.</span></span>

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

### <span data-ttu-id="9f00b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9f00b-121">-DatabaseName</span></span>
<span data-ttu-id="9f00b-122">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9f00b-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="9f00b-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9f00b-123">-DatabaseObject</span></span>
<span data-ttu-id="9f00b-124">Объект SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f00b-124">The SQL database object.</span></span>

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

### <span data-ttu-id="9f00b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f00b-125">-DefaultProfile</span></span>
<span data-ttu-id="9f00b-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f00b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f00b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f00b-127">-PassThru</span></span>
<span data-ttu-id="9f00b-128">Указывает, нужно ли выводить модель классификации конфиденциальности в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f00b-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9f00b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f00b-129">-ResourceGroupName</span></span>
<span data-ttu-id="9f00b-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f00b-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f00b-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9f00b-131">-SchemaName</span></span>
<span data-ttu-id="9f00b-132">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="9f00b-132">Name of schema.</span></span>

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

### <span data-ttu-id="9f00b-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9f00b-133">-ServerName</span></span>
<span data-ttu-id="9f00b-134">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9f00b-134">SQL server name.</span></span>

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

### <span data-ttu-id="9f00b-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="9f00b-135">-TableName</span></span>
<span data-ttu-id="9f00b-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="9f00b-136">Name of table.</span></span>

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

### <span data-ttu-id="9f00b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f00b-137">-Confirm</span></span>
<span data-ttu-id="9f00b-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9f00b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f00b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f00b-139">-WhatIf</span></span>
<span data-ttu-id="9f00b-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f00b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f00b-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f00b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f00b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f00b-142">CommonParameters</span></span>
<span data-ttu-id="9f00b-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f00b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f00b-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f00b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f00b-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f00b-145">INPUTS</span></span>

### <span data-ttu-id="9f00b-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9f00b-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9f00b-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f00b-147">OUTPUTS</span></span>

### <span data-ttu-id="9f00b-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f00b-148">System.Boolean</span></span>

## <span data-ttu-id="9f00b-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f00b-149">NOTES</span></span>

## <span data-ttu-id="9f00b-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f00b-150">RELATED LINKS</span></span>

[<span data-ttu-id="9f00b-151">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="9f00b-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
