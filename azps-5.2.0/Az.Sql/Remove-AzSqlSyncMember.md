---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322675"
---
# <span data-ttu-id="2e9e2-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2e9e2-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="2e9e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9e2-103">Удаляет участник синхронизации базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="2e9e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e9e2-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e9e2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="2e9e2-106">При этом удаляется участник синхронизации базы данных Azure SQL **AzSqlSyncMember.**</span><span class="sxs-lookup"><span data-stu-id="2e9e2-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="2e9e2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="2e9e2-108">Пример 1. Удаление участника синхронизации</span><span class="sxs-lookup"><span data-stu-id="2e9e2-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="2e9e2-109">Эта команда удаляет участник синхронизации базы SQL Azure с именем syncMember01.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="2e9e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e9e2-110">PARAMETERS</span></span>

### <span data-ttu-id="2e9e2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2e9e2-111">-DatabaseName</span></span>
<span data-ttu-id="2e9e2-112">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2e9e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9e2-113">-DefaultProfile</span></span>
<span data-ttu-id="2e9e2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2e9e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e9e2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2e9e2-115">-Force</span></span>
<span data-ttu-id="2e9e2-116">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="2e9e2-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2e9e2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2e9e2-117">-Name</span></span>
<span data-ttu-id="2e9e2-118">Имя участника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-118">The sync member name.</span></span>

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

### <span data-ttu-id="2e9e2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e9e2-119">-PassThru</span></span>
<span data-ttu-id="2e9e2-120">Определяет, будет ли возвращен удаленный участник синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="2e9e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e9e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e9e2-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e9e2-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e9e2-123">-ServerName</span></span>
<span data-ttu-id="2e9e2-124">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2e9e2-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2e9e2-125">-SyncGroupName</span></span>
<span data-ttu-id="2e9e2-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-126">The sync group name.</span></span>

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

### <span data-ttu-id="2e9e2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e9e2-127">-Confirm</span></span>
<span data-ttu-id="2e9e2-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e9e2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e9e2-129">-WhatIf</span></span>
<span data-ttu-id="2e9e2-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e9e2-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e9e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9e2-132">CommonParameters</span></span>
<span data-ttu-id="2e9e2-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e9e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9e2-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e9e2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9e2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e9e2-135">INPUTS</span></span>

### <span data-ttu-id="2e9e2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2e9e2-136">System.String</span></span>

## <span data-ttu-id="2e9e2-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e9e2-137">OUTPUTS</span></span>

### <span data-ttu-id="2e9e2-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="2e9e2-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="2e9e2-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e9e2-139">NOTES</span></span>

## <span data-ttu-id="2e9e2-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e9e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="2e9e2-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2e9e2-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="2e9e2-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2e9e2-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="2e9e2-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2e9e2-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

