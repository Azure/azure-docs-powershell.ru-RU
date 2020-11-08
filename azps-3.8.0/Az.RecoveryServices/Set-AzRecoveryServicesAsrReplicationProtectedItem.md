---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 494edd4f399855512cd7b0a847f261e711bb01cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073531"
---
# <span data-ttu-id="ccaea-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ccaea-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="ccaea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ccaea-102">SYNOPSIS</span></span>
<span data-ttu-id="ccaea-103">Задает свойства восстановления, такие как Целевая сеть и размер виртуальной машины, для указанного элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="ccaea-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="ccaea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ccaea-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccaea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccaea-105">DESCRIPTION</span></span>
<span data-ttu-id="ccaea-106">Командлет **Set-AzRecoveryServicesAsrReplicationProtectedItem** задает свойства восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="ccaea-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="ccaea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ccaea-107">EXAMPLES</span></span>

### <span data-ttu-id="ccaea-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ccaea-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="ccaea-109">Запускает операцию по обновлению параметров защищенного элемента репликации с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="ccaea-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ccaea-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ccaea-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="ccaea-111">Запускает операцию обновления параметров сетевого адаптера, защищенного с помощью репликации, с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="ccaea-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ccaea-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ccaea-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="ccaea-113">Запускает операцию по обновлению основного сетевого адаптера репликации (для использования с восстановленной виртуальной машиной) с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="ccaea-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ccaea-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ccaea-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="ccaea-115">Запускает операцию обновления сетевой карты, защищенной для репликации (для использования в восстановленных виртуальных машинах), с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="ccaea-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ccaea-116">Пример 5</span><span class="sxs-lookup"><span data-stu-id="ccaea-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="ccaea-117">Запускает операцию по обновлению элемента, защищенного с помощью учетной записи в сети NOC TP включите ускоренную работу сетей в виртуальной машине восстановления (для Azure to Azure аварийного восстановления).</span><span class="sxs-lookup"><span data-stu-id="ccaea-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="ccaea-118">Дон t не проходит-EnableAcceleratedNetworkingOnRecovery, чтобы отключить сеть с ускорением.</span><span class="sxs-lookup"><span data-stu-id="ccaea-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="ccaea-119">Пример 6</span><span class="sxs-lookup"><span data-stu-id="ccaea-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="ccaea-120">Запустите операцию обновления для указанного защищенного элемента с шифрованием, чтобы использовать предоставленные сведения о шифровании для отработки отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ccaea-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

## <span data-ttu-id="ccaea-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ccaea-121">PARAMETERS</span></span>

