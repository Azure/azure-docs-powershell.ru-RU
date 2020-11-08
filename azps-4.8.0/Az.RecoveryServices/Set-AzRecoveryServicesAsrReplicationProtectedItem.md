---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235932"
---
# <span data-ttu-id="fc941-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc941-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="fc941-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc941-102">SYNOPSIS</span></span>
<span data-ttu-id="fc941-103">Задает свойства восстановления, такие как Целевая сеть и размер виртуальной машины, для указанного элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="fc941-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="fc941-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc941-104">SYNTAX</span></span>

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

## <span data-ttu-id="fc941-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc941-105">DESCRIPTION</span></span>
<span data-ttu-id="fc941-106">Командлет **Set-AzRecoveryServicesAsrReplicationProtectedItem** задает свойства восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="fc941-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="fc941-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc941-107">EXAMPLES</span></span>

### <span data-ttu-id="fc941-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc941-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="fc941-109">Запускает операцию по обновлению параметров защищенного элемента репликации с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="fc941-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="fc941-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fc941-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="fc941-111">Запускает операцию обновления параметров сетевого адаптера, защищенного с помощью репликации, с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="fc941-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="fc941-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fc941-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="fc941-113">Запускает операцию по обновлению основного сетевого адаптера репликации (для использования с восстановленной виртуальной машиной) с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="fc941-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="fc941-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="fc941-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="fc941-115">Запускает операцию обновления сетевой карты, защищенной для репликации (для использования в восстановленных виртуальных машинах), с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="fc941-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="fc941-116">Пример 5</span><span class="sxs-lookup"><span data-stu-id="fc941-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="fc941-117">Запускает операцию по обновлению элемента, защищенного с помощью учетной записи в сети NOC TP включите ускоренную работу сетей в виртуальной машине восстановления (для Azure to Azure аварийного восстановления).</span><span class="sxs-lookup"><span data-stu-id="fc941-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="fc941-118">Дон t не проходит-EnableAcceleratedNetworkingOnRecovery, чтобы отключить сеть с ускорением.</span><span class="sxs-lookup"><span data-stu-id="fc941-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="fc941-119">Пример 6</span><span class="sxs-lookup"><span data-stu-id="fc941-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="fc941-120">Запустите операцию обновления для указанного защищенного элемента с шифрованием, чтобы использовать предоставленные сведения о шифровании для отработки отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fc941-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="fc941-121">Пример 7</span><span class="sxs-lookup"><span data-stu-id="fc941-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="fc941-122">Начните операцию обновления для указанного элемента, защищенного репликацией, чтобы использовать предоставленную группу размещения близких для отработки отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fc941-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>


## <span data-ttu-id="fc941-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc941-123">PARAMETERS</span></span>

