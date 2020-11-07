---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: cf9bea67027e7a2c5e3928755f6d88b1dc124489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906662"
---
# <span data-ttu-id="ecb79-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="ecb79-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="ecb79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecb79-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb79-103">**Внимание! этот командлет устарел, его можно заменить [на Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) .**</span><span class="sxs-lookup"><span data-stu-id="ecb79-103">**Important: This cmdlet is deprecated, [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="ecb79-104">Получает параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ecb79-104">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="ecb79-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecb79-105">SYNTAX</span></span>

### <span data-ttu-id="ecb79-106">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecb79-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb79-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="ecb79-107">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb79-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="ecb79-108">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb79-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ecb79-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb79-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ecb79-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb79-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ecb79-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecb79-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecb79-112">DESCRIPTION</span></span>
<span data-ttu-id="ecb79-113">Командлет **Get-AzSqlServerAuditing** получает параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ecb79-113">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="ecb79-114">Укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="ecb79-114">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="ecb79-115">Назначение журналов аудита определяется указанием одного из следующих параметров переключателя: BlobStorage, LogAnalytics или EventHub (если ничего не указано, по умолчанию используется значение BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="ecb79-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="ecb79-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecb79-116">EXAMPLES</span></span>

### <span data-ttu-id="ecb79-117">Пример 1: получение параметров аудита хранилища BLOB-объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="ecb79-117">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ecb79-118">Пример 2: получение параметров аудита хранилища BLOB-объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="ecb79-118">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ecb79-119">Пример 3: Get, через конвейер, параметры аудита хранилища BLOB-объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="ecb79-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ecb79-120">Пример 4: получение параметров аудита центра событий для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="ecb79-120">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="ecb79-121">Пример 5: получение через конвейер, параметры аудита центра событий для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="ecb79-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="ecb79-122">Пример 6: получение параметров аудита для анализа журналов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="ecb79-122">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="ecb79-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecb79-123">PARAMETERS</span></span>

### <span data-ttu-id="ecb79-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="ecb79-124">-BlobStorage</span></span>
<span data-ttu-id="ecb79-125">Указывает, что назначение журналов аудита — хранилище BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="ecb79-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb79-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb79-126">-DefaultProfile</span></span>
<span data-ttu-id="ecb79-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecb79-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecb79-128">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ecb79-128">-EventHub</span></span>
<span data-ttu-id="ecb79-129">Указывает на то, что назначение журналов аудита является центром событий</span><span class="sxs-lookup"><span data-stu-id="ecb79-129">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb79-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb79-130">-InputObject</span></span>
<span data-ttu-id="ecb79-131">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="ecb79-131">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb79-132">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="ecb79-132">-LogAnalytics</span></span>
<span data-ttu-id="ecb79-133">Указывает, что назначение журналов аудита — это анализ журнала</span><span class="sxs-lookup"><span data-stu-id="ecb79-133">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb79-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb79-134">-ResourceGroupName</span></span>
<span data-ttu-id="ecb79-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ecb79-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb79-136">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ecb79-136">-ServerName</span></span>
<span data-ttu-id="ecb79-137">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ecb79-137">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb79-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecb79-138">-Confirm</span></span>
<span data-ttu-id="ecb79-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ecb79-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb79-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb79-140">-WhatIf</span></span>
<span data-ttu-id="ecb79-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ecb79-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecb79-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecb79-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb79-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb79-143">CommonParameters</span></span>
<span data-ttu-id="ecb79-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecb79-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb79-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecb79-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb79-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecb79-146">INPUTS</span></span>

### <span data-ttu-id="ecb79-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ecb79-147">System.String</span></span>

### <span data-ttu-id="ecb79-148">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ecb79-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="ecb79-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ecb79-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ecb79-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecb79-150">OUTPUTS</span></span>

### <span data-ttu-id="ecb79-151">Microsoft. Azure. Commands. SQL. Audit. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="ecb79-151">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="ecb79-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecb79-152">NOTES</span></span>

## <span data-ttu-id="ecb79-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecb79-153">RELATED LINKS</span></span>
