---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 34db2f2307d60f1653b0a806350d96fa9e3380af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905941"
---
# <span data-ttu-id="bfaa7-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bfaa7-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="bfaa7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfaa7-102">SYNOPSIS</span></span>
<span data-ttu-id="bfaa7-103">Удаляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="bfaa7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfaa7-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfaa7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfaa7-105">DESCRIPTION</span></span>
<span data-ttu-id="bfaa7-106">Командлет **Remove-AzSqlSyncMember** удаляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="bfaa7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfaa7-107">EXAMPLES</span></span>

### <span data-ttu-id="bfaa7-108">Пример 1: Удаление члена синхронизации</span><span class="sxs-lookup"><span data-stu-id="bfaa7-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="bfaa7-109">Эта команда удаляет член синхронизации базы данных SQL Azure с именем syncMember01.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="bfaa7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfaa7-110">PARAMETERS</span></span>

### <span data-ttu-id="bfaa7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bfaa7-111">-DatabaseName</span></span>
<span data-ttu-id="bfaa7-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="bfaa7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfaa7-113">-DefaultProfile</span></span>
<span data-ttu-id="bfaa7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bfaa7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfaa7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bfaa7-115">-Force</span></span>
<span data-ttu-id="bfaa7-116">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="bfaa7-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bfaa7-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfaa7-117">-Name</span></span>
<span data-ttu-id="bfaa7-118">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-118">The sync member name.</span></span>

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

### <span data-ttu-id="bfaa7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfaa7-119">-PassThru</span></span>
<span data-ttu-id="bfaa7-120">Определяет, возвращают ли удаленный элемент синхронизации</span><span class="sxs-lookup"><span data-stu-id="bfaa7-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="bfaa7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfaa7-121">-ResourceGroupName</span></span>
<span data-ttu-id="bfaa7-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="bfaa7-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bfaa7-123">-ServerName</span></span>
<span data-ttu-id="bfaa7-124">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="bfaa7-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bfaa7-125">-SyncGroupName</span></span>
<span data-ttu-id="bfaa7-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-126">The sync group name.</span></span>

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

### <span data-ttu-id="bfaa7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfaa7-127">-Confirm</span></span>
<span data-ttu-id="bfaa7-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfaa7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfaa7-129">-WhatIf</span></span>
<span data-ttu-id="bfaa7-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfaa7-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfaa7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfaa7-132">CommonParameters</span></span>
<span data-ttu-id="bfaa7-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfaa7-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfaa7-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfaa7-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfaa7-135">INPUTS</span></span>

### <span data-ttu-id="bfaa7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bfaa7-136">System.String</span></span>

## <span data-ttu-id="bfaa7-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfaa7-137">OUTPUTS</span></span>

### <span data-ttu-id="bfaa7-138">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="bfaa7-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="bfaa7-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfaa7-139">NOTES</span></span>

## <span data-ttu-id="bfaa7-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfaa7-140">RELATED LINKS</span></span>

[<span data-ttu-id="bfaa7-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bfaa7-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="bfaa7-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bfaa7-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="bfaa7-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bfaa7-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

