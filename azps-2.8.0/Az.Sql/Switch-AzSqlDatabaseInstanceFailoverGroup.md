---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7d52c80bba03d0e88d6e5302647fd9e6de94675f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906885"
---
# <span data-ttu-id="e42b8-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e42b8-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="e42b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e42b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e42b8-103">Выполняет отработку отказа группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e42b8-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="e42b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e42b8-104">SYNTAX</span></span>

### <span data-ttu-id="e42b8-105">SwitchIFGDefault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e42b8-105">SwitchIFGDefault (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e42b8-106">Переключение группы отработки отказа для экземпляра с ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="e42b8-106">Switch a Instance Failover Group from Resource Id</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e42b8-107">Переключение группы отработки отказа экземпляра из определения экземпляра AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e42b8-107">Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e42b8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e42b8-108">DESCRIPTION</span></span>
<span data-ttu-id="e42b8-109">Эта команда заменяет роли управляемых экземпляров в группе отработки отказа экземпляра, переключаясь на указанный вспомогательный регион, делая его новым первичным регионом.</span><span class="sxs-lookup"><span data-stu-id="e42b8-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="e42b8-110">Все новые сеансы TDS, подключающиеся к основной конечной точке, автоматически перенаправляются в новый первичный регион.</span><span class="sxs-lookup"><span data-stu-id="e42b8-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="e42b8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e42b8-111">EXAMPLES</span></span>

### <span data-ttu-id="e42b8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e42b8-112">Example 1</span></span>
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

<span data-ttu-id="e42b8-113">Выпустить операцию отработки отказа с возможностью передачи данных через конвейер в группе отказоустойчивость экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e42b8-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="e42b8-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e42b8-114">Example 2</span></span>
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

<span data-ttu-id="e42b8-115">Выдайте наиболее фиксированную операцию отработки отказа, которая будет выполнена успешно без потери данных или отката.</span><span class="sxs-lookup"><span data-stu-id="e42b8-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="e42b8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e42b8-116">PARAMETERS</span></span>

### <span data-ttu-id="e42b8-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="e42b8-117">-AllowDataLoss</span></span>
<span data-ttu-id="e42b8-118">Завершение отработки отказа, даже если это может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="e42b8-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="e42b8-119">Это позволит продолжить отработку отказа, даже если база данных-источник недоступна.</span><span class="sxs-lookup"><span data-stu-id="e42b8-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42b8-120">-DefaultProfile</span></span>
<span data-ttu-id="e42b8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e42b8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e42b8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e42b8-122">-InputObject</span></span>
<span data-ttu-id="e42b8-123">Объект группы отработки отказа экземпляра для переключения</span><span class="sxs-lookup"><span data-stu-id="e42b8-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e42b8-124">-Location</span><span class="sxs-lookup"><span data-stu-id="e42b8-124">-Location</span></span>
<span data-ttu-id="e42b8-125">Имя локальной области, из которой извлекается группа отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e42b8-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault, Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42b8-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e42b8-126">-Name</span></span>
<span data-ttu-id="e42b8-127">Имя группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e42b8-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42b8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e42b8-128">-ResourceGroupName</span></span>
<span data-ttu-id="e42b8-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e42b8-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42b8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e42b8-130">-ResourceId</span></span>
<span data-ttu-id="e42b8-131">Идентификатор ресурса группы перемещения при сбое, которую нужно переключить.</span><span class="sxs-lookup"><span data-stu-id="e42b8-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: String
Parameter Sets: Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e42b8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e42b8-132">-Confirm</span></span>
<span data-ttu-id="e42b8-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e42b8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e42b8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e42b8-134">-WhatIf</span></span>
<span data-ttu-id="e42b8-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e42b8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e42b8-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e42b8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e42b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42b8-137">CommonParameters</span></span>
<span data-ttu-id="e42b8-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e42b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42b8-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42b8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42b8-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e42b8-140">INPUTS</span></span>

### <span data-ttu-id="e42b8-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e42b8-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="e42b8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e42b8-142">System.String</span></span>

## <span data-ttu-id="e42b8-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e42b8-143">OUTPUTS</span></span>

### <span data-ttu-id="e42b8-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e42b8-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="e42b8-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e42b8-145">NOTES</span></span>

## <span data-ttu-id="e42b8-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e42b8-146">RELATED LINKS</span></span>
