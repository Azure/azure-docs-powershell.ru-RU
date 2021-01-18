---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506421"
---
# <span data-ttu-id="94b1b-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="94b1b-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="94b1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="94b1b-103">Выполняет отбой для группы отбойных данных Azure SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="94b1b-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="94b1b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94b1b-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94b1b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="94b1b-106">Эта команда меняет роли серверов в группе отключении и переключает все дополнительные базы данных на главную роль.</span><span class="sxs-lookup"><span data-stu-id="94b1b-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="94b1b-107">Все новые сеансы TDS автоматически перена маршрутизируются на дополнительный сервер после обновления кэша клиента DNS.</span><span class="sxs-lookup"><span data-stu-id="94b1b-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="94b1b-108">Когда исходный основной сервер снова станет в сети, все его основные базы данных будут переключения на вторичную роль.</span><span class="sxs-lookup"><span data-stu-id="94b1b-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="94b1b-109">Для выполнения этой команды необходимо использовать дополнительный сервер группы отбойных серверов.</span><span class="sxs-lookup"><span data-stu-id="94b1b-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="94b1b-110">Если параметр AllowDataLoss не указан, эта команда будет ждать переключения обеих ролей.</span><span class="sxs-lookup"><span data-stu-id="94b1b-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="94b1b-111">Если задан параметр AllowDataLoss, команда будет ждать, пока новый основной не будет считаться его ролью.</span><span class="sxs-lookup"><span data-stu-id="94b1b-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="94b1b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94b1b-112">EXAMPLES</span></span>

### <span data-ttu-id="94b1b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94b1b-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="94b1b-114">Выдайте отбой, разрешив потерю данных путем перенаправки в группу отбойных передач.</span><span class="sxs-lookup"><span data-stu-id="94b1b-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="94b1b-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94b1b-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="94b1b-116">Вы можете сделать откат наилучшего действия успешным без потери данных или сбойных и откатов.</span><span class="sxs-lookup"><span data-stu-id="94b1b-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="94b1b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94b1b-117">PARAMETERS</span></span>

### <span data-ttu-id="94b1b-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="94b1b-118">-AllowDataLoss</span></span>
<span data-ttu-id="94b1b-119">Завершите отбой, даже если это приведет к потере данных.</span><span class="sxs-lookup"><span data-stu-id="94b1b-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="94b1b-120">Это позволит продолжить отбой, даже если основная база данных недоступна.</span><span class="sxs-lookup"><span data-stu-id="94b1b-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b1b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94b1b-121">-AsJob</span></span>
<span data-ttu-id="94b1b-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="94b1b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94b1b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b1b-123">-DefaultProfile</span></span>
<span data-ttu-id="94b1b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94b1b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94b1b-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="94b1b-125">-FailoverGroupName</span></span>
<span data-ttu-id="94b1b-126">Имя группы отбойного SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="94b1b-126">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94b1b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b1b-127">-ResourceGroupName</span></span>
<span data-ttu-id="94b1b-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94b1b-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="94b1b-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="94b1b-129">-ServerName</span></span>
<span data-ttu-id="94b1b-130">Имя дополнительного сервера баз данных Azure SQL группы failover.</span><span class="sxs-lookup"><span data-stu-id="94b1b-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="94b1b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94b1b-131">-Confirm</span></span>
<span data-ttu-id="94b1b-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="94b1b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b1b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b1b-133">-WhatIf</span></span>
<span data-ttu-id="94b1b-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94b1b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94b1b-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94b1b-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b1b-136">CommonParameters</span></span>
<span data-ttu-id="94b1b-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b1b-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94b1b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b1b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94b1b-139">INPUTS</span></span>

### <span data-ttu-id="94b1b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="94b1b-140">System.String</span></span>

## <span data-ttu-id="94b1b-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94b1b-141">OUTPUTS</span></span>

### <span data-ttu-id="94b1b-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="94b1b-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="94b1b-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94b1b-143">NOTES</span></span>

## <span data-ttu-id="94b1b-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94b1b-144">RELATED LINKS</span></span>

[<span data-ttu-id="94b1b-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="94b1b-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="94b1b-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="94b1b-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="94b1b-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="94b1b-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="94b1b-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="94b1b-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="94b1b-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="94b1b-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="94b1b-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="94b1b-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="94b1b-151">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="94b1b-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
