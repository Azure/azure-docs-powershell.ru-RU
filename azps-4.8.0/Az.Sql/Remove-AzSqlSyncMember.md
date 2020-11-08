---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080231"
---
# <span data-ttu-id="f78db-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f78db-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="f78db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f78db-102">SYNOPSIS</span></span>
<span data-ttu-id="f78db-103">Удаляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f78db-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f78db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f78db-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f78db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f78db-105">DESCRIPTION</span></span>
<span data-ttu-id="f78db-106">Командлет **Remove-AzSqlSyncMember** удаляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f78db-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f78db-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f78db-107">EXAMPLES</span></span>

### <span data-ttu-id="f78db-108">Пример 1: Удаление члена синхронизации</span><span class="sxs-lookup"><span data-stu-id="f78db-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="f78db-109">Эта команда удаляет член синхронизации базы данных SQL Azure с именем syncMember01.</span><span class="sxs-lookup"><span data-stu-id="f78db-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="f78db-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f78db-110">PARAMETERS</span></span>

### <span data-ttu-id="f78db-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f78db-111">-DatabaseName</span></span>
<span data-ttu-id="f78db-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f78db-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f78db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78db-113">-DefaultProfile</span></span>
<span data-ttu-id="f78db-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f78db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f78db-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f78db-115">-Force</span></span>
<span data-ttu-id="f78db-116">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="f78db-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f78db-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f78db-117">-Name</span></span>
<span data-ttu-id="f78db-118">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f78db-118">The sync member name.</span></span>

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

### <span data-ttu-id="f78db-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f78db-119">-PassThru</span></span>
<span data-ttu-id="f78db-120">Определяет, возвращают ли удаленный элемент синхронизации</span><span class="sxs-lookup"><span data-stu-id="f78db-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="f78db-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f78db-121">-ResourceGroupName</span></span>
<span data-ttu-id="f78db-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f78db-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f78db-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f78db-123">-ServerName</span></span>
<span data-ttu-id="f78db-124">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f78db-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f78db-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f78db-125">-SyncGroupName</span></span>
<span data-ttu-id="f78db-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f78db-126">The sync group name.</span></span>

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

### <span data-ttu-id="f78db-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f78db-127">-Confirm</span></span>
<span data-ttu-id="f78db-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f78db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f78db-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f78db-129">-WhatIf</span></span>
<span data-ttu-id="f78db-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f78db-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f78db-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f78db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f78db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78db-132">CommonParameters</span></span>
<span data-ttu-id="f78db-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f78db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78db-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f78db-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78db-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f78db-135">INPUTS</span></span>

### <span data-ttu-id="f78db-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f78db-136">System.String</span></span>

## <span data-ttu-id="f78db-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f78db-137">OUTPUTS</span></span>

### <span data-ttu-id="f78db-138">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="f78db-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="f78db-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="f78db-139">NOTES</span></span>

## <span data-ttu-id="f78db-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f78db-140">RELATED LINKS</span></span>

[<span data-ttu-id="f78db-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f78db-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="f78db-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f78db-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="f78db-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f78db-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

