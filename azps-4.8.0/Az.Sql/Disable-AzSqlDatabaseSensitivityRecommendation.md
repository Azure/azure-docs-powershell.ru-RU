---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243275"
---
# <span data-ttu-id="9e247-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="9e247-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="9e247-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e247-102">SYNOPSIS</span></span>
<span data-ttu-id="9e247-103">Запрещает (отправку) рекомендации относительно чувствительности к столбцам базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e247-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="9e247-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e247-104">SYNTAX</span></span>

### <span data-ttu-id="9e247-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e247-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e247-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e247-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e247-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e247-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e247-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e247-108">DESCRIPTION</span></span>
<span data-ttu-id="9e247-109">Командлет Disable-AzSqlDatabaseSensitivityRecommendation отключает (пропуски) рекомендации по пометкам столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9e247-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="9e247-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e247-110">EXAMPLES</span></span>

### <span data-ttu-id="9e247-111">Пример 1: отключение рекомендаций по конфиденциальности для определенного столбца в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9e247-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="9e247-112">Пример 2. Отключите рекомендации по пометкам для столбцов, которые содержат рекомендации по пометкам в базе данных Azure SQL с использованием конвейера.</span><span class="sxs-lookup"><span data-stu-id="9e247-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="9e247-113">Пример 3. Отключите рекомендации по отметкам для определенного столбца в базе данных Azure SQL с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="9e247-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="9e247-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e247-114">PARAMETERS</span></span>

### <span data-ttu-id="9e247-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e247-115">-AsJob</span></span>
<span data-ttu-id="9e247-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9e247-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e247-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9e247-117">-ColumnName</span></span>
<span data-ttu-id="9e247-118">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="9e247-118">Name of column.</span></span>

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

### <span data-ttu-id="9e247-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9e247-119">-DatabaseName</span></span>
<span data-ttu-id="9e247-120">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9e247-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="9e247-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9e247-121">-DatabaseObject</span></span>
<span data-ttu-id="9e247-122">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="9e247-122">The SQL database object.</span></span>

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

### <span data-ttu-id="9e247-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e247-123">-DefaultProfile</span></span>
<span data-ttu-id="9e247-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e247-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e247-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e247-125">-InputObject</span></span>
<span data-ttu-id="9e247-126">Объект, представляющий классификацию чувствительности базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="9e247-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="9e247-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e247-127">-PassThru</span></span>
<span data-ttu-id="9e247-128">Указывает, следует ли выводить модель классификации чувствительности при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="9e247-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9e247-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e247-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e247-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e247-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e247-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9e247-131">-SchemaName</span></span>
<span data-ttu-id="9e247-132">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="9e247-132">Name of schema.</span></span>

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

### <span data-ttu-id="9e247-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9e247-133">-ServerName</span></span>
<span data-ttu-id="9e247-134">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9e247-134">SQL server name.</span></span>

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

### <span data-ttu-id="9e247-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="9e247-135">-TableName</span></span>
<span data-ttu-id="9e247-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e247-136">Name of table.</span></span>

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

### <span data-ttu-id="9e247-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e247-137">-Confirm</span></span>
<span data-ttu-id="9e247-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e247-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e247-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e247-139">-WhatIf</span></span>
<span data-ttu-id="9e247-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e247-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e247-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e247-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e247-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e247-142">CommonParameters</span></span>
<span data-ttu-id="9e247-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e247-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e247-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e247-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e247-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e247-145">INPUTS</span></span>

### <span data-ttu-id="9e247-146">Microsoft. Azure. Commands. SQL. Classification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9e247-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9e247-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e247-147">OUTPUTS</span></span>

### <span data-ttu-id="9e247-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e247-148">System.Boolean</span></span>

## <span data-ttu-id="9e247-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e247-149">NOTES</span></span>

## <span data-ttu-id="9e247-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e247-150">RELATED LINKS</span></span>

[<span data-ttu-id="9e247-151">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9e247-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)