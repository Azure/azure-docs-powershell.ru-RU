---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402855"
---
# <span data-ttu-id="16ef4-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="16ef4-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="16ef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="16ef4-103">Выполняет отбой для группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="16ef4-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="16ef4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16ef4-104">SYNTAX</span></span>

### <span data-ttu-id="16ef4-105">SwitchInstanceFailoverGroupDefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16ef4-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ef4-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="16ef4-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ef4-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="16ef4-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ef4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16ef4-108">DESCRIPTION</span></span>
<span data-ttu-id="16ef4-109">Эта команда меняет роли управляемых экземпляров в группе отбойных экземпляров, не перенаправляя их на указанный дополнительный регион, делая их новыми основными.</span><span class="sxs-lookup"><span data-stu-id="16ef4-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="16ef4-110">Все новые сеансы TDS, подключаясь к основной конечной точке, автоматически переназначаются в новый первичный регион.</span><span class="sxs-lookup"><span data-stu-id="16ef4-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="16ef4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16ef4-111">EXAMPLES</span></span>

### <span data-ttu-id="16ef4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16ef4-112">Example 1</span></span>
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

<span data-ttu-id="16ef4-113">Выдайте отбой, разрешив потерю данных путем перенаправки в группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="16ef4-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="16ef4-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="16ef4-114">Example 2</span></span>
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

<span data-ttu-id="16ef4-115">Вы можете сделать откат наилучшего действия успешным без потери данных или сбойов и отката.</span><span class="sxs-lookup"><span data-stu-id="16ef4-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="16ef4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16ef4-116">PARAMETERS</span></span>

### <span data-ttu-id="16ef4-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="16ef4-117">-AllowDataLoss</span></span>
<span data-ttu-id="16ef4-118">Завершите отбой, даже если это приведет к потере данных.</span><span class="sxs-lookup"><span data-stu-id="16ef4-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="16ef4-119">Это позволит продолжить отбой, даже если основная база данных недоступна.</span><span class="sxs-lookup"><span data-stu-id="16ef4-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="16ef4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ef4-120">-DefaultProfile</span></span>
<span data-ttu-id="16ef4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16ef4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16ef4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16ef4-122">-InputObject</span></span>
<span data-ttu-id="16ef4-123">Объект failover Group для переключения</span><span class="sxs-lookup"><span data-stu-id="16ef4-123">The Instance Failover Group object to switch</span></span>

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

### <span data-ttu-id="16ef4-124">-Location</span><span class="sxs-lookup"><span data-stu-id="16ef4-124">-Location</span></span>
<span data-ttu-id="16ef4-125">Имя локального региона, из которого нужно получить группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="16ef4-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="16ef4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="16ef4-126">-Name</span></span>
<span data-ttu-id="16ef4-127">Имя группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="16ef4-127">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="16ef4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ef4-128">-ResourceGroupName</span></span>
<span data-ttu-id="16ef4-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16ef4-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="16ef4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16ef4-130">-ResourceId</span></span>
<span data-ttu-id="16ef4-131">ИД ресурса группы отключаемого экземпляра, который нужно переключить.</span><span class="sxs-lookup"><span data-stu-id="16ef4-131">The Resource ID of the Instance Failover Group to switch.</span></span>

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

### <span data-ttu-id="16ef4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16ef4-132">-Confirm</span></span>
<span data-ttu-id="16ef4-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16ef4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ef4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ef4-134">-WhatIf</span></span>
<span data-ttu-id="16ef4-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16ef4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ef4-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="16ef4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ef4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ef4-137">CommonParameters</span></span>
<span data-ttu-id="16ef4-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ef4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ef4-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16ef4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ef4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16ef4-140">INPUTS</span></span>

### <span data-ttu-id="16ef4-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="16ef4-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="16ef4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="16ef4-142">System.String</span></span>

## <span data-ttu-id="16ef4-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16ef4-143">OUTPUTS</span></span>

### <span data-ttu-id="16ef4-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="16ef4-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="16ef4-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16ef4-145">NOTES</span></span>

## <span data-ttu-id="16ef4-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16ef4-146">RELATED LINKS</span></span>
