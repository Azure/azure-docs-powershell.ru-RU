---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248635"
---
# <span data-ttu-id="88528-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="88528-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="88528-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88528-102">SYNOPSIS</span></span>
<span data-ttu-id="88528-103">Операция для создания сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="88528-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="88528-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88528-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="88528-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88528-105">DESCRIPTION</span></span>
<span data-ttu-id="88528-106">Операция для создания сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="88528-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="88528-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88528-107">EXAMPLES</span></span>

### <span data-ttu-id="88528-108">Пример 1: Создание сопоставления</span><span class="sxs-lookup"><span data-stu-id="88528-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="88528-109">Создание сопоставления</span><span class="sxs-lookup"><span data-stu-id="88528-109">Create a mapping</span></span>

## <span data-ttu-id="88528-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88528-110">PARAMETERS</span></span>

### <span data-ttu-id="88528-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88528-111">-AsJob</span></span>
<span data-ttu-id="88528-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="88528-112">Run the command as a job</span></span>

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

### <span data-ttu-id="88528-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88528-113">-DefaultProfile</span></span>
<span data-ttu-id="88528-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88528-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88528-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="88528-115">-FabricName</span></span>
<span data-ttu-id="88528-116">Имя структуры.</span><span class="sxs-lookup"><span data-stu-id="88528-116">Fabric name.</span></span>

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

### <span data-ttu-id="88528-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="88528-117">-MappingName</span></span>
<span data-ttu-id="88528-118">Имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="88528-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="88528-119">-Wait</span><span class="sxs-lookup"><span data-stu-id="88528-119">-NoWait</span></span>
<span data-ttu-id="88528-120">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="88528-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88528-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="88528-121">-PolicyId</span></span>
<span data-ttu-id="88528-122">Применимая политика.</span><span class="sxs-lookup"><span data-stu-id="88528-122">Applicable policy.</span></span>

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

### <span data-ttu-id="88528-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="88528-123">-ProtectionContainerName</span></span>
<span data-ttu-id="88528-124">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="88528-124">Protection container name.</span></span>

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

### <span data-ttu-id="88528-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="88528-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="88528-126">Специальные данные поставщика для связывания.</span><span class="sxs-lookup"><span data-stu-id="88528-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="88528-127">Для конструирования ознакомьтесь с разделом "Заметки" для свойств PROVIDERSPECIFICINPUT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="88528-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88528-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88528-128">-ResourceGroupName</span></span>
<span data-ttu-id="88528-129">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="88528-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="88528-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="88528-130">-ResourceName</span></span>
<span data-ttu-id="88528-131">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="88528-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="88528-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88528-132">-SubscriptionId</span></span>
<span data-ttu-id="88528-133">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="88528-133">The subscription Id.</span></span>

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

### <span data-ttu-id="88528-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="88528-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="88528-135">Целевое имя контейнера для уникальной защиты.</span><span class="sxs-lookup"><span data-stu-id="88528-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="88528-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88528-136">-Confirm</span></span>
<span data-ttu-id="88528-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88528-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88528-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88528-138">-WhatIf</span></span>
<span data-ttu-id="88528-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88528-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88528-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88528-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88528-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88528-141">CommonParameters</span></span>
<span data-ttu-id="88528-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88528-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88528-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88528-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88528-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88528-144">INPUTS</span></span>

## <span data-ttu-id="88528-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88528-145">OUTPUTS</span></span>

### <span data-ttu-id="88528-146">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="88528-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="88528-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="88528-147">NOTES</span></span>

<span data-ttu-id="88528-148">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="88528-148">ALIASES</span></span>

<span data-ttu-id="88528-149">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="88528-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88528-150">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88528-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88528-151">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88528-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88528-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : данные, специфические для поставщика, для связывания.</span><span class="sxs-lookup"><span data-stu-id="88528-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="88528-153">`[InstanceType <String>]`: Тип класса.</span><span class="sxs-lookup"><span data-stu-id="88528-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="88528-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88528-154">RELATED LINKS</span></span>

