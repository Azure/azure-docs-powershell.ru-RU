---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217428"
---
# <span data-ttu-id="0f6a5-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0f6a5-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="0f6a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6a5-103">Параметры аудита для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0f6a5-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="0f6a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0f6a5-104">SYNTAX</span></span>

### <span data-ttu-id="0f6a5-105">DatabaseParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f6a5-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f6a5-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f6a5-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f6a5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f6a5-107">DESCRIPTION</span></span>
<span data-ttu-id="0f6a5-108">Чтобы получить параметры аудита для базы данных Azure SQL, можно получить параметры аудита для SQL **AzSqlDatabaseAudit.**</span><span class="sxs-lookup"><span data-stu-id="0f6a5-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="0f6a5-109">Чтобы использовать этот cmdlet, используйте параметры *ResourceGroupName,* *ServerName* и *DatabaseName* для определения базы данных.</span><span class="sxs-lookup"><span data-stu-id="0f6a5-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="0f6a5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0f6a5-110">EXAMPLES</span></span>

### <span data-ttu-id="0f6a5-111">Пример 1. Настройка параметров аудита базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="0f6a5-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="0f6a5-112">Пример 2. Настройка параметров аудита в базе данных Azure SQL с помощью SQL"</span><span class="sxs-lookup"><span data-stu-id="0f6a5-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="0f6a5-113">Пример 3. Настройка параметров аудита базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="0f6a5-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="0f6a5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f6a5-114">PARAMETERS</span></span>

### <span data-ttu-id="0f6a5-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f6a5-115">-DatabaseName</span></span>
<span data-ttu-id="0f6a5-116">SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="0f6a5-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6a5-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0f6a5-117">-DatabaseObject</span></span>
<span data-ttu-id="0f6a5-118">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="0f6a5-118">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="0f6a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6a5-119">-DefaultProfile</span></span>
<span data-ttu-id="0f6a5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f6a5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f6a5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6a5-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f6a5-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f6a5-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6a5-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f6a5-123">-ServerName</span></span>
<span data-ttu-id="0f6a5-124">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="0f6a5-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6a5-125">CommonParameters</span></span>
<span data-ttu-id="0f6a5-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6a5-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f6a5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6a5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f6a5-128">INPUTS</span></span>

### <span data-ttu-id="0f6a5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0f6a5-129">System.String</span></span>

### <span data-ttu-id="0f6a5-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0f6a5-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0f6a5-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f6a5-131">OUTPUTS</span></span>

### <span data-ttu-id="0f6a5-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="0f6a5-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="0f6a5-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0f6a5-133">NOTES</span></span>

## <span data-ttu-id="0f6a5-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f6a5-134">RELATED LINKS</span></span>
