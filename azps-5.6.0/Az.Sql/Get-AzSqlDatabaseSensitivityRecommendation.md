---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: de5aa5f3347c7277c54d41de9085426b430f167c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014728"
---
# <span data-ttu-id="2b896-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="2b896-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="2b896-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b896-102">SYNOPSIS</span></span>
<span data-ttu-id="2b896-103">Возвращает рекомендуемые типы данных и метки конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="2b896-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="2b896-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b896-104">SYNTAX</span></span>

### <span data-ttu-id="2b896-105">DatabaseObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b896-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b896-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b896-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b896-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b896-107">DESCRIPTION</span></span>
<span data-ttu-id="2b896-108">Этот Get-AzSqlDatabaseSensitivityRecommendation возвращает рекомендуемые типы данных и метки конфиденциальности столбцов базы данных.</span><span class="sxs-lookup"><span data-stu-id="2b896-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="2b896-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b896-109">EXAMPLES</span></span>

### <span data-ttu-id="2b896-110">Пример 1. Получите рекомендуемые типы данных и метки конфиденциальности для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2b896-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
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

### <span data-ttu-id="2b896-111">Пример 2. Получите рекомендуемые типы данных и метки конфиденциальности базы данных Azure SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="2b896-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
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

## <span data-ttu-id="2b896-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b896-112">PARAMETERS</span></span>

### <span data-ttu-id="2b896-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b896-113">-AsJob</span></span>
<span data-ttu-id="2b896-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2b896-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b896-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b896-115">-DatabaseName</span></span>
<span data-ttu-id="2b896-116">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2b896-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="2b896-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2b896-117">-DatabaseObject</span></span>
<span data-ttu-id="2b896-118">Объект SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="2b896-118">The SQL database object.</span></span>

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

### <span data-ttu-id="2b896-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b896-119">-DefaultProfile</span></span>
<span data-ttu-id="2b896-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b896-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b896-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b896-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b896-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b896-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b896-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2b896-123">-ServerName</span></span>
<span data-ttu-id="2b896-124">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2b896-124">SQL server name.</span></span>

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

### <span data-ttu-id="2b896-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b896-125">CommonParameters</span></span>
<span data-ttu-id="2b896-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b896-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b896-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b896-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b896-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b896-128">INPUTS</span></span>

### <span data-ttu-id="2b896-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2b896-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2b896-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b896-130">OUTPUTS</span></span>

### <span data-ttu-id="2b896-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="2b896-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="2b896-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b896-132">NOTES</span></span>

## <span data-ttu-id="2b896-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b896-133">RELATED LINKS</span></span>

[<span data-ttu-id="2b896-134">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="2b896-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
