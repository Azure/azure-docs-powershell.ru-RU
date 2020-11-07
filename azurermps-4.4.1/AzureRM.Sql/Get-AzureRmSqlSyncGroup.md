---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: e581f0bd94e58f725055c0dc1a4f1d704b891c86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732191"
---
# <span data-ttu-id="9c579-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9c579-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="9c579-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c579-102">SYNOPSIS</span></span>
<span data-ttu-id="9c579-103">Возвращает сведения о группах синхронизации базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9c579-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c579-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c579-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c579-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c579-105">DESCRIPTION</span></span>
<span data-ttu-id="9c579-106">Командлет **Get-AzureRmSqlSyncGroup** возвращает сведения о одной или нескольких группах синхронизации базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9c579-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="9c579-107">Укажите имя группы синхронизации, чтобы просмотреть сведения только для этой группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9c579-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="9c579-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c579-108">EXAMPLES</span></span>

### <span data-ttu-id="9c579-109">Пример 1: получение всех экземпляров группы синхронизации Azure SQL, назначенных базе данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="9c579-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="9c579-110">Эта команда получает сведения обо всех группах синхронизации базы данных SQL Azure, назначенных в базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9c579-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="9c579-111">Пример 2: получение сведений о группе синхронизации базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="9c579-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="9c579-112">Эта команда получает сведения о группе синхронизации базы данных SQL Azure с именем "SyncGroup01".</span><span class="sxs-lookup"><span data-stu-id="9c579-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="9c579-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c579-113">PARAMETERS</span></span>

### <span data-ttu-id="9c579-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c579-114">-DatabaseName</span></span>
<span data-ttu-id="9c579-115">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9c579-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9c579-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c579-116">-Name</span></span>
<span data-ttu-id="9c579-117">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9c579-117">The sync group name.</span></span>

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

### <span data-ttu-id="9c579-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c579-118">-ResourceGroupName</span></span>
<span data-ttu-id="9c579-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c579-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="9c579-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9c579-120">-ServerName</span></span>
<span data-ttu-id="9c579-121">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9c579-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9c579-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c579-122">-DefaultProfile</span></span>
<span data-ttu-id="9c579-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c579-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c579-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c579-124">CommonParameters</span></span>
<span data-ttu-id="9c579-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c579-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c579-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c579-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c579-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c579-127">INPUTS</span></span>

## <span data-ttu-id="9c579-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c579-128">OUTPUTS</span></span>

### <span data-ttu-id="9c579-129">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="9c579-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="9c579-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c579-130">NOTES</span></span>

## <span data-ttu-id="9c579-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c579-131">RELATED LINKS</span></span>

[<span data-ttu-id="9c579-132">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9c579-132">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="9c579-133">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9c579-133">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="9c579-134">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9c579-134">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

