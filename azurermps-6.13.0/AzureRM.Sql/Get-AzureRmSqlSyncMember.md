---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: 30a73047282508adc0c2aa0d0d64a61f9f70e71a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568140"
---
# <span data-ttu-id="51b72-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="51b72-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="51b72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51b72-102">SYNOPSIS</span></span>
<span data-ttu-id="51b72-103">Возвращает сведения о членах синхронизации базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="51b72-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51b72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51b72-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51b72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51b72-105">DESCRIPTION</span></span>
<span data-ttu-id="51b72-106">Командлет **Get-AzureRmSqlSyncMember** возвращает сведения об одном или нескольких членах синхронизации базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="51b72-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="51b72-107">Укажите имя члена синхронизации, чтобы просмотреть сведения только для этого члена синхронизации.</span><span class="sxs-lookup"><span data-stu-id="51b72-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="51b72-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51b72-108">EXAMPLES</span></span>

### <span data-ttu-id="51b72-109">Пример 1: получение всех экземпляров участника Azure SQL Sync, назначенного группе синхронизации</span><span class="sxs-lookup"><span data-stu-id="51b72-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="51b72-110">Эта команда получает сведения обо всех членах синхронизации базы данных SQL Azure, назначенных группе синхронизации SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="51b72-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="51b72-111">Пример 2: получение сведений об элементе синхронизации базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="51b72-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="51b72-112">Эта команда получает сведения о члене синхронизации базы данных SQL Azure с именем "SyncMember01".</span><span class="sxs-lookup"><span data-stu-id="51b72-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="51b72-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51b72-113">PARAMETERS</span></span>

### <span data-ttu-id="51b72-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="51b72-114">-DatabaseName</span></span>
<span data-ttu-id="51b72-115">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="51b72-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="51b72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b72-116">-DefaultProfile</span></span>
<span data-ttu-id="51b72-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="51b72-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51b72-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51b72-118">-Name</span></span>
<span data-ttu-id="51b72-119">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="51b72-119">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b72-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b72-120">-ResourceGroupName</span></span>
<span data-ttu-id="51b72-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51b72-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="51b72-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="51b72-122">-ServerName</span></span>
<span data-ttu-id="51b72-123">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="51b72-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="51b72-124">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="51b72-124">-SyncGroupName</span></span>
<span data-ttu-id="51b72-125">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="51b72-125">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b72-126">CommonParameters</span></span>
<span data-ttu-id="51b72-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51b72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b72-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b72-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b72-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51b72-129">INPUTS</span></span>

### <span data-ttu-id="51b72-130">System. String</span><span class="sxs-lookup"><span data-stu-id="51b72-130">System.String</span></span>

## <span data-ttu-id="51b72-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51b72-131">OUTPUTS</span></span>

### <span data-ttu-id="51b72-132">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="51b72-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="51b72-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="51b72-133">NOTES</span></span>

## <span data-ttu-id="51b72-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51b72-134">RELATED LINKS</span></span>

[<span data-ttu-id="51b72-135">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="51b72-135">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="51b72-136">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="51b72-136">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="51b72-137">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="51b72-137">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

