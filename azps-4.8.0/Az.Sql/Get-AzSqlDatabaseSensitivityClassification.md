---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: beada19e6b5ba7792c3fda6ca07ce987bd15fe2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078695"
---
# <span data-ttu-id="05ef0-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="05ef0-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="05ef0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="05ef0-103">Возвращает текущие типы сведений и метки чувствительности к столбцам в базе данных.</span><span class="sxs-lookup"><span data-stu-id="05ef0-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="05ef0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05ef0-104">SYNTAX</span></span>

### <span data-ttu-id="05ef0-105">DatabaseObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05ef0-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05ef0-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="05ef0-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05ef0-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="05ef0-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05ef0-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="05ef0-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05ef0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05ef0-109">DESCRIPTION</span></span>
<span data-ttu-id="05ef0-110">Командлет Get-AzSqlDatabaseSensitivityClassification возвращает текущие типы данных и метки чувствительности столбцов в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="05ef0-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="05ef0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05ef0-111">EXAMPLES</span></span>

### <span data-ttu-id="05ef0-112">Пример 1: получение текущих типов сведений и меток чувствительности для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="05ef0-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
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

### <span data-ttu-id="05ef0-113">Пример 2: получение актуальных сведений о типах данных и метках чувствительных к учетной записью в SQL Server с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="05ef0-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
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

### <span data-ttu-id="05ef0-114">Пример 3: получение сведений о типе и конфиденциальности для определенного столбца базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="05ef0-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
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

### <span data-ttu-id="05ef0-115">Пример 4: получение сведений о текущем типе информации и метке о конфиденциальности для определенного столбца базы данных Azure SQL с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="05ef0-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
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

## <span data-ttu-id="05ef0-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05ef0-116">PARAMETERS</span></span>

### <span data-ttu-id="05ef0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05ef0-117">-AsJob</span></span>
<span data-ttu-id="05ef0-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="05ef0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05ef0-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="05ef0-119">-ColumnName</span></span>
<span data-ttu-id="05ef0-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="05ef0-120">Name of column.</span></span>

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

### <span data-ttu-id="05ef0-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05ef0-121">-DatabaseName</span></span>
<span data-ttu-id="05ef0-122">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="05ef0-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="05ef0-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="05ef0-123">-DatabaseObject</span></span>
<span data-ttu-id="05ef0-124">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="05ef0-124">The SQL database object.</span></span>

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

### <span data-ttu-id="05ef0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ef0-125">-DefaultProfile</span></span>
<span data-ttu-id="05ef0-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05ef0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05ef0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ef0-127">-ResourceGroupName</span></span>
<span data-ttu-id="05ef0-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05ef0-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="05ef0-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="05ef0-129">-SchemaName</span></span>
<span data-ttu-id="05ef0-130">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="05ef0-130">Name of schema.</span></span>

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

### <span data-ttu-id="05ef0-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="05ef0-131">-ServerName</span></span>
<span data-ttu-id="05ef0-132">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05ef0-132">SQL server name.</span></span>

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

### <span data-ttu-id="05ef0-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="05ef0-133">-TableName</span></span>
<span data-ttu-id="05ef0-134">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="05ef0-134">Name of table.</span></span>

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

### <span data-ttu-id="05ef0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ef0-135">CommonParameters</span></span>
<span data-ttu-id="05ef0-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05ef0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ef0-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05ef0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ef0-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05ef0-138">INPUTS</span></span>

### <span data-ttu-id="05ef0-139">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="05ef0-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="05ef0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05ef0-140">OUTPUTS</span></span>

### <span data-ttu-id="05ef0-141">Microsoft. Azure. Commands. SQL. Classification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="05ef0-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="05ef0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="05ef0-142">NOTES</span></span>

## <span data-ttu-id="05ef0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05ef0-143">RELATED LINKS</span></span>

[<span data-ttu-id="05ef0-144">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="05ef0-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
