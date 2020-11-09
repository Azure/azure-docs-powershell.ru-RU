---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248480"
---
# <span data-ttu-id="01ba3-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="01ba3-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="01ba3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="01ba3-103">Создает объект сопоставления дисков для реплицируемых дисков виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="01ba3-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="01ba3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01ba3-104">SYNTAX</span></span>

### <span data-ttu-id="01ba3-105">AzureToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01ba3-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01ba3-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="01ba3-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01ba3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ba3-107">DESCRIPTION</span></span>
<span data-ttu-id="01ba3-108">Создает объект сопоставления дисков, который сопоставляет диск виртуальной машины Azure с учетной записью хранения кэша и целевой учетной записью хранилища (областью восстановления), которая будет использоваться для репликации диска.</span><span class="sxs-lookup"><span data-stu-id="01ba3-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="01ba3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01ba3-109">EXAMPLES</span></span>

### <span data-ttu-id="01ba3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01ba3-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="01ba3-111">Создайте объект сопоставления дисков для дисков виртуальных машин Azure, которые нужно реплицировать. Используется во время работы Azure для Azure и повторно защитить операцию.</span><span class="sxs-lookup"><span data-stu-id="01ba3-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="01ba3-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="01ba3-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="01ba3-113">Создание управляемого объекта сопоставления дисков для дисков виртуальных машин Azure, которые нужно реплицировать. Используется во время работы Azure для Azure и повторно защитить операцию.</span><span class="sxs-lookup"><span data-stu-id="01ba3-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="01ba3-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="01ba3-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="01ba3-115">Создайте управляемый объект сопоставления дисков с одним из параметров шифрования для дисков виртуальных машин Azure, которые нужно реплицировать. Используется во время работы Azure для Azure и повторно защитить операцию.</span><span class="sxs-lookup"><span data-stu-id="01ba3-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="01ba3-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="01ba3-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="01ba3-117">Создание управляемого объекта сопоставления дисков с ИД наборов для шифрования целевого диска для репликации дисков виртуальной машины Azure. Используется во время работы Azure для Azure и повторно защитить операцию.</span><span class="sxs-lookup"><span data-stu-id="01ba3-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="01ba3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01ba3-118">PARAMETERS</span></span>

### <span data-ttu-id="01ba3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ba3-119">-DefaultProfile</span></span>
<span data-ttu-id="01ba3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01ba3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01ba3-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="01ba3-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="01ba3-122">Указывает секретный URL-адрес для шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="01ba3-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="01ba3-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="01ba3-124">Указывает идентификатор ARM хранилища для ключа шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="01ba3-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="01ba3-125">-DiskId</span></span>
<span data-ttu-id="01ba3-126">Указывает идентификатор диска управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="01ba3-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="01ba3-127">-FailoverDiskName</span></span>
<span data-ttu-id="01ba3-128">Указывает имя диска, созданного во время отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="01ba3-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="01ba3-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="01ba3-130">Задает URL-адрес шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="01ba3-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="01ba3-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="01ba3-132">Задает идентификатор ARM для ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="01ba3-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="01ba3-133">-LogStorageAccountId</span></span>
<span data-ttu-id="01ba3-134">Указывает идентификатор журнала или учетной записи для хранения кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="01ba3-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="01ba3-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="01ba3-135">-ManagedDisk</span></span>
<span data-ttu-id="01ba3-136">Указывает входные данные для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="01ba3-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="01ba3-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="01ba3-138">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="01ba3-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="01ba3-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="01ba3-140">Указывает идентификатор набора шифрования диска Azure, который будет использоваться для восстановления дисков.</span><span class="sxs-lookup"><span data-stu-id="01ba3-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="01ba3-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="01ba3-142">Указывает тип учетной записи реплицированного управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="01ba3-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="01ba3-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="01ba3-144">Указывает идентификатор группы ресурсов восстановления для реплицируемого управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="01ba3-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="01ba3-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="01ba3-146">Указывает конечный диск восстановления для реплицируемого управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="01ba3-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="01ba3-147">-TfoDiskName</span></span>
<span data-ttu-id="01ba3-148">Указывает имя диска, созданного во время тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="01ba3-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="01ba3-149">-VhdUri</span></span>
<span data-ttu-id="01ba3-150">Укажите URI виртуального жесткого диска, которому соответствует это сопоставление.</span><span class="sxs-lookup"><span data-stu-id="01ba3-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01ba3-151">-Confirm</span></span>
<span data-ttu-id="01ba3-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01ba3-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01ba3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ba3-153">-WhatIf</span></span>
<span data-ttu-id="01ba3-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01ba3-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01ba3-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01ba3-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01ba3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ba3-156">CommonParameters</span></span>
<span data-ttu-id="01ba3-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01ba3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ba3-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01ba3-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ba3-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01ba3-159">INPUTS</span></span>

### <span data-ttu-id="01ba3-160">Ничего</span><span class="sxs-lookup"><span data-stu-id="01ba3-160">None</span></span>

## <span data-ttu-id="01ba3-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ba3-161">OUTPUTS</span></span>

### <span data-ttu-id="01ba3-162">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="01ba3-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="01ba3-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="01ba3-163">NOTES</span></span>

## <span data-ttu-id="01ba3-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01ba3-164">RELATED LINKS</span></span>