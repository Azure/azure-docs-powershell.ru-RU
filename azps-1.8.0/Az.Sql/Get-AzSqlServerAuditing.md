---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: ba225571780d4d09dfd5ecc1b47132462468b734
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728951"
---
# <span data-ttu-id="f3a65-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="f3a65-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="f3a65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3a65-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a65-103">Получает параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f3a65-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="f3a65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3a65-104">SYNTAX</span></span>

### <span data-ttu-id="f3a65-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3a65-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a65-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="f3a65-106">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a65-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="f3a65-107">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a65-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f3a65-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a65-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f3a65-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a65-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f3a65-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3a65-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3a65-111">DESCRIPTION</span></span>
<span data-ttu-id="f3a65-112">Командлет **Get-AzSqlServerAuditing** получает параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f3a65-112">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="f3a65-113">Укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="f3a65-113">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="f3a65-114">Назначение журналов аудита определяется указанием одного из следующих параметров переключателя: BlobStorage, LogAnalytics или EventHub (если ничего не указано, по умолчанию используется значение BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="f3a65-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="f3a65-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3a65-115">EXAMPLES</span></span>

### <span data-ttu-id="f3a65-116">Пример 1: получение параметров аудита хранилища BLOB-объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3a65-116">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="f3a65-117">Пример 2: получение параметров аудита хранилища BLOB-объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3a65-117">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="f3a65-118">Пример 3: Get, через конвейер, параметры аудита хранилища BLOB-объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3a65-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="f3a65-119">Пример 4: получение параметров аудита центра событий для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3a65-119">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="f3a65-120">Пример 5: получение через конвейер, параметры аудита центра событий для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3a65-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="f3a65-121">Пример 6: получение параметров аудита для анализа журналов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3a65-121">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="f3a65-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3a65-122">PARAMETERS</span></span>

### <span data-ttu-id="f3a65-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="f3a65-123">-BlobStorage</span></span>
<span data-ttu-id="f3a65-124">Указывает, что назначение журналов аудита — хранилище BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="f3a65-124">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="f3a65-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a65-125">-DefaultProfile</span></span>
<span data-ttu-id="f3a65-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3a65-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3a65-127">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f3a65-127">-EventHub</span></span>
<span data-ttu-id="f3a65-128">Указывает на то, что назначение журналов аудита является центром событий</span><span class="sxs-lookup"><span data-stu-id="f3a65-128">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="f3a65-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3a65-129">-InputObject</span></span>
<span data-ttu-id="f3a65-130">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="f3a65-130">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="f3a65-131">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="f3a65-131">-LogAnalytics</span></span>
<span data-ttu-id="f3a65-132">Указывает, что назначение журналов аудита — это анализ журнала</span><span class="sxs-lookup"><span data-stu-id="f3a65-132">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="f3a65-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a65-133">-ResourceGroupName</span></span>
<span data-ttu-id="f3a65-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3a65-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3a65-135">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f3a65-135">-ServerName</span></span>
<span data-ttu-id="f3a65-136">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f3a65-136">SQL server name.</span></span>

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

### <span data-ttu-id="f3a65-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3a65-137">-Confirm</span></span>
<span data-ttu-id="f3a65-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3a65-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a65-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a65-139">-WhatIf</span></span>
<span data-ttu-id="f3a65-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3a65-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3a65-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3a65-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a65-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a65-142">CommonParameters</span></span>
<span data-ttu-id="f3a65-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3a65-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a65-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3a65-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a65-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3a65-145">INPUTS</span></span>

### <span data-ttu-id="f3a65-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f3a65-146">System.String</span></span>

### <span data-ttu-id="f3a65-147">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f3a65-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="f3a65-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f3a65-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f3a65-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3a65-149">OUTPUTS</span></span>

### <span data-ttu-id="f3a65-150">Microsoft. Azure. Commands. SQL. Audit. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="f3a65-150">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="f3a65-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3a65-151">NOTES</span></span>

## <span data-ttu-id="f3a65-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3a65-152">RELATED LINKS</span></span>
