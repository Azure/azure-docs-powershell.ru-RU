---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: a20f2196b6052befb74cd74366c96bf262cdd325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992284"
---
# <span data-ttu-id="8ecb5-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8ecb5-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8ecb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ecb5-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecb5-103">Выполняет отбой для группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="8ecb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ecb5-104">SYNTAX</span></span>

### <span data-ttu-id="8ecb5-105">SwitchInstanceFailoverGroupDefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ecb5-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecb5-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8ecb5-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecb5-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8ecb5-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ecb5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ecb5-108">DESCRIPTION</span></span>
<span data-ttu-id="8ecb5-109">Эта команда меняет роли управляемых экземпляров в группе отбойных экземпляров, не перенаправляя их на указанный дополнительный регион, делая их новыми основными.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="8ecb5-110">Все новые сеансы TDS, подключаясь к основной конечной точке, автоматически переназначаются в новый первичный регион.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="8ecb5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ecb5-111">EXAMPLES</span></span>

### <span data-ttu-id="8ecb5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ecb5-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
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

<span data-ttu-id="8ecb5-113">Выдайте отбой, разрешив потерю данных путем перенаправки в группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="8ecb5-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8ecb5-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
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

<span data-ttu-id="8ecb5-115">Вы можете сделать откат наилучшего действия успешным без потери данных или сбойов и отката.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="8ecb5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ecb5-116">PARAMETERS</span></span>

### <span data-ttu-id="8ecb5-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="8ecb5-117">-AllowDataLoss</span></span>
<span data-ttu-id="8ecb5-118">Завершите отбой, даже если это приведет к потере данных.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="8ecb5-119">Это позволит продолжить отбой, даже если основная база данных недоступна.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="8ecb5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecb5-120">-DefaultProfile</span></span>
<span data-ttu-id="8ecb5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ecb5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ecb5-122">-InputObject</span></span>
<span data-ttu-id="8ecb5-123">Объект failover Group для переключения</span><span class="sxs-lookup"><span data-stu-id="8ecb5-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecb5-124">-Location</span><span class="sxs-lookup"><span data-stu-id="8ecb5-124">-Location</span></span>
<span data-ttu-id="8ecb5-125">Имя локального региона, из которого нужно получить группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecb5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8ecb5-126">-Name</span></span>
<span data-ttu-id="8ecb5-127">Имя группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecb5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecb5-128">-ResourceGroupName</span></span>
<span data-ttu-id="8ecb5-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecb5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecb5-130">-ResourceId</span></span>
<span data-ttu-id="8ecb5-131">ИД ресурса группы отключателя экземпляра, который нужно переключить.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecb5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ecb5-132">-Confirm</span></span>
<span data-ttu-id="8ecb5-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ecb5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ecb5-134">-WhatIf</span></span>
<span data-ttu-id="8ecb5-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ecb5-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ecb5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecb5-137">CommonParameters</span></span>
<span data-ttu-id="8ecb5-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ecb5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecb5-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ecb5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecb5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ecb5-140">INPUTS</span></span>

### <span data-ttu-id="8ecb5-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8ecb5-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="8ecb5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8ecb5-142">System.String</span></span>

## <span data-ttu-id="8ecb5-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ecb5-143">OUTPUTS</span></span>

### <span data-ttu-id="8ecb5-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8ecb5-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8ecb5-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ecb5-145">NOTES</span></span>

## <span data-ttu-id="8ecb5-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ecb5-146">RELATED LINKS</span></span>
