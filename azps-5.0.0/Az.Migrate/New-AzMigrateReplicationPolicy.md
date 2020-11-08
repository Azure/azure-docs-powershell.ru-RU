---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247315"
---
# <span data-ttu-id="105bb-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="105bb-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="105bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="105bb-102">SYNOPSIS</span></span>
<span data-ttu-id="105bb-103">Операция создания политики репликации</span><span class="sxs-lookup"><span data-stu-id="105bb-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="105bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="105bb-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="105bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="105bb-105">DESCRIPTION</span></span>
<span data-ttu-id="105bb-106">Операция создания политики репликации</span><span class="sxs-lookup"><span data-stu-id="105bb-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="105bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="105bb-107">EXAMPLES</span></span>

### <span data-ttu-id="105bb-108">Пример 1: Создание политики репликации</span><span class="sxs-lookup"><span data-stu-id="105bb-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="105bb-109">Создание политики для VmWare CBT</span><span class="sxs-lookup"><span data-stu-id="105bb-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="105bb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="105bb-110">PARAMETERS</span></span>

### <span data-ttu-id="105bb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="105bb-111">-AsJob</span></span>
<span data-ttu-id="105bb-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="105bb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="105bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105bb-113">-DefaultProfile</span></span>
<span data-ttu-id="105bb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="105bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105bb-115">-Wait</span><span class="sxs-lookup"><span data-stu-id="105bb-115">-NoWait</span></span>
<span data-ttu-id="105bb-116">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="105bb-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="105bb-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="105bb-117">-PolicyName</span></span>
<span data-ttu-id="105bb-118">Имя политики репликации</span><span class="sxs-lookup"><span data-stu-id="105bb-118">Replication policy name</span></span>

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

### <span data-ttu-id="105bb-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="105bb-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="105bb-120">ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="105bb-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="105bb-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств PROVIDERSPECIFICINPUT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="105bb-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="105bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="105bb-123">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="105bb-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="105bb-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="105bb-124">-ResourceName</span></span>
<span data-ttu-id="105bb-125">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="105bb-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="105bb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="105bb-126">-SubscriptionId</span></span>
<span data-ttu-id="105bb-127">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="105bb-127">The subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105bb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="105bb-128">-Confirm</span></span>
<span data-ttu-id="105bb-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="105bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="105bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="105bb-130">-WhatIf</span></span>
<span data-ttu-id="105bb-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="105bb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="105bb-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="105bb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="105bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105bb-133">CommonParameters</span></span>
<span data-ttu-id="105bb-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="105bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105bb-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="105bb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105bb-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="105bb-136">INPUTS</span></span>

## <span data-ttu-id="105bb-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="105bb-137">OUTPUTS</span></span>

### <span data-ttu-id="105bb-138">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="105bb-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="105bb-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="105bb-139">NOTES</span></span>

<span data-ttu-id="105bb-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="105bb-140">ALIASES</span></span>

<span data-ttu-id="105bb-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="105bb-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="105bb-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="105bb-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="105bb-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="105bb-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="105bb-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="105bb-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="105bb-145">`[InstanceType <String>]`: Тип класса.</span><span class="sxs-lookup"><span data-stu-id="105bb-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="105bb-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="105bb-146">RELATED LINKS</span></span>

