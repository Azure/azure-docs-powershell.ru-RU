---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: beada19e6b5ba7792c3fda6ca07ce987bd15fe2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225196"
---
# <span data-ttu-id="dd7c8-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="dd7c8-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="dd7c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7c8-103">Возвращает текущие типы данных и метки конфиденциальности столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="dd7c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd7c8-104">SYNTAX</span></span>

### <span data-ttu-id="dd7c8-105">DatabaseObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd7c8-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd7c8-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd7c8-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd7c8-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd7c8-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd7c8-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd7c8-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd7c8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd7c8-109">DESCRIPTION</span></span>
<span data-ttu-id="dd7c8-110">Этот Get-AzSqlDatabaseSensitivityClassification возвращает текущие типы данных и метки конфиденциальности столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="dd7c8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd7c8-111">EXAMPLES</span></span>

### <span data-ttu-id="dd7c8-112">Пример 1. Получите текущие типы данных и метки конфиденциальности для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="dd7c8-113">Пример 2. Получите текущие типы данных и метки конфиденциальности базы данных Azure SQL с Piping.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="dd7c8-114">Пример 3. Получите текущий тип данных и метку конфиденциальности для определенного столбца базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="dd7c8-115">Пример 4. Получите текущий тип данных и метку конфиденциальности определенного столбца базы данных Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="dd7c8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd7c8-116">PARAMETERS</span></span>

### <span data-ttu-id="dd7c8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd7c8-117">-AsJob</span></span>
<span data-ttu-id="dd7c8-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dd7c8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd7c8-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="dd7c8-119">-ColumnName</span></span>
<span data-ttu-id="dd7c8-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-120">Name of column.</span></span>

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

### <span data-ttu-id="dd7c8-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd7c8-121">-DatabaseName</span></span>
<span data-ttu-id="dd7c8-122">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c8-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="dd7c8-123">-DatabaseObject</span></span>
<span data-ttu-id="dd7c8-124">Объект SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7c8-125">-DefaultProfile</span></span>
<span data-ttu-id="dd7c8-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd7c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd7c8-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c8-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dd7c8-129">-SchemaName</span></span>
<span data-ttu-id="dd7c8-130">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-130">Name of schema.</span></span>

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

### <span data-ttu-id="dd7c8-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dd7c8-131">-ServerName</span></span>
<span data-ttu-id="dd7c8-132">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-132">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c8-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="dd7c8-133">-TableName</span></span>
<span data-ttu-id="dd7c8-134">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-134">Name of table.</span></span>

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

### <span data-ttu-id="dd7c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7c8-135">CommonParameters</span></span>
<span data-ttu-id="dd7c8-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7c8-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd7c8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7c8-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd7c8-138">INPUTS</span></span>

### <span data-ttu-id="dd7c8-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="dd7c8-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="dd7c8-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd7c8-140">OUTPUTS</span></span>

### <span data-ttu-id="dd7c8-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="dd7c8-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="dd7c8-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd7c8-142">NOTES</span></span>

## <span data-ttu-id="dd7c8-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd7c8-143">RELATED LINKS</span></span>

[<span data-ttu-id="dd7c8-144">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="dd7c8-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