### <span data-ttu-id="ccaea-122">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccaea-122">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="ccaea-123">Задает параметры конфигурации для проверки отказоустойчивости и отказоустойчивости сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="ccaea-123">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="ccaea-124">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccaea-124">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="ccaea-125">Указывает конфигурацию диска для управляемой виртуальной машины на udpated (Azure to Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="ccaea-125">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="ccaea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccaea-126">-DefaultProfile</span></span>
<span data-ttu-id="ccaea-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccaea-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ccaea-128">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="ccaea-128">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="ccaea-129">Указывает секретный URL-адрес шифрования диска, который будет использоваться в качестве виртуальной машины для восстановления после отработки отказа (шифрование диска Azure).</span><span class="sxs-lookup"><span data-stu-id="ccaea-129">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="ccaea-130">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="ccaea-130">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="ccaea-131">Указывает идентификатор хранилища секретного ключа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления виртуальной машины после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ccaea-131">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="ccaea-132">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="ccaea-132">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="ccaea-133">Словарь идентификатора дискового ресурса для набора номера ARM.</span><span class="sxs-lookup"><span data-stu-id="ccaea-133">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="ccaea-134">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="ccaea-134">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="ccaea-135">Указывает указанную сетевую карту в виртуальной машине восстановления после отработки отказа, использующей сетевые адаптеры.</span><span class="sxs-lookup"><span data-stu-id="ccaea-135">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="ccaea-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccaea-136">-InputObject</span></span>
<span data-ttu-id="ccaea-137">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для обновления.</span><span class="sxs-lookup"><span data-stu-id="ccaea-137">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="ccaea-138">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="ccaea-138">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="ccaea-139">Указывает, что версия URL-адреса ключа шифрования диска (шифрование диска Azure) будет использоваться для восстановления виртуальной машины после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ccaea-139">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="ccaea-140">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="ccaea-140">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="ccaea-141">Указывает, что при переходе на другой ресурс keyVault ключ шифрования диска (шифрование диска Azure) будет использоваться для восстановления виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ccaea-141">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="ccaea-142">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ccaea-142">-LicenseType</span></span>
<span data-ttu-id="ccaea-143">Укажите тип лицензии, который будет использоваться для виртуальных машин Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ccaea-143">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="ccaea-144">Если вы правы на использование гибридной возможности использования службы Azure (HUB) для миграции и хотели бы указать, что параметр HUB будет использоваться при сбое для этого защищенного элемента, установите для него тип лицензии WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="ccaea-144">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="ccaea-145">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ccaea-145">-Name</span></span>
<span data-ttu-id="ccaea-146">Указывает имя виртуальной машины восстановления, которая будет создана при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="ccaea-146">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="ccaea-147">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="ccaea-147">-NicSelectionType</span></span>
<span data-ttu-id="ccaea-148">Задает свойства сетевого адаптера, заданные пользователем или заданные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ccaea-148">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="ccaea-149">Вы можете указать NotSelected, чтобы вернуться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ccaea-149">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="ccaea-150">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="ccaea-150">-PrimaryNic</span></span>
<span data-ttu-id="ccaea-151">Указывает NIC, который будет использоваться в качестве основного сетевого адаптера для виртуальной машины recvcovery после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="ccaea-151">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="ccaea-152">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ccaea-152">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="ccaea-153">Набор доступности для защищенного элемента репликации после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ccaea-153">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="ccaea-154">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ccaea-154">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="ccaea-155">Указывает учетную запись хранения для диагностики загрузки для восстановления ВМ Azure.</span><span class="sxs-lookup"><span data-stu-id="ccaea-155">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="ccaea-156">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="ccaea-156">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="ccaea-157">Идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ccaea-157">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="ccaea-158">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ccaea-158">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="ccaea-159">Указывает целевые серверные пулы адресов, которые должны быть связаны с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="ccaea-159">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="ccaea-160">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="ccaea-160">-RecoveryNetworkId</span></span>
<span data-ttu-id="ccaea-161">Указывает идентификатор виртуальной сети Azure, для которой должен быть выполнен отказ для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="ccaea-161">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="ccaea-162">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ccaea-162">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="ccaea-163">Указывает идентификатор сетевой группы безопасности, которая будет связана с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="ccaea-163">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="ccaea-164">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="ccaea-164">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="ccaea-165">Статический IP-адрес, который должен быть назначен основной NIC при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="ccaea-165">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="ccaea-166">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="ccaea-166">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="ccaea-167">Указывает имя подсети в виртуальной сети восстановления Azure, к которому следует подключить этот сетевой адаптер защищенного элемента при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="ccaea-167">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="ccaea-168">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="ccaea-168">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="ccaea-169">Указывает идентификатор ресурса общедоступного IP-адреса, который должен быть связан с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="ccaea-169">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="ccaea-170">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="ccaea-170">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="ccaea-171">Идентификатор группы ресурсов Azure в области восстановления, в которой защищенный элемент будет восстанавливаться при переходе на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="ccaea-171">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="ccaea-172">-Size</span><span class="sxs-lookup"><span data-stu-id="ccaea-172">-Size</span></span>
<span data-ttu-id="ccaea-173">Указывает размер виртуальной машины для восстановления.</span><span class="sxs-lookup"><span data-stu-id="ccaea-173">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="ccaea-174">Значение должно быть из набора размеров, поддерживаемых виртуальными машинами Azure.</span><span class="sxs-lookup"><span data-stu-id="ccaea-174">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="ccaea-175">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="ccaea-175">-TfoAzureVMName</span></span>
<span data-ttu-id="ccaea-176">Указывает имя тестовой виртуальной машины для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ccaea-176">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="ccaea-177">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="ccaea-177">-UpdateNic</span></span>
<span data-ttu-id="ccaea-178">Задает сетевую плату виртуальной машины, для которой этот командлет задает свойство сетевого восстановления, которое требуется udpated.</span><span class="sxs-lookup"><span data-stu-id="ccaea-178">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="ccaea-179">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ccaea-179">-UseManagedDisk</span></span>
<span data-ttu-id="ccaea-180">Указывает, должны ли виртуальные машины Azure, созданные на отработке отказа, использовать управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="ccaea-180">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="ccaea-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccaea-181">-Confirm</span></span>
<span data-ttu-id="ccaea-182">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ccaea-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccaea-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccaea-183">-WhatIf</span></span>
<span data-ttu-id="ccaea-184">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ccaea-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccaea-185">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ccaea-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccaea-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccaea-186">CommonParameters</span></span>
<span data-ttu-id="ccaea-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ccaea-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccaea-188">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccaea-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccaea-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ccaea-189">INPUTS</span></span>

### <span data-ttu-id="ccaea-190">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ccaea-190">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ccaea-191">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccaea-191">OUTPUTS</span></span>

### <span data-ttu-id="ccaea-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ccaea-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ccaea-193">Пуск</span><span class="sxs-lookup"><span data-stu-id="ccaea-193">NOTES</span></span>

## <span data-ttu-id="ccaea-194">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccaea-194">RELATED LINKS</span></span>

[<span data-ttu-id="ccaea-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ccaea-195">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="ccaea-196">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ccaea-196">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="ccaea-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ccaea-197">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
