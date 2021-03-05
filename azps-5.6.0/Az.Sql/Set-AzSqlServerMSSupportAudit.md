---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 6e101beb73b68427f806fdae3fa2406082a9b47a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985575"
---
# <span data-ttu-id="3f2ac-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="3f2ac-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="3f2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2ac-103">Изменение параметров аудита операций поддержки Майкрософт на сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="3f2ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f2ac-104">SYNTAX</span></span>

### <span data-ttu-id="3f2ac-105">ServerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f2ac-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f2ac-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f2ac-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f2ac-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f2ac-107">DESCRIPTION</span></span>
<span data-ttu-id="3f2ac-108">Cmdlet **Set-AzSqlServerMSSupportAudit** изменяет параметры аудита операций поддержки Майкрософт для сервера Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="3f2ac-109">Чтобы использовать этот cmdlet, используйте *параметры ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="3f2ac-110">Если хранилище BLOB-устройств является местом назначения для журналов аудита, укажите параметр *StorageAccountResourceId,* чтобы определить учетную запись хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="3f2ac-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f2ac-111">EXAMPLES</span></span>

### <span data-ttu-id="3f2ac-112">Пример 1. В enable the BLOB-хранилище Microsoft support operations auditing policy of an Azure SQL server</span><span class="sxs-lookup"><span data-stu-id="3f2ac-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="3f2ac-113">Пример 2. Отключение политики аудита службы поддержки хранилища BLOB-SQL Microsoft</span><span class="sxs-lookup"><span data-stu-id="3f2ac-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="3f2ac-114">Пример 3. В том случае, если центр событий поддерживает операции аудита для сервера Azure SQL Майкрософт</span><span class="sxs-lookup"><span data-stu-id="3f2ac-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="3f2ac-115">Пример 4. Отключение центра событий службы поддержки Майкрософт для аудита политики azure SQL server</span><span class="sxs-lookup"><span data-stu-id="3f2ac-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="3f2ac-116">Пример 5. В enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span><span class="sxs-lookup"><span data-stu-id="3f2ac-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="3f2ac-117">Пример 6. Отключение аналитики журналов корпорации Майкрософт для операций аудита политики аудита сервера Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3f2ac-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="3f2ac-118">Пример 7. Отключение (через канал) аналитики журналов Корпорации Майкрософт для операций аудита сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="3f2ac-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="3f2ac-119">Пример 8. Отключать отправку записей аудита для операций поддержки Майкрософт на сервере Azure SQL для хранения BLOB-приложений и включить отправку их для аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="3f2ac-120">Пример 9. Отправка записей аудита для операций поддержки Майкрософт на сервере Azure SQL для хранения BLOB-приложений, центра событий и аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="3f2ac-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f2ac-121">PARAMETERS</span></span>

### <span data-ttu-id="3f2ac-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f2ac-122">-AsJob</span></span>
<span data-ttu-id="3f2ac-123">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3f2ac-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f2ac-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="3f2ac-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="3f2ac-125">Указывает, является ли хранилище BLOB-хранилищ назначением для записей аудита операций поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2ac-126">-DefaultProfile</span></span>
<span data-ttu-id="3f2ac-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f2ac-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2ac-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="3f2ac-129">ИД ресурса для правила авторизации концентратора событий</span><span class="sxs-lookup"><span data-stu-id="3f2ac-129">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ac-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="3f2ac-130">-EventHubName</span></span>
<span data-ttu-id="3f2ac-131">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-131">The name of the event hub.</span></span> <span data-ttu-id="3f2ac-132">Если при предоставлении EventHubAuthorizationRuleResourceId отсутствует, будет выбран центр событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ac-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="3f2ac-133">-EventHubTargetState</span></span>
<span data-ttu-id="3f2ac-134">Указывает, является ли центр событий местом назначения для операций аудита службы поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ac-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="3f2ac-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="3f2ac-136">Указывает, является ли аналитика журнала назначением для записей аудита операций поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ac-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f2ac-137">-PassThru</span></span>
<span data-ttu-id="3f2ac-138">Указывает, нужно ли выводить политику аудита операций поддержки Майкрософт в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="3f2ac-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2ac-139">-ResourceGroupName</span></span>
<span data-ttu-id="3f2ac-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f2ac-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3f2ac-141">-ServerName</span></span>
<span data-ttu-id="3f2ac-142">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-142">SQL server name.</span></span>

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

### <span data-ttu-id="3f2ac-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="3f2ac-143">-ServerObject</span></span>
<span data-ttu-id="3f2ac-144">Объект сервера для управления политикой аудита операций поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="3f2ac-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2ac-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="3f2ac-146">ИД ресурса учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="3f2ac-146">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ac-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2ac-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="3f2ac-148">ИД рабочей области (ИД ресурса рабочей области журнала аналитики журнала) для рабочей области "Аналитика журналов", в которую вы хотите отправлять журналы аудита операций поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="3f2ac-149">Пример: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="3f2ac-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ac-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f2ac-150">-Confirm</span></span>
<span data-ttu-id="3f2ac-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f2ac-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f2ac-152">-WhatIf</span></span>
<span data-ttu-id="3f2ac-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f2ac-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f2ac-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2ac-155">CommonParameters</span></span>
<span data-ttu-id="3f2ac-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2ac-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2ac-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f2ac-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2ac-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f2ac-158">INPUTS</span></span>

### <span data-ttu-id="3f2ac-159">System.String</span><span class="sxs-lookup"><span data-stu-id="3f2ac-159">System.String</span></span>

### <span data-ttu-id="3f2ac-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="3f2ac-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="3f2ac-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3f2ac-161">System.Guid</span></span>

### <span data-ttu-id="3f2ac-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3f2ac-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3f2ac-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="3f2ac-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="3f2ac-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f2ac-164">OUTPUTS</span></span>

### <span data-ttu-id="3f2ac-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f2ac-165">System.Boolean</span></span>

## <span data-ttu-id="3f2ac-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f2ac-166">NOTES</span></span>

## <span data-ttu-id="3f2ac-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f2ac-167">RELATED LINKS</span></span>