### <span data-ttu-id="fc941-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc941-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="fc941-125">Задает параметры конфигурации для проверки отказоустойчивости и отказоустойчивости сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="fc941-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="fc941-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc941-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="fc941-127">Указывает конфигурацию диска для управляемой виртуальной машины на udpated (Azure to Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="fc941-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="fc941-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc941-128">-DefaultProfile</span></span>
<span data-ttu-id="fc941-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc941-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fc941-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="fc941-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="fc941-131">Указывает секретный URL-адрес шифрования диска, который будет использоваться в качестве виртуальной машины для восстановления после отработки отказа (шифрование диска Azure).</span><span class="sxs-lookup"><span data-stu-id="fc941-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="fc941-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="fc941-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="fc941-133">Указывает идентификатор хранилища секретного ключа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления виртуальной машины после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fc941-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="fc941-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="fc941-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="fc941-135">Словарь идентификатора дискового ресурса для набора номера ARM.</span><span class="sxs-lookup"><span data-stu-id="fc941-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="fc941-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="fc941-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="fc941-137">Указывает указанную сетевую карту в виртуальной машине восстановления после отработки отказа, использующей сетевые адаптеры.</span><span class="sxs-lookup"><span data-stu-id="fc941-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="fc941-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc941-138">-InputObject</span></span>
<span data-ttu-id="fc941-139">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для обновления.</span><span class="sxs-lookup"><span data-stu-id="fc941-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="fc941-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="fc941-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="fc941-141">Указывает, что версия URL-адреса ключа шифрования диска (шифрование диска Azure) будет использоваться для восстановления виртуальной машины после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fc941-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="fc941-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="fc941-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="fc941-143">Указывает, что при переходе на другой ресурс keyVault ключ шифрования диска (шифрование диска Azure) будет использоваться для восстановления виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fc941-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="fc941-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fc941-144">-LicenseType</span></span>
<span data-ttu-id="fc941-145">Укажите тип лицензии, который будет использоваться для виртуальных машин Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fc941-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="fc941-146">Если вы правы на использование гибридной возможности использования службы Azure (HUB) для миграции и хотели бы указать, что параметр HUB будет использоваться при сбое для этого защищенного элемента, установите для него тип лицензии WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="fc941-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="fc941-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc941-147">-Name</span></span>
<span data-ttu-id="fc941-148">Указывает имя виртуальной машины восстановления, которая будет создана при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="fc941-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="fc941-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="fc941-149">-NicSelectionType</span></span>
<span data-ttu-id="fc941-150">Задает свойства сетевого адаптера, заданные пользователем или заданные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc941-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="fc941-151">Вы можете указать NotSelected, чтобы вернуться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc941-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="fc941-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="fc941-152">-PrimaryNic</span></span>
<span data-ttu-id="fc941-153">Указывает NIC, который будет использоваться в качестве основного сетевого адаптера для виртуальной машины recvcovery после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="fc941-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="fc941-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fc941-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="fc941-155">Набор доступности для защищенного элемента репликации после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fc941-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="fc941-156">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fc941-156">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="fc941-157">Указывает учетную запись хранения для диагностики загрузки для восстановления ВМ Azure.</span><span class="sxs-lookup"><span data-stu-id="fc941-157">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="fc941-158">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="fc941-158">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="fc941-159">Идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fc941-159">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="fc941-160">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="fc941-160">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="fc941-161">Указывает целевые серверные пулы адресов, которые должны быть связаны с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="fc941-161">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="fc941-162">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="fc941-162">-RecoveryNetworkId</span></span>
<span data-ttu-id="fc941-163">Указывает идентификатор виртуальной сети Azure, для которой должен быть выполнен отказ для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="fc941-163">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="fc941-164">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fc941-164">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="fc941-165">Указывает идентификатор сетевой группы безопасности, которая будет связана с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="fc941-165">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="fc941-166">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="fc941-166">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="fc941-167">Статический IP-адрес, который должен быть назначен основной NIC при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="fc941-167">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="fc941-168">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="fc941-168">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="fc941-169">Указывает имя подсети в виртуальной сети восстановления Azure, к которому следует подключить этот сетевой адаптер защищенного элемента при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="fc941-169">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="fc941-170">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fc941-170">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="fc941-171">Указывает идентификатор ресурса группы размещения для восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fc941-171">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="fc941-172">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="fc941-172">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="fc941-173">Указывает идентификатор ресурса общедоступного IP-адреса, который должен быть связан с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="fc941-173">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="fc941-174">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="fc941-174">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="fc941-175">Идентификатор группы ресурсов Azure в области восстановления, в которой защищенный элемент будет восстанавливаться при переходе на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="fc941-175">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="fc941-176">-Size</span><span class="sxs-lookup"><span data-stu-id="fc941-176">-Size</span></span>
<span data-ttu-id="fc941-177">Указывает размер виртуальной машины для восстановления.</span><span class="sxs-lookup"><span data-stu-id="fc941-177">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="fc941-178">Значение должно быть из набора размеров, поддерживаемых виртуальными машинами Azure.</span><span class="sxs-lookup"><span data-stu-id="fc941-178">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="fc941-179">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="fc941-179">-TfoAzureVMName</span></span>
<span data-ttu-id="fc941-180">Указывает имя тестовой виртуальной машины для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fc941-180">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="fc941-181">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="fc941-181">-UpdateNic</span></span>
<span data-ttu-id="fc941-182">Задает сетевую плату виртуальной машины, для которой этот командлет задает свойство сетевого восстановления, которое требуется udpated.</span><span class="sxs-lookup"><span data-stu-id="fc941-182">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="fc941-183">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="fc941-183">-UseManagedDisk</span></span>
<span data-ttu-id="fc941-184">Указывает, должны ли виртуальные машины Azure, созданные на отработке отказа, использовать управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="fc941-184">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="fc941-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc941-185">-Confirm</span></span>
<span data-ttu-id="fc941-186">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc941-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc941-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc941-187">-WhatIf</span></span>
<span data-ttu-id="fc941-188">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc941-188">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc941-189">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc941-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc941-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc941-190">CommonParameters</span></span>
<span data-ttu-id="fc941-191">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc941-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc941-192">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc941-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc941-193">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc941-193">INPUTS</span></span>

### <span data-ttu-id="fc941-194">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc941-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fc941-195">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc941-195">OUTPUTS</span></span>

### <span data-ttu-id="fc941-196">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fc941-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fc941-197">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc941-197">NOTES</span></span>

## <span data-ttu-id="fc941-198">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc941-198">RELATED LINKS</span></span>

[<span data-ttu-id="fc941-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc941-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="fc941-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc941-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="fc941-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc941-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
