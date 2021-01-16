---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409324"
---
# <span data-ttu-id="2b9b7-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2b9b7-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="2b9b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9b7-103">Задает свойства восстановления, такие как целевая сеть и размер виртуальной машины для указанного элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="2b9b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b9b7-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b9b7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-105">DESCRIPTION</span></span>
<span data-ttu-id="2b9b7-106">**Cmdlet Set-AzRecoveryServicesAsrReplicationProtectedItem** задает свойства восстановления для защищенного элемента репликации.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="2b9b7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-107">EXAMPLES</span></span>

### <span data-ttu-id="2b9b7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b9b7-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="2b9b7-109">Запускает операцию обновления параметров элемента, защищенного репликацией, с использованием указанных параметров и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2b9b7-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b9b7-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="2b9b7-111">Запускает операцию обновления параметров карточки сетевого интерфейса защищенного элемента с помощью указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2b9b7-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2b9b7-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="2b9b7-113">Запускает операцию обновления основного элемента, защищенного репликацией, NIC(для использования для параметров recovered vm ), используя указанные параметры, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2b9b7-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="2b9b7-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="2b9b7-115">Запускает операцию обновления NIC элемента, защищенного репликацией (для использования для параметров recovered vm ), с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2b9b7-116">Пример 5</span><span class="sxs-lookup"><span data-stu-id="2b9b7-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="2b9b7-117">Начало операции обновления элемента, защищенного репликацией, выбранного без tc, включает ускорение работы сети при восстановлении VM-модели (при аварийном восстановлении из Azure в Azure).</span><span class="sxs-lookup"><span data-stu-id="2b9b7-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="2b9b7-118">Не проходите -EnableAcceleratedNetworkingOnRecovery, чтобы отключить ускорение работы сети.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="2b9b7-119">Пример 6</span><span class="sxs-lookup"><span data-stu-id="2b9b7-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="2b9b7-120">Начните операцию обновления для указанного защищенного зашифрованного элемента репликации, чтобы использовать предоставленные сведения шифрования для отбойной версии VM.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="2b9b7-121">Пример 7</span><span class="sxs-lookup"><span data-stu-id="2b9b7-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="2b9b7-122">Начните операцию обновления для указанного элемента, защищенного репликацией, чтобы использовать группу расположения расположения предоставленных расположений для отбойной версии VM.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>


## <span data-ttu-id="2b9b7-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b9b7-123">PARAMETERS</span></span>

