---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226964"
---
# <span data-ttu-id="3a577-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="3a577-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="3a577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a577-102">SYNOPSIS</span></span>
<span data-ttu-id="3a577-103">Создает объект сопоставления дисков для реплицируемых дисков виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="3a577-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="3a577-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a577-104">SYNTAX</span></span>

### <span data-ttu-id="3a577-105">AzureToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a577-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a577-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3a577-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a577-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a577-107">DESCRIPTION</span></span>
<span data-ttu-id="3a577-108">Создает объект сопоставления дисков, сопоставленный с учетной записью хранения кэша и целевой учетной записью хранилища (регионом восстановления), который будет использоваться для репликации диска.</span><span class="sxs-lookup"><span data-stu-id="3a577-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="3a577-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a577-109">EXAMPLES</span></span>

### <span data-ttu-id="3a577-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a577-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="3a577-111">Создайте объект сопоставления дисков для репликации дисков виртуальной машины Azure. Используется во время использования Azure в Azure EnableDr и повторной защиты.</span><span class="sxs-lookup"><span data-stu-id="3a577-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="3a577-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3a577-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="3a577-113">Создайте объект сопоставления управляемых дисков для реплицируемых дисков виртуальной машины Azure. Используется во время использования Azure в Azure EnableDr и повторной защиты.</span><span class="sxs-lookup"><span data-stu-id="3a577-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="3a577-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3a577-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="3a577-115">Создайте объект сопоставления управляемых дисков с одним параметром шифрования для репликации виртуальных машин Azure. Используется во время использования Azure в Azure EnableDr и повторной защиты.</span><span class="sxs-lookup"><span data-stu-id="3a577-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="3a577-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="3a577-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="3a577-117">Создайте объект сопоставления управляемых дисков с кодом набора шифрования целевого диска, чтобы реплицировать диски виртуальных машин Azure. Используется во время использования Azure в Azure EnableDr и повторной защиты.</span><span class="sxs-lookup"><span data-stu-id="3a577-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="3a577-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a577-118">PARAMETERS</span></span>

### <span data-ttu-id="3a577-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a577-119">-DefaultProfile</span></span>
<span data-ttu-id="3a577-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a577-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a577-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="3a577-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="3a577-122">Url-адрес секретного ключа шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="3a577-122">Specifies the disk encryption secret url.</span></span>

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

### <span data-ttu-id="3a577-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="3a577-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="3a577-124">Определяет хранилище ключа шифрования диска ARM коду.</span><span class="sxs-lookup"><span data-stu-id="3a577-124">Specifies the disk encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="3a577-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="3a577-125">-DiskId</span></span>
<span data-ttu-id="3a577-126">Определяет дисковый id управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="3a577-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="3a577-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="3a577-127">-FailoverDiskName</span></span>
<span data-ttu-id="3a577-128">Указывает имя диска, созданного во время отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="3a577-128">Specifies the name of the disk created during failover.</span></span>

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

### <span data-ttu-id="3a577-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="3a577-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="3a577-130">Url-адрес шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="3a577-130">Specifies the key encryption Url.</span></span>

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

### <span data-ttu-id="3a577-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="3a577-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="3a577-132">Указывает ключ ключа шифрования ARM код.</span><span class="sxs-lookup"><span data-stu-id="3a577-132">Specifies the key encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="3a577-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3a577-133">-LogStorageAccountId</span></span>
<span data-ttu-id="3a577-134">Определяет ИД учетной записи хранения журнала или кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="3a577-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="3a577-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3a577-135">-ManagedDisk</span></span>
<span data-ttu-id="3a577-136">Определяет входные данные для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="3a577-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="3a577-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3a577-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="3a577-138">Определяет ИД учетной записи хранения Azure, к которая будет реплицироваться.</span><span class="sxs-lookup"><span data-stu-id="3a577-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="3a577-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="3a577-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="3a577-140">Определяет код набора шифрования диска Azure, который будет использоваться для дисков восстановления.</span><span class="sxs-lookup"><span data-stu-id="3a577-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

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

### <span data-ttu-id="3a577-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="3a577-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="3a577-142">Определяет тип учетной записи реплицированный управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="3a577-142">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="3a577-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="3a577-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="3a577-144">Определяет id группы ресурсов восстановления для реплицированный управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="3a577-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="3a577-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="3a577-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="3a577-146">Указывает целевой диск восстановления для реплицированный управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="3a577-146">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="3a577-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="3a577-147">-TfoDiskName</span></span>
<span data-ttu-id="3a577-148">Указывает имя диска, созданного во время отбойной проверки.</span><span class="sxs-lookup"><span data-stu-id="3a577-148">Specifies the name of the disk created during test failover.</span></span>

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

### <span data-ttu-id="3a577-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="3a577-149">-VhdUri</span></span>
<span data-ttu-id="3a577-150">Укажите URI VHD диска, соответствующему этому сопоставлению.</span><span class="sxs-lookup"><span data-stu-id="3a577-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="3a577-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a577-151">-Confirm</span></span>
<span data-ttu-id="3a577-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a577-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a577-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a577-153">-WhatIf</span></span>
<span data-ttu-id="3a577-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a577-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a577-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3a577-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a577-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a577-156">CommonParameters</span></span>
<span data-ttu-id="3a577-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a577-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a577-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a577-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a577-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a577-159">INPUTS</span></span>

### <span data-ttu-id="3a577-160">Нет</span><span class="sxs-lookup"><span data-stu-id="3a577-160">None</span></span>

## <span data-ttu-id="3a577-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a577-161">OUTPUTS</span></span>

### <span data-ttu-id="3a577-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="3a577-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="3a577-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a577-163">NOTES</span></span>

## <span data-ttu-id="3a577-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a577-164">RELATED LINKS</span></span>
