---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 6b07ba5e31ab8e301d94b50170aca3869f9dea65
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066945"
---
# <span data-ttu-id="7024d-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7024d-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="7024d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7024d-102">SYNOPSIS</span></span>
<span data-ttu-id="7024d-103">Получает параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7024d-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="7024d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7024d-104">SYNTAX</span></span>

### <span data-ttu-id="7024d-105">ServerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7024d-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7024d-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7024d-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7024d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7024d-107">DESCRIPTION</span></span>
<span data-ttu-id="7024d-108">Командлет **Get-AzSqlServerAudit** получает параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7024d-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="7024d-109">Укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="7024d-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="7024d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7024d-110">EXAMPLES</span></span>

### <span data-ttu-id="7024d-111">Пример 1: получение параметров аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="7024d-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

### <span data-ttu-id="7024d-112">Пример 2: Get, с помощью конвейера параметры аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="7024d-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAudit
ServerName                          : server01
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

### <span data-ttu-id="7024d-113">Пример 3: получение параметров аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="7024d-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

## <span data-ttu-id="7024d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7024d-114">PARAMETERS</span></span>

### <span data-ttu-id="7024d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7024d-115">-AsJob</span></span>
<span data-ttu-id="7024d-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7024d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7024d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7024d-117">-DefaultProfile</span></span>
<span data-ttu-id="7024d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7024d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7024d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7024d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7024d-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7024d-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7024d-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7024d-121">-ServerName</span></span>
<span data-ttu-id="7024d-122">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7024d-122">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7024d-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="7024d-123">-ServerObject</span></span>
<span data-ttu-id="7024d-124">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="7024d-124">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7024d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7024d-125">CommonParameters</span></span>
<span data-ttu-id="7024d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7024d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7024d-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7024d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7024d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7024d-128">INPUTS</span></span>

### <span data-ttu-id="7024d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7024d-129">System.String</span></span>

### <span data-ttu-id="7024d-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7024d-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="7024d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7024d-131">OUTPUTS</span></span>

### <span data-ttu-id="7024d-132">Microsoft. Azure. Commands. SQL. Audit. Model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="7024d-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="7024d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7024d-133">NOTES</span></span>

## <span data-ttu-id="7024d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7024d-134">RELATED LINKS</span></span>
