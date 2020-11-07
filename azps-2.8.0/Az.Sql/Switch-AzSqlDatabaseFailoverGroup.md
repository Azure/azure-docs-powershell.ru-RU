---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 15b0026158f3942ffbb9ff1d426104cffcb18a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906890"
---
# <span data-ttu-id="ae0c2-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ae0c2-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="ae0c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0c2-103">Выполняет отработку отказа группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="ae0c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae0c2-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae0c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae0c2-105">DESCRIPTION</span></span>
<span data-ttu-id="ae0c2-106">Эта команда меняет местами роли серверов в группе отработки отказа и переключает все базы данных-получатели на основную роль.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="ae0c2-107">Все новые сеансы TDS автоматически перенаправляются на дополнительный сервер после обновления кэша DNS-клиента.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="ae0c2-108">После возвращения исходного основного сервера в сети все ранее базы данных-источники будут переключаться на эту роль.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="ae0c2-109">Для выполнения этой команды необходимо использовать сервер-получатель группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="ae0c2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae0c2-110">EXAMPLES</span></span>

### <span data-ttu-id="ae0c2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae0c2-111">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="ae0c2-112">Выпустить операцию отработки отказа, которая позволяет по конвейеру потерять данные в группе отказоустойчивости.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="ae0c2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ae0c2-113">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="ae0c2-114">Выдайте наиболее фиксированную операцию отработки отказа, которая будет выполнена успешно без потери данных или отката.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="ae0c2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae0c2-115">PARAMETERS</span></span>

### <span data-ttu-id="ae0c2-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="ae0c2-116">-AllowDataLoss</span></span>
<span data-ttu-id="ae0c2-117">Завершение отработки отказа, даже если это может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="ae0c2-118">Это позволит продолжить отработку отказа, даже если база данных-источник недоступна.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="ae0c2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae0c2-119">-AsJob</span></span>
<span data-ttu-id="ae0c2-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ae0c2-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae0c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0c2-121">-DefaultProfile</span></span>
<span data-ttu-id="ae0c2-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ae0c2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae0c2-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ae0c2-123">-FailoverGroupName</span></span>
<span data-ttu-id="ae0c2-124">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="ae0c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae0c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae0c2-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ae0c2-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ae0c2-127">-ServerName</span></span>
<span data-ttu-id="ae0c2-128">Имя дополнительного сервера базы данных SQL Azure для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="ae0c2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae0c2-129">-Confirm</span></span>
<span data-ttu-id="ae0c2-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae0c2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae0c2-131">-WhatIf</span></span>
<span data-ttu-id="ae0c2-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae0c2-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae0c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0c2-134">CommonParameters</span></span>
<span data-ttu-id="ae0c2-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae0c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0c2-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae0c2-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0c2-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae0c2-137">INPUTS</span></span>

### <span data-ttu-id="ae0c2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ae0c2-138">System.String</span></span>

## <span data-ttu-id="ae0c2-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae0c2-139">OUTPUTS</span></span>

### <span data-ttu-id="ae0c2-140">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ae0c2-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="ae0c2-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae0c2-141">NOTES</span></span>

## <span data-ttu-id="ae0c2-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae0c2-142">RELATED LINKS</span></span>

[<span data-ttu-id="ae0c2-143">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ae0c2-143">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ae0c2-144">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ae0c2-144">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ae0c2-145">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ae0c2-145">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ae0c2-146">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ae0c2-146">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="ae0c2-147">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ae0c2-147">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="ae0c2-148">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ae0c2-148">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ae0c2-149">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="ae0c2-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
