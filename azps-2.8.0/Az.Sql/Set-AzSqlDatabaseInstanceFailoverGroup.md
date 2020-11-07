---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 38e19e764e7a9d272db777a295f05016f0ef95af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906341"
---
# <span data-ttu-id="7a913-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7a913-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="7a913-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a913-102">SYNOPSIS</span></span>
<span data-ttu-id="7a913-103">Изменяет конфигурацию группы отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a913-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="7a913-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a913-104">SYNTAX</span></span>

### <span data-ttu-id="7a913-105">SetIFGDefault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a913-105">SetIFGDefault (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a913-106">Установка группы отработки отказа для экземпляра из идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="7a913-106">Set a Instance Failover Group from Resource Id</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a913-107">Установка группы отработки отказа для экземпляра из определения экземпляра AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7a913-107">Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a913-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a913-108">DESCRIPTION</span></span>
<span data-ttu-id="7a913-109">Эта команда изменяет конфигурацию группы отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a913-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="7a913-110">Для выполнения команды следует использовать первичный регион для группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a913-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="7a913-111">Во время предварительного просмотра функции групп, отработки отказа для экземпляра, для параметра-GracePeriodWithDataLossHours поддерживаются только значения, превышающие или равные 1 часу.</span><span class="sxs-lookup"><span data-stu-id="7a913-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="7a913-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a913-112">EXAMPLES</span></span>

### <span data-ttu-id="7a913-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a913-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
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

<span data-ttu-id="7a913-114">Задает в качестве политики отработки отказа для группы перемещения при сбое значение "вручную" по конвейеру в группе отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="7a913-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="7a913-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a913-115">PARAMETERS</span></span>

### <span data-ttu-id="7a913-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="7a913-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="7a913-117">Следует ли запускать автоматический переход с конечной точки только для чтения на сервере-получателе.</span><span class="sxs-lookup"><span data-stu-id="7a913-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="7a913-118">Эта функция пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7a913-118">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a913-119">-DefaultProfile</span></span>
<span data-ttu-id="7a913-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a913-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="7a913-121">-FailoverPolicy</span></span>
<span data-ttu-id="7a913-122">Политика перемещения при сбое для группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a913-122">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="7a913-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="7a913-124">Интервал перед автоматическим переходом на другой ресурс инициируется при возникновении сбоя на сервере основного сервера, и отработка отказа не может быть завершена без потери данных.</span><span class="sxs-lookup"><span data-stu-id="7a913-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a913-125">-InputObject</span></span>
<span data-ttu-id="7a913-126">Объект группы для отработки отказа экземпляра, который нужно настроить</span><span class="sxs-lookup"><span data-stu-id="7a913-126">The Instance Failover Group object to set</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-127">-Location</span><span class="sxs-lookup"><span data-stu-id="7a913-127">-Location</span></span>
<span data-ttu-id="7a913-128">Имя локальной области, из которой извлекается группа отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a913-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault, Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a913-129">-Name</span></span>
<span data-ttu-id="7a913-130">Имя группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a913-130">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a913-131">-ResourceGroupName</span></span>
<span data-ttu-id="7a913-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a913-132">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a913-133">-ResourceId</span></span>
<span data-ttu-id="7a913-134">Идентификатор ресурса группы отработки отказа экземпляра, которую нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="7a913-134">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: String
Parameter Sets: Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a913-135">-Confirm</span></span>
<span data-ttu-id="7a913-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a913-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a913-137">-WhatIf</span></span>
<span data-ttu-id="7a913-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a913-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a913-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a913-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a913-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a913-140">CommonParameters</span></span>
<span data-ttu-id="7a913-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a913-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a913-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a913-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a913-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a913-143">INPUTS</span></span>

### <span data-ttu-id="7a913-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7a913-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="7a913-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7a913-145">System.String</span></span>

## <span data-ttu-id="7a913-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a913-146">OUTPUTS</span></span>

### <span data-ttu-id="7a913-147">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7a913-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="7a913-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a913-148">NOTES</span></span>

## <span data-ttu-id="7a913-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a913-149">RELATED LINKS</span></span>
