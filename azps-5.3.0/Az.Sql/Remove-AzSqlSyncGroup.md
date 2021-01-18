---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504774"
---
# <span data-ttu-id="da772-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="da772-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="da772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da772-102">SYNOPSIS</span></span>
<span data-ttu-id="da772-103">Удаляет группу синхронизации SQL баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="da772-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="da772-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da772-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da772-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da772-105">DESCRIPTION</span></span>
<span data-ttu-id="da772-106">При этом удаляется группа синхронизации базы данных Azure SQL **AzSqlSyncGroup.**</span><span class="sxs-lookup"><span data-stu-id="da772-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="da772-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da772-107">EXAMPLES</span></span>

### <span data-ttu-id="da772-108">Пример 1. Удаление группы синхронизации</span><span class="sxs-lookup"><span data-stu-id="da772-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="da772-109">Эта команда удаляет группу синхронизации баз данных Azure SQL с именем syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="da772-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="da772-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da772-110">PARAMETERS</span></span>

### <span data-ttu-id="da772-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da772-111">-DatabaseName</span></span>
<span data-ttu-id="da772-112">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="da772-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="da772-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da772-113">-DefaultProfile</span></span>
<span data-ttu-id="da772-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="da772-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da772-115">-Force</span><span class="sxs-lookup"><span data-stu-id="da772-115">-Force</span></span>
<span data-ttu-id="da772-116">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="da772-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="da772-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da772-117">-Name</span></span>
<span data-ttu-id="da772-118">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="da772-118">The sync group name.</span></span>

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

### <span data-ttu-id="da772-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da772-119">-PassThru</span></span>
<span data-ttu-id="da772-120">Определяет, возвращает ли удаленная группа синхронизации</span><span class="sxs-lookup"><span data-stu-id="da772-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="da772-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da772-121">-ResourceGroupName</span></span>
<span data-ttu-id="da772-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da772-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="da772-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da772-123">-ServerName</span></span>
<span data-ttu-id="da772-124">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da772-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="da772-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da772-125">-Confirm</span></span>
<span data-ttu-id="da772-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da772-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da772-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da772-127">-WhatIf</span></span>
<span data-ttu-id="da772-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da772-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da772-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da772-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da772-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da772-130">CommonParameters</span></span>
<span data-ttu-id="da772-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da772-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da772-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da772-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da772-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da772-133">INPUTS</span></span>

### <span data-ttu-id="da772-134">System.String</span><span class="sxs-lookup"><span data-stu-id="da772-134">System.String</span></span>

## <span data-ttu-id="da772-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da772-135">OUTPUTS</span></span>

### <span data-ttu-id="da772-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="da772-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="da772-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da772-137">NOTES</span></span>

## <span data-ttu-id="da772-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da772-138">RELATED LINKS</span></span>

[<span data-ttu-id="da772-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="da772-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="da772-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="da772-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="da772-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="da772-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

