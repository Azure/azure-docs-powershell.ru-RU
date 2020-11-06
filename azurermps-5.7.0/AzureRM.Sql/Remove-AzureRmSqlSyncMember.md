---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: b96d125b2a4f608c54024619ca6259a136d2ed69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561384"
---
# <span data-ttu-id="e50d5-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e50d5-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="e50d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e50d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e50d5-103">Удаляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e50d5-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e50d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e50d5-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e50d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e50d5-105">DESCRIPTION</span></span>
<span data-ttu-id="e50d5-106">Командлет **Remove-AzureRmSqlSyncMember** удаляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e50d5-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e50d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e50d5-107">EXAMPLES</span></span>

### <span data-ttu-id="e50d5-108">Пример 1: Удаление члена синхронизации</span><span class="sxs-lookup"><span data-stu-id="e50d5-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="e50d5-109">Эта команда удаляет член синхронизации базы данных SQL Azure с именем syncMember01.</span><span class="sxs-lookup"><span data-stu-id="e50d5-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="e50d5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e50d5-110">PARAMETERS</span></span>

### <span data-ttu-id="e50d5-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e50d5-111">-DatabaseName</span></span>
<span data-ttu-id="e50d5-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e50d5-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50d5-113">-DefaultProfile</span></span>
<span data-ttu-id="e50d5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e50d5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e50d5-115">-Force</span></span>
<span data-ttu-id="e50d5-116">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="e50d5-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e50d5-117">-Name</span></span>
<span data-ttu-id="e50d5-118">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e50d5-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e50d5-119">-PassThru</span></span>
<span data-ttu-id="e50d5-120">Определяет, возвращают ли удаленный элемент синхронизации</span><span class="sxs-lookup"><span data-stu-id="e50d5-120">Defines Whether return the removed sync member</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e50d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="e50d5-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e50d5-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e50d5-123">-ServerName</span></span>
<span data-ttu-id="e50d5-124">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e50d5-124">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e50d5-125">-SyncGroupName</span></span>
<span data-ttu-id="e50d5-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e50d5-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e50d5-127">-Confirm</span></span>
<span data-ttu-id="e50d5-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e50d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50d5-129">-WhatIf</span></span>
<span data-ttu-id="e50d5-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e50d5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e50d5-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e50d5-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50d5-132">CommonParameters</span></span>
<span data-ttu-id="e50d5-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e50d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50d5-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50d5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50d5-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e50d5-135">INPUTS</span></span>

### <span data-ttu-id="e50d5-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="e50d5-136">None</span></span>
<span data-ttu-id="e50d5-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e50d5-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e50d5-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e50d5-138">OUTPUTS</span></span>

### <span data-ttu-id="e50d5-139">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="e50d5-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="e50d5-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e50d5-140">NOTES</span></span>

## <span data-ttu-id="e50d5-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e50d5-141">RELATED LINKS</span></span>

[<span data-ttu-id="e50d5-142">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e50d5-142">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="e50d5-143">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e50d5-143">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="e50d5-144">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e50d5-144">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

