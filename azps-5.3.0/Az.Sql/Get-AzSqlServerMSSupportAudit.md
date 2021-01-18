---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: c4f3687b2e520783c4b0392e1711dcea976e0c05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504685"
---
# <span data-ttu-id="7512b-101">Get-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="7512b-101">Get-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="7512b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7512b-102">SYNOPSIS</span></span>
<span data-ttu-id="7512b-103">Получает параметры аудита операций поддержки Майкрософт на сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7512b-103">Gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="7512b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7512b-104">SYNTAX</span></span>

### <span data-ttu-id="7512b-105">ServerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7512b-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7512b-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7512b-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7512b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7512b-107">DESCRIPTION</span></span>
<span data-ttu-id="7512b-108">Для получения параметров аудита операций аудита для сервера Azure SQL Майкрософт возвращается **cmdlet Get-AzSqlServerMSSupportAudit.**</span><span class="sxs-lookup"><span data-stu-id="7512b-108">The **Get-AzSqlServerMSSupportAudit** cmdlet gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="7512b-109">Укажите *параметры ResourceGroupName* *и ServerName,* чтобы определить сервер.</span><span class="sxs-lookup"><span data-stu-id="7512b-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="7512b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7512b-110">EXAMPLES</span></span>

### <span data-ttu-id="7512b-111">Пример 1. Получить параметры аудита операций поддержки Майкрософт для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7512b-111">Example 1: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7512b-112">Пример 2. По конвейеру служба поддержки Майкрософт проводит аудит параметров сервера Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7512b-112">Example 2: Get, through pipeline, the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerMSSupportAudit
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7512b-113">Пример 3. Настройка параметров аудита операций поддержки Майкрософт на сервере Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7512b-113">Example 3: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="7512b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7512b-114">PARAMETERS</span></span>

### <span data-ttu-id="7512b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7512b-115">-AsJob</span></span>
<span data-ttu-id="7512b-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7512b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7512b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7512b-117">-DefaultProfile</span></span>
<span data-ttu-id="7512b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7512b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7512b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7512b-119">-ResourceGroupName</span></span>
<span data-ttu-id="7512b-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7512b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7512b-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7512b-121">-ServerName</span></span>
<span data-ttu-id="7512b-122">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7512b-122">SQL server name.</span></span>

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

### <span data-ttu-id="7512b-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="7512b-123">-ServerObject</span></span>
<span data-ttu-id="7512b-124">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="7512b-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="7512b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7512b-125">CommonParameters</span></span>
<span data-ttu-id="7512b-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7512b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7512b-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7512b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7512b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7512b-128">INPUTS</span></span>

### <span data-ttu-id="7512b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7512b-129">System.String</span></span>

### <span data-ttu-id="7512b-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7512b-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="7512b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7512b-131">OUTPUTS</span></span>

### <span data-ttu-id="7512b-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="7512b-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="7512b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7512b-133">NOTES</span></span>

## <span data-ttu-id="7512b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7512b-134">RELATED LINKS</span></span>
