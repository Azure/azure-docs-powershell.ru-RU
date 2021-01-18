---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506422"
---
# <span data-ttu-id="3829e-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="3829e-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="3829e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3829e-102">SYNOPSIS</span></span>
<span data-ttu-id="3829e-103">Остановка синхронизации группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3829e-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="3829e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3829e-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3829e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3829e-105">DESCRIPTION</span></span>
<span data-ttu-id="3829e-106">Команда **stop-AzSqlSyncGroupSync** останавливает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3829e-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="3829e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3829e-107">EXAMPLES</span></span>

### <span data-ttu-id="3829e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3829e-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="3829e-109">Эта команда останавливает синхронизацию, которая продолжается для группы синхронизации mysg.</span><span class="sxs-lookup"><span data-stu-id="3829e-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="3829e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3829e-110">PARAMETERS</span></span>

### <span data-ttu-id="3829e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3829e-111">-DatabaseName</span></span>
<span data-ttu-id="3829e-112">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3829e-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3829e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3829e-113">-DefaultProfile</span></span>
<span data-ttu-id="3829e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3829e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3829e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3829e-115">-PassThru</span></span>
<span data-ttu-id="3829e-116">Определяет, возвращает ли группа синхронизации</span><span class="sxs-lookup"><span data-stu-id="3829e-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="3829e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3829e-117">-ResourceGroupName</span></span>
<span data-ttu-id="3829e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3829e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3829e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3829e-119">-ServerName</span></span>
<span data-ttu-id="3829e-120">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3829e-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="3829e-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3829e-121">-SyncGroupName</span></span>
<span data-ttu-id="3829e-122">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3829e-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3829e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3829e-123">-Confirm</span></span>
<span data-ttu-id="3829e-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3829e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3829e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3829e-125">-WhatIf</span></span>
<span data-ttu-id="3829e-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3829e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3829e-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3829e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3829e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3829e-128">CommonParameters</span></span>
<span data-ttu-id="3829e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3829e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3829e-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3829e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3829e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3829e-131">INPUTS</span></span>

### <span data-ttu-id="3829e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3829e-132">System.String</span></span>

## <span data-ttu-id="3829e-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3829e-133">OUTPUTS</span></span>

### <span data-ttu-id="3829e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="3829e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="3829e-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3829e-135">NOTES</span></span>

## <span data-ttu-id="3829e-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3829e-136">RELATED LINKS</span></span>

[<span data-ttu-id="3829e-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="3829e-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

