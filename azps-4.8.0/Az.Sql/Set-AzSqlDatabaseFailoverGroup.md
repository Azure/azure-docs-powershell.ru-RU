---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 825d6f367fb4fbace53fccdb8798d17a915fc2bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243892"
---
# <span data-ttu-id="dd2e4-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd2e4-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="dd2e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd2e4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2e4-103">Изменяет конфигурацию группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="dd2e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd2e4-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd2e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd2e4-105">DESCRIPTION</span></span>
<span data-ttu-id="dd2e4-106">Эта команда изменяет конфигурацию группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="dd2e4-107">Для выполнения команды следует использовать основной сервер группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="dd2e4-108">Для управления набором баз данных в группе используйте команды "Add-AzSqlDatabaseToFailoverGroup" и "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="dd2e4-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="dd2e4-109">Во время предварительного просмотра компонента "группы отработки отказа" для параметра "-GracePeriodWithDataLossHours" поддерживаются только значения, превышающие или равные 1 часу.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="dd2e4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd2e4-110">EXAMPLES</span></span>

### <span data-ttu-id="dd2e4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd2e4-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="dd2e4-112">Задает для политики отработки отказа отказоустойчивой группы значение "Авто".</span><span class="sxs-lookup"><span data-stu-id="dd2e4-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="dd2e4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dd2e4-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="dd2e4-114">Задает для политики отработки отказа отказоустойчивой группы значение "вручную" по конвейеру в группе отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="dd2e4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd2e4-115">PARAMETERS</span></span>

### <span data-ttu-id="dd2e4-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="dd2e4-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="dd2e4-117">Следует ли запускать автоматический переход с конечной точки только для чтения на сервере-получателе.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="dd2e4-118">Эта функция пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-118">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2e4-119">-DefaultProfile</span></span>
<span data-ttu-id="dd2e4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd2e4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd2e4-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2e4-121">-FailoverGroupName</span></span>
<span data-ttu-id="dd2e4-122">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="dd2e4-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="dd2e4-123">-FailoverPolicy</span></span>
<span data-ttu-id="dd2e4-124">Политика перемещения при сбое для группы Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2e4-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="dd2e4-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="dd2e4-126">Интервал перед автоматическим переходом на другой ресурс инициируется при возникновении сбоя на основном сервере.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="dd2e4-127">Это означает, что база данных Azure SQL не будет инициировать автоматический переход на другой ресурс до истечения льготного периода.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="dd2e4-128">Обратите внимание, что операция отработки отказа с помощью параметра AllowDataLoss может привести к потере данных из-за природы асинхронной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2e4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2e4-129">-ResourceGroupName</span></span>
<span data-ttu-id="dd2e4-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd2e4-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="dd2e4-131">-ServerName</span></span>
<span data-ttu-id="dd2e4-132">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="dd2e4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2e4-133">CommonParameters</span></span>
<span data-ttu-id="dd2e4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd2e4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2e4-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd2e4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2e4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd2e4-136">INPUTS</span></span>

### <span data-ttu-id="dd2e4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dd2e4-137">System.String</span></span>

## <span data-ttu-id="dd2e4-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd2e4-138">OUTPUTS</span></span>

### <span data-ttu-id="dd2e4-139">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="dd2e4-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="dd2e4-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd2e4-140">NOTES</span></span>

## <span data-ttu-id="dd2e4-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd2e4-141">RELATED LINKS</span></span>

[<span data-ttu-id="dd2e4-142">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd2e4-142">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd2e4-143">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd2e4-143">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd2e4-144">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd2e4-144">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="dd2e4-145">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd2e4-145">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="dd2e4-146">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd2e4-146">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd2e4-147">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd2e4-147">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd2e4-148">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="dd2e4-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)