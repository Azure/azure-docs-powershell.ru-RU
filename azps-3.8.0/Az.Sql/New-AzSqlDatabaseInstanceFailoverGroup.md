---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 41032d2af506305f35197244bad3355f67185861
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066944"
---
# <span data-ttu-id="8a9ee-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8a9ee-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8a9ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9ee-103">Эта команда создает новую группу отработки отказов для экземпляра базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="8a9ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a9ee-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a9ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a9ee-105">DESCRIPTION</span></span>
<span data-ttu-id="8a9ee-106">Создание новой группы отработки отказа для экземпляра базы данных SQL Azure между указанными областями с парой помеченных управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="8a9ee-107">Две конечные точки TDS базы данных SQL Azure создаются на базе Name. SqlDatabaseDnsSuffix (например, Name.database.windows.net) и Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="8a9ee-108">Эти конечные точки можно использовать для подключения к основным и дополнительным областям группы отработки отказа, соответственно.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="8a9ee-109">Если на основном регионе возникнет сбой, автоматический переход конечных точек и баз данных будет срабатывать в соответствии с политикой перемещения и льготным периодом для группы отказа на перемещение экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="8a9ee-110">Во время предварительного просмотра функции групп, отработки отказа для экземпляра, для параметра-GracePeriodWithDataLossHours поддерживаются только значения, превышающие или равные 1 часу.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="8a9ee-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a9ee-111">EXAMPLES</span></span>

### <span data-ttu-id="8a9ee-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a9ee-112">Example 1</span></span>
```
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

<span data-ttu-id="8a9ee-113">Эта команда создает новую группу отработки отказа для экземпляра с политикой перемещения при сбое "Авто" для пары управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="8a9ee-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8a9ee-114">Example 2</span></span>
```
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

<span data-ttu-id="8a9ee-115">Эта команда создает новую группу отработки отказа для экземпляра с политикой перемещения при сбое "вручную" для пары управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="8a9ee-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a9ee-116">PARAMETERS</span></span>

### <span data-ttu-id="8a9ee-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="8a9ee-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="8a9ee-118">Должен ли отказ на сервере-получателе инициировать автоматический переход конечной точки, доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="8a9ee-119">Эта функция пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-119">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="8a9ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9ee-120">-DefaultProfile</span></span>
<span data-ttu-id="8a9ee-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a9ee-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="8a9ee-122">-FailoverPolicy</span></span>
<span data-ttu-id="8a9ee-123">Политика перемещения при сбое для группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-123">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8a9ee-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="8a9ee-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="8a9ee-125">Интервал перед автоматическим переходом на другой ресурс инициируется при возникновении сбоя на сервере основного сервера, и отработка отказа не может быть завершена без потери данных.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="8a9ee-126">-Location</span><span class="sxs-lookup"><span data-stu-id="8a9ee-126">-Location</span></span>
<span data-ttu-id="8a9ee-127">Имя локальной области, из которой извлекается группа отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8a9ee-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a9ee-128">-Name</span></span>
<span data-ttu-id="8a9ee-129">Имя создаваемой группы отработки отказа базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-129">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="8a9ee-130">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="8a9ee-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="8a9ee-131">Имя управляемого экземпляра в области партнера, который нужно добавить в группу отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8a9ee-132">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="8a9ee-132">-PartnerRegion</span></span>
<span data-ttu-id="8a9ee-133">Имя региона участника группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-133">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8a9ee-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a9ee-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="8a9ee-135">Имя вторичной группы ресурсов для группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8a9ee-136">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a9ee-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="8a9ee-137">Идентификатор подписки дополнительного управляемого экземпляра группы, отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="8a9ee-138">Этот параметр требуется только для настройки подписку</span><span class="sxs-lookup"><span data-stu-id="8a9ee-138">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="8a9ee-139">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="8a9ee-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="8a9ee-140">Имя управляемого экземпляра в локальной области, добавляемого в группу отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8a9ee-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a9ee-141">-ResourceGroupName</span></span>
<span data-ttu-id="8a9ee-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="8a9ee-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a9ee-143">-Confirm</span></span>
<span data-ttu-id="8a9ee-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a9ee-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a9ee-145">-WhatIf</span></span>
<span data-ttu-id="8a9ee-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a9ee-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a9ee-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9ee-148">CommonParameters</span></span>
<span data-ttu-id="8a9ee-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a9ee-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9ee-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a9ee-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9ee-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a9ee-151">INPUTS</span></span>

### <span data-ttu-id="8a9ee-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8a9ee-152">System.String</span></span>

## <span data-ttu-id="8a9ee-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a9ee-153">OUTPUTS</span></span>

### <span data-ttu-id="8a9ee-154">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8a9ee-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8a9ee-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a9ee-155">NOTES</span></span>

## <span data-ttu-id="8a9ee-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a9ee-156">RELATED LINKS</span></span>
