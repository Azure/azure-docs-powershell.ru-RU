---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7a893099a81225f165fc6fc56c6ba3fd6cfaec3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078656"
---
# <span data-ttu-id="c291d-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c291d-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="c291d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c291d-102">SYNOPSIS</span></span>
<span data-ttu-id="c291d-103">Эта команда создает новую группу отработки отказов для экземпляра базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c291d-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="c291d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c291d-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c291d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c291d-105">DESCRIPTION</span></span>
<span data-ttu-id="c291d-106">Создание новой группы отработки отказа для экземпляра базы данных SQL Azure между указанными областями с парой помеченных управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c291d-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="c291d-107">Две конечные точки TDS базы данных SQL Azure создаются на базе Name. SqlDatabaseDnsSuffix (например, Name.database.windows.net) и Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="c291d-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="c291d-108">Эти конечные точки можно использовать для подключения к основным и дополнительным областям группы отработки отказа, соответственно.</span><span class="sxs-lookup"><span data-stu-id="c291d-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="c291d-109">Если на основном регионе возникнет сбой, автоматический переход конечных точек и баз данных будет срабатывать в соответствии с политикой перемещения и льготным периодом для группы отказа на перемещение экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="c291d-110">Во время предварительного просмотра функции групп, отработки отказа для экземпляра, для параметра-GracePeriodWithDataLossHours поддерживаются только значения, превышающие или равные 1 часу.</span><span class="sxs-lookup"><span data-stu-id="c291d-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="c291d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c291d-111">EXAMPLES</span></span>

### <span data-ttu-id="c291d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c291d-112">Example 1</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="c291d-113">Эта команда создает новую группу отработки отказа для экземпляра с политикой перемещения при сбое "Авто" для пары управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c291d-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="c291d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c291d-114">Example 2</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="c291d-115">Эта команда создает новую группу отработки отказа для экземпляра с политикой перемещения при сбое "вручную" для пары управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="c291d-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c291d-116">Example 3</span></span>

<span data-ttu-id="c291d-117">Эта команда создает новую группу отработки отказов для экземпляра базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c291d-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="c291d-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="c291d-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="c291d-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c291d-119">PARAMETERS</span></span>

### <span data-ttu-id="c291d-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="c291d-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="c291d-121">Должен ли отказ на сервере-получателе инициировать автоматический переход конечной точки, доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c291d-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="c291d-122">Эта функция пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c291d-122">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="c291d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c291d-123">-DefaultProfile</span></span>
<span data-ttu-id="c291d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c291d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c291d-125">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="c291d-125">-FailoverPolicy</span></span>
<span data-ttu-id="c291d-126">Политика перемещения при сбое для группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-126">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="c291d-127">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="c291d-127">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="c291d-128">Интервал перед автоматическим переходом на другой ресурс инициируется при возникновении сбоя на сервере основного сервера, и отработка отказа не может быть завершена без потери данных.</span><span class="sxs-lookup"><span data-stu-id="c291d-128">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c291d-129">-Location</span><span class="sxs-lookup"><span data-stu-id="c291d-129">-Location</span></span>
<span data-ttu-id="c291d-130">Имя локальной области, из которой извлекается группа отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-130">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c291d-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c291d-131">-Name</span></span>
<span data-ttu-id="c291d-132">Имя создаваемой группы отработки отказа базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c291d-132">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c291d-133">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="c291d-133">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="c291d-134">Имя управляемого экземпляра в области партнера, который нужно добавить в группу отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-134">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="c291d-135">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="c291d-135">-PartnerRegion</span></span>
<span data-ttu-id="c291d-136">Имя региона участника группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-136">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="c291d-137">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c291d-137">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c291d-138">Имя вторичной группы ресурсов для группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-138">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="c291d-139">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c291d-139">-PartnerSubscriptionId</span></span>
<span data-ttu-id="c291d-140">Идентификатор подписки дополнительного управляемого экземпляра группы, отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-140">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="c291d-141">Этот параметр требуется только для настройки подписку</span><span class="sxs-lookup"><span data-stu-id="c291d-141">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="c291d-142">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="c291d-142">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="c291d-143">Имя управляемого экземпляра в локальной области, добавляемого в группу отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c291d-143">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="c291d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c291d-144">-ResourceGroupName</span></span>
<span data-ttu-id="c291d-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c291d-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c291d-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c291d-146">-Confirm</span></span>
<span data-ttu-id="c291d-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c291d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c291d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c291d-148">-WhatIf</span></span>
<span data-ttu-id="c291d-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c291d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c291d-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c291d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c291d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c291d-151">CommonParameters</span></span>
<span data-ttu-id="c291d-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c291d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c291d-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c291d-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c291d-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c291d-154">INPUTS</span></span>

### <span data-ttu-id="c291d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c291d-155">System.String</span></span>

## <span data-ttu-id="c291d-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c291d-156">OUTPUTS</span></span>

### <span data-ttu-id="c291d-157">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c291d-157">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="c291d-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="c291d-158">NOTES</span></span>

## <span data-ttu-id="c291d-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c291d-159">RELATED LINKS</span></span>