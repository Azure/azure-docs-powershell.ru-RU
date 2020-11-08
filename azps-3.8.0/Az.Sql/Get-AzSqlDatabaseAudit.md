---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066034"
---
# <span data-ttu-id="5ffa4-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5ffa4-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="5ffa4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ffa4-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffa4-103">Получает параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="5ffa4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ffa4-104">SYNTAX</span></span>

### <span data-ttu-id="5ffa4-105">DatabaseParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ffa4-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ffa4-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ffa4-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ffa4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ffa4-107">DESCRIPTION</span></span>
<span data-ttu-id="5ffa4-108">Командлет **Get-AzSqlDatabaseAudit** получает параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="5ffa4-109">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="5ffa4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ffa4-110">EXAMPLES</span></span>

### <span data-ttu-id="5ffa4-111">Пример 1: получение параметров аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="5ffa4-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="5ffa4-112">Пример 2: Get, с помощью конвейера параметры аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="5ffa4-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="5ffa4-113">Пример 3: получение параметров аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="5ffa4-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
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

## <span data-ttu-id="5ffa4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ffa4-114">PARAMETERS</span></span>

### <span data-ttu-id="5ffa4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ffa4-115">-DatabaseName</span></span>
<span data-ttu-id="5ffa4-116">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-116">SQL Database name.</span></span>

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

### <span data-ttu-id="5ffa4-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5ffa4-117">-DatabaseObject</span></span>
<span data-ttu-id="5ffa4-118">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-118">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="5ffa4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffa4-119">-DefaultProfile</span></span>
<span data-ttu-id="5ffa4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ffa4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffa4-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ffa4-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ffa4-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5ffa4-123">-ServerName</span></span>
<span data-ttu-id="5ffa4-124">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-124">SQL server name.</span></span>

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

### <span data-ttu-id="5ffa4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffa4-125">CommonParameters</span></span>
<span data-ttu-id="5ffa4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffa4-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ffa4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffa4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ffa4-128">INPUTS</span></span>

### <span data-ttu-id="5ffa4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5ffa4-129">System.String</span></span>

### <span data-ttu-id="5ffa4-130">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5ffa4-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5ffa4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ffa4-131">OUTPUTS</span></span>

### <span data-ttu-id="5ffa4-132">Microsoft. Azure. Commands. SQL. Audit. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="5ffa4-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="5ffa4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ffa4-133">NOTES</span></span>

## <span data-ttu-id="5ffa4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ffa4-134">RELATED LINKS</span></span>
