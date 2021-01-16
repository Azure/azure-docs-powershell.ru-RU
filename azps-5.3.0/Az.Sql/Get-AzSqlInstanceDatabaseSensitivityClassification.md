---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fe8cffb4ab9d79828795cc1148a3c109cfbfdddb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506657"
---
# <span data-ttu-id="b781f-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="b781f-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="b781f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b781f-102">SYNOPSIS</span></span>
<span data-ttu-id="b781f-103">Возвращает текущие типы данных и метки конфиденциальности столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b781f-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b781f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b781f-104">SYNTAX</span></span>

### <span data-ttu-id="b781f-105">DatabaseObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b781f-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b781f-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="b781f-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b781f-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b781f-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b781f-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b781f-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b781f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b781f-109">DESCRIPTION</span></span>
<span data-ttu-id="b781f-110">Этот Get-AzSqlInstanceDatabaseSensitivityClassification возвращает текущие типы данных и метки конфиденциальности столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b781f-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b781f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b781f-111">EXAMPLES</span></span>

### <span data-ttu-id="b781f-112">Пример 1. Получите текущие типы данных и метки конфиденциальности для базы данных azure SQL экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b781f-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="b781f-113">Пример 2. Получите текущие типы данных и метки конфиденциальности для базы данных Azure SQL Экземпляра с Piping.</span><span class="sxs-lookup"><span data-stu-id="b781f-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="b781f-114">Пример 3. Получите текущий тип данных и метку конфиденциальности для определенного столбца базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b781f-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="b781f-115">Пример 4. Получите текущий тип данных и метку конфиденциальности для определенного столбца базы данных azure SQL экземпляра с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="b781f-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="b781f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b781f-116">PARAMETERS</span></span>

### <span data-ttu-id="b781f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b781f-117">-AsJob</span></span>
<span data-ttu-id="b781f-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b781f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b781f-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b781f-119">-ColumnName</span></span>
<span data-ttu-id="b781f-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="b781f-120">Name of column.</span></span>

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

### <span data-ttu-id="b781f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b781f-121">-DatabaseName</span></span>
<span data-ttu-id="b781f-122">Имя базы данных экземпляра Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b781f-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="b781f-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b781f-123">-DatabaseObject</span></span>
<span data-ttu-id="b781f-124">Объект базы SQL экземпляра Azure.</span><span class="sxs-lookup"><span data-stu-id="b781f-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b781f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b781f-125">-DefaultProfile</span></span>
<span data-ttu-id="b781f-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b781f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b781f-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b781f-127">-InstanceName</span></span>
<span data-ttu-id="b781f-128">Azure SQL управляемым именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b781f-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="b781f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b781f-129">-ResourceGroupName</span></span>
<span data-ttu-id="b781f-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b781f-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b781f-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b781f-131">-SchemaName</span></span>
<span data-ttu-id="b781f-132">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="b781f-132">Name of schema.</span></span>

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

### <span data-ttu-id="b781f-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="b781f-133">-TableName</span></span>
<span data-ttu-id="b781f-134">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="b781f-134">Name of table.</span></span>

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

### <span data-ttu-id="b781f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b781f-135">CommonParameters</span></span>
<span data-ttu-id="b781f-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b781f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b781f-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b781f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b781f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b781f-138">INPUTS</span></span>

### <span data-ttu-id="b781f-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b781f-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b781f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b781f-140">OUTPUTS</span></span>

### <span data-ttu-id="b781f-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b781f-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b781f-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b781f-142">NOTES</span></span>

## <span data-ttu-id="b781f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b781f-143">RELATED LINKS</span></span>

[<span data-ttu-id="b781f-144">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="b781f-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)