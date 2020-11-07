---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 76b7366dabc648dc7f5812aedcc7fef18437b68e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728713"
---
# <span data-ttu-id="800a3-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="800a3-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="800a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="800a3-102">SYNOPSIS</span></span>
<span data-ttu-id="800a3-103">Обновляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="800a3-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="800a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="800a3-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="800a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="800a3-105">DESCRIPTION</span></span>
<span data-ttu-id="800a3-106">Командлет **Update-AzSqlSyncGroup** изменяет свойства члена синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="800a3-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="800a3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="800a3-107">EXAMPLES</span></span>

### <span data-ttu-id="800a3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="800a3-108">Example 1</span></span>
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

<span data-ttu-id="800a3-109">Эта команда сбрасывает пароль администратора для базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="800a3-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="800a3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="800a3-110">PARAMETERS</span></span>

### <span data-ttu-id="800a3-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="800a3-111">-DatabaseName</span></span>
<span data-ttu-id="800a3-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="800a3-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="800a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800a3-113">-DefaultProfile</span></span>
<span data-ttu-id="800a3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="800a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="800a3-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="800a3-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="800a3-116">Учетные данные (имя пользователя и пароль) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="800a3-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800a3-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="800a3-117">-Name</span></span>
<span data-ttu-id="800a3-118">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="800a3-118">The sync member name.</span></span>

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

### <span data-ttu-id="800a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="800a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="800a3-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="800a3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="800a3-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="800a3-121">-ServerName</span></span>
<span data-ttu-id="800a3-122">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="800a3-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="800a3-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="800a3-123">-SyncGroupName</span></span>
<span data-ttu-id="800a3-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="800a3-124">The sync group name.</span></span>

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

### <span data-ttu-id="800a3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="800a3-125">-Confirm</span></span>
<span data-ttu-id="800a3-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="800a3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="800a3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800a3-127">-WhatIf</span></span>
<span data-ttu-id="800a3-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="800a3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="800a3-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="800a3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="800a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800a3-130">CommonParameters</span></span>
<span data-ttu-id="800a3-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="800a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800a3-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="800a3-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800a3-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="800a3-133">INPUTS</span></span>

### <span data-ttu-id="800a3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="800a3-134">System.String</span></span>

## <span data-ttu-id="800a3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="800a3-135">OUTPUTS</span></span>

### <span data-ttu-id="800a3-136">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="800a3-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="800a3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="800a3-137">NOTES</span></span>

## <span data-ttu-id="800a3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="800a3-138">RELATED LINKS</span></span>

[<span data-ttu-id="800a3-139">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="800a3-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="800a3-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="800a3-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="800a3-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="800a3-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

