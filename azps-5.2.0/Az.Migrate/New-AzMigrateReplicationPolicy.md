---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408935"
---
# <span data-ttu-id="0103a-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="0103a-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="0103a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0103a-102">SYNOPSIS</span></span>
<span data-ttu-id="0103a-103">Операция создания политики репликации</span><span class="sxs-lookup"><span data-stu-id="0103a-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="0103a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0103a-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0103a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0103a-105">DESCRIPTION</span></span>
<span data-ttu-id="0103a-106">Операция создания политики репликации</span><span class="sxs-lookup"><span data-stu-id="0103a-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="0103a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0103a-107">EXAMPLES</span></span>

### <span data-ttu-id="0103a-108">Пример 1. Создание политики репликации</span><span class="sxs-lookup"><span data-stu-id="0103a-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="0103a-109">Создание политики для VmWare Cbt</span><span class="sxs-lookup"><span data-stu-id="0103a-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="0103a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0103a-110">PARAMETERS</span></span>

### <span data-ttu-id="0103a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0103a-111">-AsJob</span></span>
<span data-ttu-id="0103a-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0103a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0103a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0103a-113">-DefaultProfile</span></span>
<span data-ttu-id="0103a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0103a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0103a-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0103a-115">-NoWait</span></span>
<span data-ttu-id="0103a-116">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0103a-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0103a-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="0103a-117">-PolicyName</span></span>
<span data-ttu-id="0103a-118">Имя политики репликации</span><span class="sxs-lookup"><span data-stu-id="0103a-118">Replication policy name</span></span>

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

### <span data-ttu-id="0103a-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="0103a-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="0103a-120">The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="0103a-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="0103a-121">Чтобы построить, см. раздел "ПРИМЕЧАНИЯ" для свойств PROVIDERSPECIFICINPUT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0103a-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0103a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0103a-122">-ResourceGroupName</span></span>
<span data-ttu-id="0103a-123">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0103a-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="0103a-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0103a-124">-ResourceName</span></span>
<span data-ttu-id="0103a-125">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0103a-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="0103a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0103a-126">-SubscriptionId</span></span>
<span data-ttu-id="0103a-127">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="0103a-127">The subscription Id.</span></span>

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

### <span data-ttu-id="0103a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0103a-128">-Confirm</span></span>
<span data-ttu-id="0103a-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0103a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0103a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0103a-130">-WhatIf</span></span>
<span data-ttu-id="0103a-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0103a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0103a-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0103a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0103a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0103a-133">CommonParameters</span></span>
<span data-ttu-id="0103a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0103a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0103a-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0103a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0103a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0103a-136">INPUTS</span></span>

## <span data-ttu-id="0103a-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0103a-137">OUTPUTS</span></span>

### <span data-ttu-id="0103a-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="0103a-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="0103a-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0103a-139">NOTES</span></span>

<span data-ttu-id="0103a-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0103a-140">ALIASES</span></span>

<span data-ttu-id="0103a-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0103a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0103a-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0103a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0103a-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0103a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0103a-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="0103a-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="0103a-145">`[InstanceType <String>]`: Тип занятия.</span><span class="sxs-lookup"><span data-stu-id="0103a-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="0103a-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0103a-146">RELATED LINKS</span></span>

