---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507105"
---
# <span data-ttu-id="40b27-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="40b27-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="40b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b27-102">SYNOPSIS</span></span>
<span data-ttu-id="40b27-103">Операция создания сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="40b27-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="40b27-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40b27-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="40b27-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40b27-105">DESCRIPTION</span></span>
<span data-ttu-id="40b27-106">Операция создания сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="40b27-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="40b27-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40b27-107">EXAMPLES</span></span>

### <span data-ttu-id="40b27-108">Пример 1. Создание сопоставления</span><span class="sxs-lookup"><span data-stu-id="40b27-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="40b27-109">Создание сопоставления</span><span class="sxs-lookup"><span data-stu-id="40b27-109">Create a mapping</span></span>

## <span data-ttu-id="40b27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40b27-110">PARAMETERS</span></span>

### <span data-ttu-id="40b27-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40b27-111">-AsJob</span></span>
<span data-ttu-id="40b27-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="40b27-112">Run the command as a job</span></span>

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

### <span data-ttu-id="40b27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b27-113">-DefaultProfile</span></span>
<span data-ttu-id="40b27-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40b27-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b27-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="40b27-115">-FabricName</span></span>
<span data-ttu-id="40b27-116">Имя ткань.</span><span class="sxs-lookup"><span data-stu-id="40b27-116">Fabric name.</span></span>

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

### <span data-ttu-id="40b27-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="40b27-117">-MappingName</span></span>
<span data-ttu-id="40b27-118">Имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="40b27-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="40b27-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="40b27-119">-NoWait</span></span>
<span data-ttu-id="40b27-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="40b27-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="40b27-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="40b27-121">-PolicyId</span></span>
<span data-ttu-id="40b27-122">Применимая политика.</span><span class="sxs-lookup"><span data-stu-id="40b27-122">Applicable policy.</span></span>

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

### <span data-ttu-id="40b27-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="40b27-123">-ProtectionContainerName</span></span>
<span data-ttu-id="40b27-124">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="40b27-124">Protection container name.</span></span>

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

### <span data-ttu-id="40b27-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="40b27-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="40b27-126">Сведения о поставщике для сопряжения.</span><span class="sxs-lookup"><span data-stu-id="40b27-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="40b27-127">Чтобы создать, см. раздел "ПРИМЕЧАНИЯ" для свойств PROVIDERSPECIFICINPUT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="40b27-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b27-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b27-128">-ResourceGroupName</span></span>
<span data-ttu-id="40b27-129">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="40b27-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="40b27-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="40b27-130">-ResourceName</span></span>
<span data-ttu-id="40b27-131">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="40b27-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="40b27-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40b27-132">-SubscriptionId</span></span>
<span data-ttu-id="40b27-133">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="40b27-133">The subscription Id.</span></span>

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

### <span data-ttu-id="40b27-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="40b27-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="40b27-135">Имя целевого уникального контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="40b27-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="40b27-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40b27-136">-Confirm</span></span>
<span data-ttu-id="40b27-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="40b27-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b27-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b27-138">-WhatIf</span></span>
<span data-ttu-id="40b27-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40b27-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b27-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="40b27-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b27-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b27-141">CommonParameters</span></span>
<span data-ttu-id="40b27-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b27-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b27-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40b27-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b27-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40b27-144">INPUTS</span></span>

## <span data-ttu-id="40b27-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40b27-145">OUTPUTS</span></span>

### <span data-ttu-id="40b27-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="40b27-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="40b27-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40b27-147">NOTES</span></span>

<span data-ttu-id="40b27-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="40b27-148">ALIASES</span></span>

<span data-ttu-id="40b27-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="40b27-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40b27-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="40b27-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40b27-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40b27-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40b27-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : входные данные поставщика для сопряжения.</span><span class="sxs-lookup"><span data-stu-id="40b27-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="40b27-153">`[InstanceType <String>]`: Тип занятия.</span><span class="sxs-lookup"><span data-stu-id="40b27-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="40b27-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40b27-154">RELATED LINKS</span></span>