### <span data-ttu-id="2b9b7-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b9b7-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="2b9b7-125">Указывает сведения о конфигурациях NIC для проверки.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-125">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b9b7-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="2b9b7-127">Указывает конфигурацию диска, которая будет udpated для управляемого диска VM (От Azure до Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="2b9b7-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9b7-128">-DefaultProfile</span></span>
<span data-ttu-id="2b9b7-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2b9b7-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="2b9b7-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="2b9b7-131">Указывает секретный URL-адрес шифрования диска с версией (шифрованием диска Azure), который будет использоваться для восстановления VM после отбойного канала.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="2b9b7-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="2b9b7-133">Определяет код секретного сейфа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM после отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="2b9b7-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="2b9b7-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="2b9b7-135">Словарь ИД дискового ресурса для шифрования диска, ARM код.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="2b9b7-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="2b9b7-137">Указывает указанную NIC в режиме восстановления vm после отсека с использованием ускорить передачу данных.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="2b9b7-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b9b7-138">-InputObject</span></span>
<span data-ttu-id="2b9b7-139">Объект ввода для cmdlet: объект, защищенный репликацией ASR, соответствующий обновляемой позиции, защищенной репликацией.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="2b9b7-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="2b9b7-141">Указывает версию URL-адреса ключа шифрования диска (шифрование диска Azure), которая будет использоваться для восстановления VM после отбойного канала.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="2b9b7-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="2b9b7-143">Определяет код keyVault ключа шифрования диска(шифрование диска Azure), который будет использоваться для восстановления VM после отбоя.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="2b9b7-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2b9b7-144">-LicenseType</span></span>
<span data-ttu-id="2b9b7-145">Выбор типа лицензии, который будет использоваться для виртуальных машин Windows Server.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="2b9b7-146">Если вы имеете право на использование Преимущества гибридного использования Azure для миграции и хотите указать, что параметр HUB будет использоваться при отступе над этим защищенным элементом, закажите тип лицензии WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-147">-Name</span><span class="sxs-lookup"><span data-stu-id="2b9b7-147">-Name</span></span>
<span data-ttu-id="2b9b7-148">Указывает имя виртуальной машины восстановления, которая будет создана при откеке.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="2b9b7-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="2b9b7-149">-NicSelectionType</span></span>
<span data-ttu-id="2b9b7-150">Определяет свойства карточки сетевого интерфейса( NIC), задамые пользователем или заданные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="2b9b7-151">Вы можете указать notSelected, чтобы вернуться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-151">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="2b9b7-152">-PrimaryNic</span></span>
<span data-ttu-id="2b9b7-153">Определяет NIC, которая будет использоваться в качестве основного NIC для recvcovery VM после отступа.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="2b9b7-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2b9b7-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="2b9b7-155">Доступность для элемента, защищенного репликацией, после отоятия.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="2b9b7-156">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-156">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="2b9b7-157">Указывает учетную запись хранения для диагностики загрузки для восстановления Azure VM.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-157">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="2b9b7-158">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-158">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="2b9b7-159">ИД ресурса облачной службы восстановления для отохода от сбойной работы этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-159">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="2b9b7-160">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-160">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="2b9b7-161">Определяет целевые пулы адресов, которые будут связаны с NIC для восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-161">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-162">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-162">-RecoveryNetworkId</span></span>
<span data-ttu-id="2b9b7-163">Определяет ID виртуальной сети Azure, в которую необходимо сбой защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-163">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="2b9b7-164">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-164">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="2b9b7-165">Определяет ID группы безопасности сети, которая должна быть связана с NIC восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-165">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="2b9b7-166">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="2b9b7-166">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="2b9b7-167">Указывает статический IP-адрес, который должен быть назначен основной службе NIC при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-167">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="2b9b7-168">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="2b9b7-168">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="2b9b7-169">Имя подсети в виртуальной сети Azure для восстановления, к которой во время отсещения должна быть подключена эта NIC защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-169">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="2b9b7-170">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-170">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="2b9b7-171">Определяет ИД ресурса группы расположения расположения близости восстановления для отостановки отостановки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-171">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="2b9b7-172">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-172">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="2b9b7-173">Определяет ИД ресурса общедоступных IP-адресов, который будет связан с NIC восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-173">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="2b9b7-174">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="2b9b7-174">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="2b9b7-175">ИД группы ресурсов Azure в регионе восстановления, в котором защищенный элемент будет восстановлен при отоходе.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-175">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="2b9b7-176">-Size</span><span class="sxs-lookup"><span data-stu-id="2b9b7-176">-Size</span></span>
<span data-ttu-id="2b9b7-177">Определяет размер виртуальной машины восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-177">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="2b9b7-178">Значение должно быть установлено из набора размеров, поддерживаемых виртуальными машиными Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-178">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="2b9b7-179">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="2b9b7-179">-TfoAzureVMName</span></span>
<span data-ttu-id="2b9b7-180">Указывает имя VM-теста отбойной проверки.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-180">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="2b9b7-181">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="2b9b7-181">-UpdateNic</span></span>
<span data-ttu-id="2b9b7-182">Задает NIC виртуальной машины, для которой этот cmdlet задает udpated свойство сети восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-182">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="2b9b7-183">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2b9b7-183">-UseManagedDisk</span></span>
<span data-ttu-id="2b9b7-184">Указывает, должна ли виртуальная машина Azure, созданная на отбойном компьютере, использовать управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-184">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b9b7-185">-Confirm</span></span>
<span data-ttu-id="2b9b7-186">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9b7-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9b7-187">-WhatIf</span></span>
<span data-ttu-id="2b9b7-188">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-188">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b9b7-189">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9b7-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9b7-190">CommonParameters</span></span>
<span data-ttu-id="2b9b7-191">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9b7-192">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b9b7-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9b7-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b9b7-193">INPUTS</span></span>

### <span data-ttu-id="2b9b7-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2b9b7-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2b9b7-195">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b9b7-195">OUTPUTS</span></span>

### <span data-ttu-id="2b9b7-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="2b9b7-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2b9b7-197">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-197">NOTES</span></span>

## <span data-ttu-id="2b9b7-198">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-198">RELATED LINKS</span></span>

[<span data-ttu-id="2b9b7-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2b9b7-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="2b9b7-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2b9b7-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="2b9b7-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2b9b7-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
