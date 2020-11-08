---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: 08192eb96b7c0a2dde84a51cf49f3b96e5429ffc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2020
ms.locfileid: "94245128"
---
# <span data-ttu-id="96684-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="96684-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="96684-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96684-102">SYNOPSIS</span></span>
<span data-ttu-id="96684-103">Выполняет отработку отказа группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="96684-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="96684-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96684-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96684-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96684-105">DESCRIPTION</span></span>
<span data-ttu-id="96684-106">Эта команда меняет местами роли серверов в группе отработки отказа и переключает все базы данных-получатели на основную роль.</span><span class="sxs-lookup"><span data-stu-id="96684-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="96684-107">Все новые сеансы TDS автоматически перенаправляются на дополнительный сервер после обновления кэша DNS-клиента.</span><span class="sxs-lookup"><span data-stu-id="96684-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="96684-108">После возвращения исходного основного сервера в сети все ранее базы данных-источники будут переключаться на эту роль.</span><span class="sxs-lookup"><span data-stu-id="96684-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="96684-109">Для выполнения этой команды необходимо использовать сервер-получатель группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="96684-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="96684-110">Если параметр AllowDataLoss не указан, эта команда ожидает, пока обе роли не будут переключены.</span><span class="sxs-lookup"><span data-stu-id="96684-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="96684-111">Если указан параметр AllowDataLoss, команда ждет, пока новая основная роль не станет ее ролью.</span><span class="sxs-lookup"><span data-stu-id="96684-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="96684-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96684-112">EXAMPLES</span></span>

### <span data-ttu-id="96684-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96684-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="96684-114">Выпустить операцию отработки отказа, которая позволяет по конвейеру потерять данные в группе отказоустойчивости.</span><span class="sxs-lookup"><span data-stu-id="96684-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="96684-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="96684-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="96684-116">Выдайте наиболее фиксированную операцию отработки отказа, которая будет выполнена успешно без потери данных или отката.</span><span class="sxs-lookup"><span data-stu-id="96684-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="96684-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96684-117">PARAMETERS</span></span>

### <span data-ttu-id="96684-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="96684-118">-AllowDataLoss</span></span>
<span data-ttu-id="96684-119">Завершение отработки отказа, даже если это может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="96684-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="96684-120">Это позволит продолжить отработку отказа, даже если база данных-источник недоступна.</span><span class="sxs-lookup"><span data-stu-id="96684-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="96684-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96684-121">-AsJob</span></span>
<span data-ttu-id="96684-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="96684-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96684-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96684-123">-DefaultProfile</span></span>
<span data-ttu-id="96684-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="96684-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96684-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="96684-125">-FailoverGroupName</span></span>
<span data-ttu-id="96684-126">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="96684-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="96684-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96684-127">-ResourceGroupName</span></span>
<span data-ttu-id="96684-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96684-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="96684-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="96684-129">-ServerName</span></span>
<span data-ttu-id="96684-130">Имя дополнительного сервера базы данных SQL Azure для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="96684-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="96684-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96684-131">-Confirm</span></span>
<span data-ttu-id="96684-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96684-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96684-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96684-133">-WhatIf</span></span>
<span data-ttu-id="96684-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96684-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96684-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96684-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96684-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96684-136">CommonParameters</span></span>
<span data-ttu-id="96684-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96684-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96684-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96684-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96684-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96684-139">INPUTS</span></span>

### <span data-ttu-id="96684-140">System. String</span><span class="sxs-lookup"><span data-stu-id="96684-140">System.String</span></span>

## <span data-ttu-id="96684-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96684-141">OUTPUTS</span></span>

### <span data-ttu-id="96684-142">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="96684-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="96684-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="96684-143">NOTES</span></span>

## <span data-ttu-id="96684-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96684-144">RELATED LINKS</span></span>

[<span data-ttu-id="96684-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="96684-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="96684-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="96684-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="96684-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="96684-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="96684-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="96684-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="96684-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="96684-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="96684-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="96684-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="96684-151">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="96684-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
