---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245179"
---
# <span data-ttu-id="553da-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="553da-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="553da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="553da-102">SYNOPSIS</span></span>
<span data-ttu-id="553da-103">Обновляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="553da-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="553da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="553da-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="553da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="553da-105">DESCRIPTION</span></span>
<span data-ttu-id="553da-106">Командлет **Update-AzSqlSyncGroup** изменяет свойства члена синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="553da-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="553da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="553da-107">EXAMPLES</span></span>

### <span data-ttu-id="553da-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="553da-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
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
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="553da-109">Эта команда сбрасывает пароль администратора для базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="553da-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="553da-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="553da-110">PARAMETERS</span></span>

### <span data-ttu-id="553da-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="553da-111">-DatabaseName</span></span>
<span data-ttu-id="553da-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="553da-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="553da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553da-113">-DefaultProfile</span></span>
<span data-ttu-id="553da-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="553da-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="553da-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="553da-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="553da-116">Учетные данные (имя пользователя и пароль) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="553da-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553da-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="553da-117">-Name</span></span>
<span data-ttu-id="553da-118">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="553da-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="553da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553da-119">-ResourceGroupName</span></span>
<span data-ttu-id="553da-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="553da-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="553da-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="553da-121">-ServerName</span></span>
<span data-ttu-id="553da-122">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="553da-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="553da-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="553da-123">-SyncGroupName</span></span>
<span data-ttu-id="553da-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="553da-124">The sync group name.</span></span>

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

### <span data-ttu-id="553da-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="553da-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="553da-126">Идентификатор ресурса для базы данных элемента синхронизации, который используется, если UsePrivateLinkConnection имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="553da-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="553da-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="553da-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="553da-128">Следует ли использовать частную ссылку при подключении к этому члену синхронизации.</span><span class="sxs-lookup"><span data-stu-id="553da-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553da-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="553da-129">-Confirm</span></span>
<span data-ttu-id="553da-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="553da-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="553da-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="553da-131">-WhatIf</span></span>
<span data-ttu-id="553da-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="553da-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="553da-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="553da-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="553da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553da-134">CommonParameters</span></span>
<span data-ttu-id="553da-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="553da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553da-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="553da-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553da-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="553da-137">INPUTS</span></span>

### <span data-ttu-id="553da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="553da-138">System.String</span></span>

## <span data-ttu-id="553da-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="553da-139">OUTPUTS</span></span>

### <span data-ttu-id="553da-140">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="553da-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="553da-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="553da-141">NOTES</span></span>

## <span data-ttu-id="553da-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="553da-142">RELATED LINKS</span></span>

[<span data-ttu-id="553da-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="553da-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="553da-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="553da-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="553da-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="553da-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

