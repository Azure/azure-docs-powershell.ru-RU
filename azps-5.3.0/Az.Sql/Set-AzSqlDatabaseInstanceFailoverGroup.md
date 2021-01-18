---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: f8ac83b684718a6a2698fd1b304b85ffa1ae5d45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504754"
---
# <span data-ttu-id="f7a4f-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f7a4f-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="f7a4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a4f-103">Изменяет конфигурацию группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="f7a4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7a4f-104">SYNTAX</span></span>

### <span data-ttu-id="f7a4f-105">SetInstanceFailoverGroupDefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7a4f-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7a4f-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f7a4f-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7a4f-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="f7a4f-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7a4f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7a4f-108">DESCRIPTION</span></span>
<span data-ttu-id="f7a4f-109">Эта команда изменяет конфигурацию группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="f7a4f-110">Для выполнения команды следует использовать основную область группы отбойных команд экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="f7a4f-111">Во время предварительного просмотра функции "Группы отката" для параметра "-GracePeriodWithDataLossHours" поддерживаются только значения, которые больше или равны 1 часу.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f7a4f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7a4f-112">EXAMPLES</span></span>

### <span data-ttu-id="f7a4f-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7a4f-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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

<span data-ttu-id="f7a4f-114">Устанавливает для группы отбойных отбойных экземпляров политику "Вручную", перенаправив в группу отбойных передач.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="f7a4f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7a4f-115">PARAMETERS</span></span>

### <span data-ttu-id="f7a4f-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f7a4f-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f7a4f-117">Должно ли сбой на дополнительном сервере запускать автоматическую отключку конечной точки, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="f7a4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a4f-118">-DefaultProfile</span></span>
<span data-ttu-id="f7a4f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7a4f-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f7a4f-120">-FailoverPolicy</span></span>
<span data-ttu-id="f7a4f-121">Политика отбойного курса для группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="f7a4f-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f7a4f-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f7a4f-123">Интервал до того, как автоматический отключок будет инициен, если происходит сбой на основном сервере и отбой невозможно завершить без потери данных.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="f7a4f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7a4f-124">-InputObject</span></span>
<span data-ttu-id="f7a4f-125">Объект, который нужно задать в группе отбойных передач экземпляров</span><span class="sxs-lookup"><span data-stu-id="f7a4f-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a4f-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f7a4f-126">-Location</span></span>
<span data-ttu-id="f7a4f-127">Имя локального региона, из которого нужно получить группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a4f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f7a4f-128">-Name</span></span>
<span data-ttu-id="f7a4f-129">Имя группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a4f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7a4f-130">-ResourceGroupName</span></span>
<span data-ttu-id="f7a4f-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a4f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7a4f-132">-ResourceId</span></span>
<span data-ttu-id="f7a4f-133">ИД ресурса группы отбойного управления экземпляра, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a4f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7a4f-134">-Confirm</span></span>
<span data-ttu-id="f7a4f-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7a4f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7a4f-136">-WhatIf</span></span>
<span data-ttu-id="f7a4f-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7a4f-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7a4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a4f-139">CommonParameters</span></span>
<span data-ttu-id="f7a4f-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7a4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a4f-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7a4f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a4f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7a4f-142">INPUTS</span></span>

### <span data-ttu-id="f7a4f-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f7a4f-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="f7a4f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f7a4f-144">System.String</span></span>

## <span data-ttu-id="f7a4f-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7a4f-145">OUTPUTS</span></span>

### <span data-ttu-id="f7a4f-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f7a4f-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="f7a4f-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7a4f-147">NOTES</span></span>

## <span data-ttu-id="f7a4f-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7a4f-148">RELATED LINKS</span></span>
