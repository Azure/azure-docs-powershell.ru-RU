---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 99be70e225dd607c580c4571f4ae332e7badf33a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225100"
---
# <span data-ttu-id="94250-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="94250-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="94250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94250-102">SYNOPSIS</span></span>
<span data-ttu-id="94250-103">Эта команда создает новую группу отбойных SQL экземпляра базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="94250-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="94250-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94250-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94250-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94250-105">DESCRIPTION</span></span>
<span data-ttu-id="94250-106">Создает новую группу отбойного SQL экземпляра базы данных Azure между указанными регионами с указанной парой "Управляемый экземпляр".</span><span class="sxs-lookup"><span data-stu-id="94250-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="94250-107">В доменах Name.SqlDataDnsSuffix (например, Name.database.windows.net) и Name.secondary.SqlDataBaseDnsSuffix создаются две конечные точки базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="94250-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="94250-108">Эти конечные точки могут использоваться для подключения к основной и дополнительным областям группы отключении соответственно.</span><span class="sxs-lookup"><span data-stu-id="94250-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="94250-109">Если на основной регион влияет сбой, автоматический отключок конечных точек и баз данных активируется так, как это диктуется политикой отключки и льготным периодом для группы отключания экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="94250-110">Во время предварительного просмотра функции "Группы отката" для параметра "-GracePeriodWithDataLossHours" поддерживаются только значения, которые больше или равны 1 часу.</span><span class="sxs-lookup"><span data-stu-id="94250-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="94250-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94250-111">EXAMPLES</span></span>

### <span data-ttu-id="94250-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94250-112">Example 1</span></span>
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

<span data-ttu-id="94250-113">Эта команда создает новую группу отключаемого экземпляра с политикой отключки "Автоматически" для пары управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="94250-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94250-114">Example 2</span></span>
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

<span data-ttu-id="94250-115">Эта команда создает новую группу отбойных экземпляров с политикой отбойного управления "Вручную" для пары управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="94250-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="94250-116">Example 3</span></span>

<span data-ttu-id="94250-117">Эта команда создает новую группу отбойных SQL экземпляра базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="94250-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="94250-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="94250-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="94250-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94250-119">PARAMETERS</span></span>

### <span data-ttu-id="94250-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="94250-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="94250-121">Должен ли сбой на дополнительном сервере запускать автоматическую отключку конечной точки, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="94250-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="94250-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94250-122">-DefaultProfile</span></span>
<span data-ttu-id="94250-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94250-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94250-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="94250-124">-FailoverPolicy</span></span>
<span data-ttu-id="94250-125">Политика отс неудачной передачи для группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="94250-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="94250-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="94250-127">Интервал до того, как автоматический отключок будет инициен, если происходит сбой на основном сервере и отбой невозможно завершить без потери данных.</span><span class="sxs-lookup"><span data-stu-id="94250-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="94250-128">-Location</span><span class="sxs-lookup"><span data-stu-id="94250-128">-Location</span></span>
<span data-ttu-id="94250-129">Имя локального региона, из которого нужно получить группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="94250-130">-Name</span><span class="sxs-lookup"><span data-stu-id="94250-130">-Name</span></span>
<span data-ttu-id="94250-131">Имя группы отбойных SQL баз данных Azure, которая создается.</span><span class="sxs-lookup"><span data-stu-id="94250-131">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="94250-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="94250-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="94250-133">Имя управляемого экземпляра в регионе партнера, который нужно добавить в группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="94250-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="94250-134">-PartnerRegion</span></span>
<span data-ttu-id="94250-135">Имя региона партнера группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-135">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="94250-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94250-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="94250-137">Имя вторичной группы ресурсов группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="94250-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94250-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="94250-139">ИД подписки дополнительного управляемого экземпляра группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="94250-140">Этот параметр нужен только для настройки перекрестной подписки.</span><span class="sxs-lookup"><span data-stu-id="94250-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="94250-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="94250-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="94250-142">Имя управляемого экземпляра в локальном регионе, который нужно добавить в группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94250-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="94250-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94250-143">-ResourceGroupName</span></span>
<span data-ttu-id="94250-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94250-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="94250-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94250-145">-Confirm</span></span>
<span data-ttu-id="94250-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="94250-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94250-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94250-147">-WhatIf</span></span>
<span data-ttu-id="94250-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94250-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94250-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94250-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94250-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94250-150">CommonParameters</span></span>
<span data-ttu-id="94250-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94250-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94250-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94250-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94250-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94250-153">INPUTS</span></span>

### <span data-ttu-id="94250-154">System.String</span><span class="sxs-lookup"><span data-stu-id="94250-154">System.String</span></span>

## <span data-ttu-id="94250-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94250-155">OUTPUTS</span></span>

### <span data-ttu-id="94250-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="94250-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="94250-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94250-157">NOTES</span></span>

## <span data-ttu-id="94250-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94250-158">RELATED LINKS</span></span>
