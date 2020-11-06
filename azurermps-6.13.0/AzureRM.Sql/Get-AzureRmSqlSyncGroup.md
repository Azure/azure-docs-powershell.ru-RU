---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: bc4a547ec216cc4c88837f48eadc1c1e80c9087a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568143"
---
# <span data-ttu-id="91058-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91058-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="91058-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91058-102">SYNOPSIS</span></span>
<span data-ttu-id="91058-103">Возвращает сведения о группах синхронизации базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="91058-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91058-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91058-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91058-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91058-105">DESCRIPTION</span></span>
<span data-ttu-id="91058-106">Командлет **Get-AzureRmSqlSyncGroup** возвращает сведения о одной или нескольких группах синхронизации базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="91058-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="91058-107">Укажите имя группы синхронизации, чтобы просмотреть сведения только для этой группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="91058-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="91058-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91058-108">EXAMPLES</span></span>

### <span data-ttu-id="91058-109">Пример 1: получение всех экземпляров группы синхронизации Azure SQL, назначенных базе данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="91058-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="91058-110">Эта команда получает сведения обо всех группах синхронизации базы данных SQL Azure, назначенных в базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="91058-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="91058-111">Пример 2: получение сведений о группе синхронизации базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="91058-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="91058-112">Эта команда получает сведения о группе синхронизации базы данных SQL Azure с именем "SyncGroup01".</span><span class="sxs-lookup"><span data-stu-id="91058-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="91058-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91058-113">PARAMETERS</span></span>

### <span data-ttu-id="91058-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91058-114">-DatabaseName</span></span>
<span data-ttu-id="91058-115">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="91058-115">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91058-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91058-116">-DefaultProfile</span></span>
<span data-ttu-id="91058-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="91058-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91058-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91058-118">-Name</span></span>
<span data-ttu-id="91058-119">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="91058-119">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91058-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91058-120">-ResourceGroupName</span></span>
<span data-ttu-id="91058-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91058-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91058-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="91058-122">-ServerName</span></span>
<span data-ttu-id="91058-123">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="91058-123">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91058-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91058-124">CommonParameters</span></span>
<span data-ttu-id="91058-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91058-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91058-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91058-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91058-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91058-127">INPUTS</span></span>

### <span data-ttu-id="91058-128">System. String</span><span class="sxs-lookup"><span data-stu-id="91058-128">System.String</span></span>

## <span data-ttu-id="91058-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91058-129">OUTPUTS</span></span>

### <span data-ttu-id="91058-130">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="91058-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="91058-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="91058-131">NOTES</span></span>

## <span data-ttu-id="91058-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91058-132">RELATED LINKS</span></span>

[<span data-ttu-id="91058-133">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91058-133">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="91058-134">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91058-134">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="91058-135">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91058-135">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

