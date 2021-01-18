---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506415"
---
# <span data-ttu-id="f2fa7-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="f2fa7-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="f2fa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="f2fa7-103">Обновив схему синхронизации для базы данных ее участника или концентратора синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="f2fa7-104">Он получит последнюю схему базы данных из настоящей базы данных, а затем будет использовать ее для обновления схемы, кэш которой используется в базе данных синхронизации метаданных.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="f2fa7-105">Если задана команда SyncMemberName, будет обновлена схема базы данных участника. Если нет, будет обновлена схема базы данных концентратора.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="f2fa7-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2fa7-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2fa7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2fa7-107">DESCRIPTION</span></span>
<span data-ttu-id="f2fa7-108">Командалет **Update-AzSqlSyncSchema** обновляет схему синхронизации для базы данных ее участника или концентратора синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="f2fa7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2fa7-109">EXAMPLES</span></span>

### <span data-ttu-id="f2fa7-110">Пример 1. Обновление схемы синхронизации для базы данных концентратора</span><span class="sxs-lookup"><span data-stu-id="f2fa7-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="f2fa7-111">Эта команда обновляет схему синхронизации центральной базы данных в группе синхронизацииGroup01.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="f2fa7-112">Пример 2. Обновление схемы синхронизации для базы данных участника</span><span class="sxs-lookup"><span data-stu-id="f2fa7-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="f2fa7-113">Эта команда обновляет схему синхронизации для базы данных ее членов в syncMember01.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="f2fa7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2fa7-114">PARAMETERS</span></span>

### <span data-ttu-id="f2fa7-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2fa7-115">-DatabaseName</span></span>
<span data-ttu-id="f2fa7-116">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f2fa7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2fa7-117">-DefaultProfile</span></span>
<span data-ttu-id="f2fa7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f2fa7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2fa7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2fa7-119">-PassThru</span></span>
<span data-ttu-id="f2fa7-120">Определяет, возвращает ли эта группа синхронизации, с</span><span class="sxs-lookup"><span data-stu-id="f2fa7-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="f2fa7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2fa7-121">-ResourceGroupName</span></span>
<span data-ttu-id="f2fa7-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2fa7-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f2fa7-123">-ServerName</span></span>
<span data-ttu-id="f2fa7-124">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f2fa7-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f2fa7-125">-SyncGroupName</span></span>
<span data-ttu-id="f2fa7-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-126">The sync group name.</span></span>

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

### <span data-ttu-id="f2fa7-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="f2fa7-127">-SyncMemberName</span></span>
<span data-ttu-id="f2fa7-128">Имя участника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-128">The sync member name.</span></span>

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

### <span data-ttu-id="f2fa7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2fa7-129">-Confirm</span></span>
<span data-ttu-id="f2fa7-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2fa7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2fa7-131">-WhatIf</span></span>
<span data-ttu-id="f2fa7-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2fa7-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2fa7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2fa7-134">CommonParameters</span></span>
<span data-ttu-id="f2fa7-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2fa7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2fa7-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2fa7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2fa7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2fa7-137">INPUTS</span></span>

### <span data-ttu-id="f2fa7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f2fa7-138">System.String</span></span>

## <span data-ttu-id="f2fa7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2fa7-139">OUTPUTS</span></span>

### <span data-ttu-id="f2fa7-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="f2fa7-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="f2fa7-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2fa7-141">NOTES</span></span>

## <span data-ttu-id="f2fa7-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2fa7-142">RELATED LINKS</span></span>
