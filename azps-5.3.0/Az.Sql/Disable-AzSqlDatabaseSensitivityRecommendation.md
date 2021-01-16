---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419548"
---
# <span data-ttu-id="5a6a2-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="5a6a2-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="5a6a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6a2-103">Отключает (отключает) рекомендации по конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="5a6a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a6a2-104">SYNTAX</span></span>

### <span data-ttu-id="5a6a2-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a6a2-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6a2-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a6a2-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6a2-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a6a2-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6a2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a6a2-108">DESCRIPTION</span></span>
<span data-ttu-id="5a6a2-109">Этот Disable-AzSqlDatabaseSensitivityRecommendation отключает (отключает) рекомендации по конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="5a6a2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a6a2-110">EXAMPLES</span></span>

### <span data-ttu-id="5a6a2-111">Пример 1. Отключать рекомендации по конфиденциальности для данного столбца в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="5a6a2-112">Пример 2. Отключать рекомендации по конфиденциальности для столбцов, которые имеют рекомендации по конфиденциальности в базе данных Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="5a6a2-113">Пример 3. Отключать рекомендации по конфиденциальности для данного столбца в базе данных Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="5a6a2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a6a2-114">PARAMETERS</span></span>

### <span data-ttu-id="5a6a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a6a2-115">-AsJob</span></span>
<span data-ttu-id="5a6a2-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5a6a2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a6a2-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5a6a2-117">-ColumnName</span></span>
<span data-ttu-id="5a6a2-118">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-118">Name of column.</span></span>

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

### <span data-ttu-id="5a6a2-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a6a2-119">-DatabaseName</span></span>
<span data-ttu-id="5a6a2-120">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="5a6a2-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5a6a2-121">-DatabaseObject</span></span>
<span data-ttu-id="5a6a2-122">Объект SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-122">The SQL database object.</span></span>

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

### <span data-ttu-id="5a6a2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6a2-123">-DefaultProfile</span></span>
<span data-ttu-id="5a6a2-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a6a2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a6a2-125">-InputObject</span></span>
<span data-ttu-id="5a6a2-126">Объект, представляющий SQL классификации конфиденциальности базы данных.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="5a6a2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a6a2-127">-PassThru</span></span>
<span data-ttu-id="5a6a2-128">Указывает, нужно ли выводить модель классификации конфиденциальности в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="5a6a2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a6a2-129">-ResourceGroupName</span></span>
<span data-ttu-id="5a6a2-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="5a6a2-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5a6a2-131">-SchemaName</span></span>
<span data-ttu-id="5a6a2-132">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-132">Name of schema.</span></span>

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

### <span data-ttu-id="5a6a2-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a6a2-133">-ServerName</span></span>
<span data-ttu-id="5a6a2-134">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-134">SQL server name.</span></span>

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

### <span data-ttu-id="5a6a2-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="5a6a2-135">-TableName</span></span>
<span data-ttu-id="5a6a2-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-136">Name of table.</span></span>

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

### <span data-ttu-id="5a6a2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a6a2-137">-Confirm</span></span>
<span data-ttu-id="5a6a2-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6a2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6a2-139">-WhatIf</span></span>
<span data-ttu-id="5a6a2-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a6a2-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a6a2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6a2-142">CommonParameters</span></span>
<span data-ttu-id="5a6a2-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a6a2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6a2-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a6a2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6a2-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a6a2-145">INPUTS</span></span>

### <span data-ttu-id="5a6a2-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="5a6a2-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="5a6a2-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a6a2-147">OUTPUTS</span></span>

### <span data-ttu-id="5a6a2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a6a2-148">System.Boolean</span></span>

## <span data-ttu-id="5a6a2-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a6a2-149">NOTES</span></span>

## <span data-ttu-id="5a6a2-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a6a2-150">RELATED LINKS</span></span>

[<span data-ttu-id="5a6a2-151">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="5a6a2-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)