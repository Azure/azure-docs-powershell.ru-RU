---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c1164f7c4875d6cdd00ca13236c1d8e6d4b07cb3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506634"
---
# <span data-ttu-id="f77f7-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f77f7-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f77f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f77f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f77f7-103">Эта команда создает новую группу отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f77f7-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f77f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f77f7-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f77f7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f77f7-105">DESCRIPTION</span></span>
<span data-ttu-id="f77f7-106">Создает новую группу отбойных SQL баз данных Azure для указанных серверов.</span><span class="sxs-lookup"><span data-stu-id="f77f7-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="f77f7-107">В failoverGroupName.SqlDataDnsSuffix (например, FailoverGroupName.database.windows.net) и FailoverGroupName.secondary.SqlDataBaseDnsSuffix создаются две конечные точки базы данных Azure SQL. Secondary.SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="f77f7-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="f77f7-108">Эти конечные точки могут использоваться для подключения к основному и дополнительным серверам в группе failover соответственно.</span><span class="sxs-lookup"><span data-stu-id="f77f7-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="f77f7-109">Если сбой основного сервера влияет на основной сервер, автоматический отключить конечные точки и базы данных будет запускаться автоматически, как это диктуется политикой отключки и льготным периодом для группы отбойных серверов.</span><span class="sxs-lookup"><span data-stu-id="f77f7-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="f77f7-110">Новые группы отбойного управления не содержат баз данных.</span><span class="sxs-lookup"><span data-stu-id="f77f7-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="f77f7-111">Для управления набором баз данных в группе отката используйте cmdlets Add-AzSqlDatabaseToFailoverGroup и Remove-AzSqlDatabaseFromFailoverGroup.</span><span class="sxs-lookup"><span data-stu-id="f77f7-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="f77f7-112">Для параметра "-GracePeriodWithDataLossHours" поддерживаются только значения, которые больше или равны 1 часу.</span><span class="sxs-lookup"><span data-stu-id="f77f7-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f77f7-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f77f7-113">EXAMPLES</span></span>

### <span data-ttu-id="f77f7-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f77f7-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="f77f7-115">Эта команда создает новую группу отбойных серверов с политикой отключки "Автоматически" для двух серверов в одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f77f7-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="f77f7-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f77f7-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="f77f7-117">Эта команда создает новую группу отбойных серверов с политикой отбойного управления "Вручную" для двух серверов в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f77f7-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="f77f7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f77f7-118">PARAMETERS</span></span>

### <span data-ttu-id="f77f7-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f77f7-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f77f7-120">Должен ли сбой на дополнительном сервере запускать автоматическую отключку конечной точки, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f77f7-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="f77f7-121">Эта функция пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f77f7-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="f77f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77f7-122">-DefaultProfile</span></span>
<span data-ttu-id="f77f7-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f77f7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f77f7-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f77f7-124">-FailoverGroupName</span></span>
<span data-ttu-id="f77f7-125">Имя группы отбойных SQL базы данных Azure, которая создается.</span><span class="sxs-lookup"><span data-stu-id="f77f7-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f77f7-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f77f7-126">-FailoverPolicy</span></span>
<span data-ttu-id="f77f7-127">Политика отополномо для группы отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f77f7-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f77f7-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f77f7-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f77f7-129">Интервал до того, как автоматический отключок будет инициен, если происходит сбой на основном сервере и отбой невозможно завершить без потери данных.</span><span class="sxs-lookup"><span data-stu-id="f77f7-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="f77f7-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f77f7-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f77f7-131">Имя вторичной группы ресурсов группы отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f77f7-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f77f7-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="f77f7-132">-PartnerServerName</span></span>
<span data-ttu-id="f77f7-133">Имя дополнительного сервера группы отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f77f7-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f77f7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f77f7-134">-ResourceGroupName</span></span>
<span data-ttu-id="f77f7-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f77f7-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="f77f7-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f77f7-136">-ServerName</span></span>
<span data-ttu-id="f77f7-137">Имя основного сервера баз данных Azure SQL группы failover.</span><span class="sxs-lookup"><span data-stu-id="f77f7-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f77f7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77f7-138">CommonParameters</span></span>
<span data-ttu-id="f77f7-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f77f7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77f7-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f77f7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77f7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f77f7-141">INPUTS</span></span>

### <span data-ttu-id="f77f7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f77f7-142">System.String</span></span>

## <span data-ttu-id="f77f7-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f77f7-143">OUTPUTS</span></span>

### <span data-ttu-id="f77f7-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f77f7-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f77f7-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f77f7-145">NOTES</span></span>

## <span data-ttu-id="f77f7-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f77f7-146">RELATED LINKS</span></span>

[<span data-ttu-id="f77f7-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f77f7-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f77f7-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f77f7-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f77f7-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f77f7-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f77f7-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f77f7-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f77f7-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f77f7-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f77f7-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f77f7-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f77f7-153">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f77f7-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
