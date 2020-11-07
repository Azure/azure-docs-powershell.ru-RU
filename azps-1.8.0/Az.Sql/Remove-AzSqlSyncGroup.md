---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 0010dad985755512e97aaccb14540ec16dc47cab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728819"
---
# <span data-ttu-id="0c388-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0c388-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="0c388-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c388-102">SYNOPSIS</span></span>
<span data-ttu-id="0c388-103">Удаляет группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0c388-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0c388-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c388-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c388-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c388-105">DESCRIPTION</span></span>
<span data-ttu-id="0c388-106">Командлет **Remove-AzSqlSyncGroup** удаляет группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0c388-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0c388-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c388-107">EXAMPLES</span></span>

### <span data-ttu-id="0c388-108">Пример 1: Удаление группы синхронизации</span><span class="sxs-lookup"><span data-stu-id="0c388-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="0c388-109">Эта команда удаляет группу синхронизации базы данных SQL Azure с именем syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="0c388-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="0c388-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c388-110">PARAMETERS</span></span>

### <span data-ttu-id="0c388-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c388-111">-DatabaseName</span></span>
<span data-ttu-id="0c388-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0c388-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0c388-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c388-113">-DefaultProfile</span></span>
<span data-ttu-id="0c388-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0c388-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c388-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0c388-115">-Force</span></span>
<span data-ttu-id="0c388-116">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="0c388-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0c388-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c388-117">-Name</span></span>
<span data-ttu-id="0c388-118">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0c388-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c388-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c388-119">-PassThru</span></span>
<span data-ttu-id="0c388-120">Определяет, возвращают ли удаленную группу синхронизации</span><span class="sxs-lookup"><span data-stu-id="0c388-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="0c388-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c388-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c388-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c388-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c388-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0c388-123">-ServerName</span></span>
<span data-ttu-id="0c388-124">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0c388-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0c388-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c388-125">-Confirm</span></span>
<span data-ttu-id="0c388-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c388-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c388-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c388-127">-WhatIf</span></span>
<span data-ttu-id="0c388-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c388-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c388-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c388-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c388-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c388-130">CommonParameters</span></span>
<span data-ttu-id="0c388-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c388-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c388-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c388-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c388-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c388-133">INPUTS</span></span>

### <span data-ttu-id="0c388-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0c388-134">System.String</span></span>

## <span data-ttu-id="0c388-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c388-135">OUTPUTS</span></span>

### <span data-ttu-id="0c388-136">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="0c388-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="0c388-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c388-137">NOTES</span></span>

## <span data-ttu-id="0c388-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c388-138">RELATED LINKS</span></span>

[<span data-ttu-id="0c388-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0c388-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="0c388-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0c388-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="0c388-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0c388-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

