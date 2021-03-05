---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 2f7d9421ada70946f18322828c138eca186df5c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011512"
---
# <span data-ttu-id="e9699-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="e9699-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="e9699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9699-102">SYNOPSIS</span></span>
<span data-ttu-id="e9699-103">Отключает (отключает) рекомендации по конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e9699-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="e9699-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9699-104">SYNTAX</span></span>

### <span data-ttu-id="e9699-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9699-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9699-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9699-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9699-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9699-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9699-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9699-108">DESCRIPTION</span></span>
<span data-ttu-id="e9699-109">Этот Disable-AzSqlDatabaseSensitivityRecommendation отключает (отключает) рекомендации по конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e9699-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="e9699-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9699-110">EXAMPLES</span></span>

### <span data-ttu-id="e9699-111">Пример 1. Отключать рекомендации по конфиденциальности для данного столбца в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e9699-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="e9699-112">Пример 2. Отключать рекомендации по конфиденциальности для столбцов, которые имеют рекомендации по конфиденциальности в базе данных Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="e9699-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="e9699-113">Пример 3. Отключать рекомендации по конфиденциальности для данного столбца в базе данных Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="e9699-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="e9699-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9699-114">PARAMETERS</span></span>

### <span data-ttu-id="e9699-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9699-115">-AsJob</span></span>
<span data-ttu-id="e9699-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e9699-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9699-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e9699-117">-ColumnName</span></span>
<span data-ttu-id="e9699-118">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="e9699-118">Name of column.</span></span>

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

### <span data-ttu-id="e9699-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9699-119">-DatabaseName</span></span>
<span data-ttu-id="e9699-120">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e9699-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="e9699-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e9699-121">-DatabaseObject</span></span>
<span data-ttu-id="e9699-122">Объект SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="e9699-122">The SQL database object.</span></span>

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

### <span data-ttu-id="e9699-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9699-123">-DefaultProfile</span></span>
<span data-ttu-id="e9699-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9699-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9699-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9699-125">-InputObject</span></span>
<span data-ttu-id="e9699-126">Объект, представляющий классификацию SQL конфиденциальности базы данных.</span><span class="sxs-lookup"><span data-stu-id="e9699-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="e9699-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9699-127">-PassThru</span></span>
<span data-ttu-id="e9699-128">Указывает, нужно ли выводить модель классификации конфиденциальности в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9699-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e9699-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9699-129">-ResourceGroupName</span></span>
<span data-ttu-id="e9699-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9699-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9699-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e9699-131">-SchemaName</span></span>
<span data-ttu-id="e9699-132">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="e9699-132">Name of schema.</span></span>

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

### <span data-ttu-id="e9699-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e9699-133">-ServerName</span></span>
<span data-ttu-id="e9699-134">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e9699-134">SQL server name.</span></span>

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

### <span data-ttu-id="e9699-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="e9699-135">-TableName</span></span>
<span data-ttu-id="e9699-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="e9699-136">Name of table.</span></span>

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

### <span data-ttu-id="e9699-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9699-137">-Confirm</span></span>
<span data-ttu-id="e9699-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9699-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9699-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9699-139">-WhatIf</span></span>
<span data-ttu-id="e9699-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9699-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9699-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e9699-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9699-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9699-142">CommonParameters</span></span>
<span data-ttu-id="e9699-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9699-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9699-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9699-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9699-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9699-145">INPUTS</span></span>

### <span data-ttu-id="e9699-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e9699-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="e9699-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9699-147">OUTPUTS</span></span>

### <span data-ttu-id="e9699-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9699-148">System.Boolean</span></span>

## <span data-ttu-id="e9699-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9699-149">NOTES</span></span>

## <span data-ttu-id="e9699-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9699-150">RELATED LINKS</span></span>

[<span data-ttu-id="e9699-151">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="e9699-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)