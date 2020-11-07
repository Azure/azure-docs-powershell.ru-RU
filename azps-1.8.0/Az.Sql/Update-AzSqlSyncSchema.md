---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: b5a0a09986be3856db4ab65f9dc411e6940ffb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728712"
---
# <span data-ttu-id="88623-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="88623-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="88623-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88623-102">SYNOPSIS</span></span>
<span data-ttu-id="88623-103">Обновите схему синхронизации для базы данных участника синхронизации или базы данных концентратора синхронизации.</span><span class="sxs-lookup"><span data-stu-id="88623-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="88623-104">Она будет получать последнюю схему базы данных из реальной базы данных, а затем использовать ее для обновления схемы, кэшированной с помощью базы данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="88623-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="88623-105">Если задано значение "SyncMemberName", будет обновлена схема базы данных участника; в противном случае будет обновлена схема базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="88623-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="88623-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88623-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88623-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88623-107">DESCRIPTION</span></span>
<span data-ttu-id="88623-108">Командлет **Update-AzSqlSyncSchema** обновляет схему синхронизации для базы данных участника синхронизации или базы данных концентратора синхронизации.</span><span class="sxs-lookup"><span data-stu-id="88623-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="88623-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88623-109">EXAMPLES</span></span>

### <span data-ttu-id="88623-110">Пример 1: обновление схемы синхронизации для базы данных-концентратора</span><span class="sxs-lookup"><span data-stu-id="88623-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="88623-111">Эта команда обновляет схему синхронизации для базы данных Hub в группе "Синхронизация" syncGroup01</span><span class="sxs-lookup"><span data-stu-id="88623-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="88623-112">Пример 2: обновление схемы синхронизации для базы данных участника</span><span class="sxs-lookup"><span data-stu-id="88623-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="88623-113">Эта команда обновляет схему синхронизации для базы данных пользователей в элементе Sync syncMember01</span><span class="sxs-lookup"><span data-stu-id="88623-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="88623-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88623-114">PARAMETERS</span></span>

### <span data-ttu-id="88623-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88623-115">-DatabaseName</span></span>
<span data-ttu-id="88623-116">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="88623-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="88623-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88623-117">-DefaultProfile</span></span>
<span data-ttu-id="88623-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="88623-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88623-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88623-119">-PassThru</span></span>
<span data-ttu-id="88623-120">Определяет, будет ли возвращена группа синхронизации, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88623-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="88623-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88623-121">-ResourceGroupName</span></span>
<span data-ttu-id="88623-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88623-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="88623-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="88623-123">-ServerName</span></span>
<span data-ttu-id="88623-124">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88623-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="88623-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="88623-125">-SyncGroupName</span></span>
<span data-ttu-id="88623-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="88623-126">The sync group name.</span></span>

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

### <span data-ttu-id="88623-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="88623-127">-SyncMemberName</span></span>
<span data-ttu-id="88623-128">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="88623-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88623-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88623-129">-Confirm</span></span>
<span data-ttu-id="88623-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88623-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88623-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88623-131">-WhatIf</span></span>
<span data-ttu-id="88623-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88623-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88623-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88623-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88623-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88623-134">CommonParameters</span></span>
<span data-ttu-id="88623-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88623-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88623-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88623-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88623-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88623-137">INPUTS</span></span>

### <span data-ttu-id="88623-138">System. String</span><span class="sxs-lookup"><span data-stu-id="88623-138">System.String</span></span>

## <span data-ttu-id="88623-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88623-139">OUTPUTS</span></span>

### <span data-ttu-id="88623-140">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="88623-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="88623-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="88623-141">NOTES</span></span>

## <span data-ttu-id="88623-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88623-142">RELATED LINKS</span></span>
