---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 7f163a80efe4e10f0107298351c59a72bfaaceb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001683"
---
# <span data-ttu-id="6bdec-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="6bdec-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="6bdec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bdec-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdec-103">Включает шифрование диска для набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="6bdec-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="6bdec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6bdec-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bdec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bdec-105">DESCRIPTION</span></span>
<span data-ttu-id="6bdec-106">С **помощью cmdlet Set-AzVmssDiskEncryptionExtension** можно использовать шифрование в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="6bdec-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="6bdec-107">Этот cmdlet включает шифрование, устанавливая расширение шифрования диска в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="6bdec-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="6bdec-108">Для виртуальных машин Linux параметр *VolumeType* должен быть задан как "Data" (Данные).</span><span class="sxs-lookup"><span data-stu-id="6bdec-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="6bdec-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6bdec-109">EXAMPLES</span></span>

### <span data-ttu-id="6bdec-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bdec-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="6bdec-111">Эта команда позволяет шифровать на всех дисках всех ВМ-файлов Windows в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="6bdec-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="6bdec-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6bdec-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="6bdec-113">Эта команда позволяет шифровать на дисках данных всех VMs Linux в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="6bdec-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="6bdec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bdec-114">PARAMETERS</span></span>

### <span data-ttu-id="6bdec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bdec-115">-DefaultProfile</span></span>
<span data-ttu-id="6bdec-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bdec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bdec-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6bdec-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6bdec-118">Отключение автоматического обновления незначительных версий</span><span class="sxs-lookup"><span data-stu-id="6bdec-118">Disable auto-upgrade of minor version</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6bdec-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="6bdec-120">ResourceID ключаVault, в который будет помещен сгенерированная ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="6bdec-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="6bdec-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="6bdec-122">URL-адрес KeyVault, в который будет помещен сгенерированная ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="6bdec-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="6bdec-123">-ExtensionName</span></span>
<span data-ttu-id="6bdec-124">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="6bdec-124">The extension name.</span></span>
<span data-ttu-id="6bdec-125">Если этот параметр не указан, по умолчанию используются значения AzureDiskEncryption для VMs Windows и AzureDiskEncryptionForLinux для VMs для Linux.</span><span class="sxs-lookup"><span data-stu-id="6bdec-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6bdec-126">-Force</span></span>
<span data-ttu-id="6bdec-127">Принудительное включение шифрования в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6bdec-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6bdec-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="6bdec-128">-ForceUpdate</span></span>
<span data-ttu-id="6bdec-129">Создать тег для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="6bdec-129">Generate a tag for force update.</span></span>  <span data-ttu-id="6bdec-130">Эта возможность предоставляется для выполнения повторяюных операций шифрования на том же VM-</span><span class="sxs-lookup"><span data-stu-id="6bdec-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6bdec-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="6bdec-132">Алгоритм шифрования ключа, используемый для шифрования ключа шифрования тома</span><span class="sxs-lookup"><span data-stu-id="6bdec-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="6bdec-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="6bdec-134">URL-адрес ключа KeyEncryptionKey, используемого для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="6bdec-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6bdec-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="6bdec-136">ResourceID ключаVault, содержащего ключEncryptionKey, используемого для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="6bdec-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="6bdec-137">-Passphrase</span></span>
<span data-ttu-id="6bdec-138">Passphrase specified in parameters (Passphrase specified in parameters).</span><span class="sxs-lookup"><span data-stu-id="6bdec-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="6bdec-139">Этот параметр работает только для Linux VM.</span><span class="sxs-lookup"><span data-stu-id="6bdec-139">This parameter only works for Linux VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bdec-140">-ResourceGroupName</span></span>
<span data-ttu-id="6bdec-141">Имя группы ресурсов, к которой относится набор масштаба VM</span><span class="sxs-lookup"><span data-stu-id="6bdec-141">The resource group name to which the VM Scale Set belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6bdec-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="6bdec-143">Версия обработера типов.</span><span class="sxs-lookup"><span data-stu-id="6bdec-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6bdec-144">-VMScaleSetName</span></span>
<span data-ttu-id="6bdec-145">Имя набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6bdec-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="6bdec-146">-VolumeType</span></span>
<span data-ttu-id="6bdec-147">Определяет тип томов виртуальной машины, с которыми выполняется операция шифрования: ОС, Data или All.</span><span class="sxs-lookup"><span data-stu-id="6bdec-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="6bdec-148">Linux: параметр **VolumeType** должен быть задан в параметре Data.</span><span class="sxs-lookup"><span data-stu-id="6bdec-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="6bdec-149">Windows: параметр **VolumeType** при его отобразить должен быть задан в параметре All или OS.</span><span class="sxs-lookup"><span data-stu-id="6bdec-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="6bdec-150">Если параметр **VolumeType** опущен, по умолчанию он имеет значение "Все".</span><span class="sxs-lookup"><span data-stu-id="6bdec-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdec-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bdec-151">-Confirm</span></span>
<span data-ttu-id="6bdec-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bdec-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bdec-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bdec-153">-WhatIf</span></span>
<span data-ttu-id="6bdec-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bdec-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bdec-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6bdec-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bdec-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdec-156">CommonParameters</span></span>
<span data-ttu-id="6bdec-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bdec-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bdec-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bdec-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdec-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bdec-159">INPUTS</span></span>

### <span data-ttu-id="6bdec-160">System.String</span><span class="sxs-lookup"><span data-stu-id="6bdec-160">System.String</span></span>

### <span data-ttu-id="6bdec-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bdec-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bdec-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6bdec-162">OUTPUTS</span></span>

### <span data-ttu-id="6bdec-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="6bdec-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="6bdec-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6bdec-164">NOTES</span></span>

## <span data-ttu-id="6bdec-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bdec-165">RELATED LINKS</span></span>
