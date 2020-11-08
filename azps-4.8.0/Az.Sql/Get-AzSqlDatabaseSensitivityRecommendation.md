---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243940"
---
# <span data-ttu-id="b0a84-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="b0a84-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="b0a84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0a84-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a84-103">Получает Рекомендуемые типы сведений и метки чувствительности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b0a84-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="b0a84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0a84-104">SYNTAX</span></span>

### <span data-ttu-id="b0a84-105">DatabaseObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0a84-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0a84-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a84-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0a84-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0a84-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a84-108">Командлет Get-AzSqlDatabaseSensitivityRecommendation возвращает Рекомендуемые типы данных и метки чувствительности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b0a84-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="b0a84-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0a84-109">EXAMPLES</span></span>

### <span data-ttu-id="b0a84-110">Пример 1: получение рекомендуемых типов данных и меток чувствительности для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a84-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

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

### <span data-ttu-id="b0a84-111">Пример 2: получение рекомендуемых типов данных и меток чувствительности для базы данных SQL Azure с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="b0a84-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

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

## <span data-ttu-id="b0a84-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0a84-112">PARAMETERS</span></span>

### <span data-ttu-id="b0a84-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0a84-113">-AsJob</span></span>
<span data-ttu-id="b0a84-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b0a84-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0a84-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0a84-115">-DatabaseName</span></span>
<span data-ttu-id="b0a84-116">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a84-116">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a84-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b0a84-117">-DatabaseObject</span></span>
<span data-ttu-id="b0a84-118">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b0a84-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a84-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a84-119">-DefaultProfile</span></span>
<span data-ttu-id="b0a84-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a84-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a84-121">-ResourceGroupName</span></span>
<span data-ttu-id="b0a84-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0a84-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a84-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b0a84-123">-ServerName</span></span>
<span data-ttu-id="b0a84-124">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b0a84-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a84-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a84-125">CommonParameters</span></span>
<span data-ttu-id="b0a84-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0a84-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a84-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0a84-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a84-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0a84-128">INPUTS</span></span>

### <span data-ttu-id="b0a84-129">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b0a84-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b0a84-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0a84-130">OUTPUTS</span></span>

### <span data-ttu-id="b0a84-131">Microsoft. Azure. Commands. SQL. Classification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b0a84-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b0a84-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0a84-132">NOTES</span></span>

## <span data-ttu-id="b0a84-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0a84-133">RELATED LINKS</span></span>

[<span data-ttu-id="b0a84-134">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b0a84-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
