---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 90dd1854db30ff20cd864dc04b3235cc4e34c4d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721663"
---
# <span data-ttu-id="60bd6-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="60bd6-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="60bd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="60bd6-103">Включает шифрование дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60bd6-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="60bd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60bd6-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60bd6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60bd6-105">DESCRIPTION</span></span>
<span data-ttu-id="60bd6-106">Командлет **Set-AzVmssDiskEncryptionExtension** включает шифрование на МНОЖЕСТВЕ виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60bd6-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="60bd6-107">Этот командлет включает шифрование, устанавливая расширение шифрования диска в установленном масштабе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60bd6-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="60bd6-108">Для виртуальных машин Linux параметр *VolumeType* должен быть представлен и для него должно быть задано значение Data.</span><span class="sxs-lookup"><span data-stu-id="60bd6-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="60bd6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60bd6-109">EXAMPLES</span></span>

### <span data-ttu-id="60bd6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60bd6-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="60bd6-111">Эта команда обеспечивает шифрование на всех дисках всех виртуальных машин Windows в наборе масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60bd6-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="60bd6-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="60bd6-112">Example 2</span></span>
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

<span data-ttu-id="60bd6-113">Эта команда обеспечивает шифрование на дисках с данными всех виртуальных машин Linux в наборе масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60bd6-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="60bd6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60bd6-114">PARAMETERS</span></span>

### <span data-ttu-id="60bd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60bd6-115">-DefaultProfile</span></span>
<span data-ttu-id="60bd6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60bd6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60bd6-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="60bd6-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="60bd6-118">Отключение автоматического обновления дополнительной версии</span><span class="sxs-lookup"><span data-stu-id="60bd6-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="60bd6-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="60bd6-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="60bd6-120">ResourceID класса KeyVault, в который будет помещен созданный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="60bd6-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="60bd6-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="60bd6-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="60bd6-122">URL-адрес KeyVault, в котором будет размещен созданный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="60bd6-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="60bd6-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="60bd6-123">-ExtensionName</span></span>
<span data-ttu-id="60bd6-124">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="60bd6-124">The extension name.</span></span>
<span data-ttu-id="60bd6-125">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux</span><span class="sxs-lookup"><span data-stu-id="60bd6-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="60bd6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="60bd6-126">-Force</span></span>
<span data-ttu-id="60bd6-127">Чтобы принудительно включить шифрование на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60bd6-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="60bd6-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="60bd6-128">-ForceUpdate</span></span>
<span data-ttu-id="60bd6-129">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="60bd6-129">Generate a tag for force update.</span></span>  <span data-ttu-id="60bd6-130">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="60bd6-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="60bd6-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="60bd6-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="60bd6-132">Алгоритм KeyEncryption, используемый для шифрования ключа шифрования тома</span><span class="sxs-lookup"><span data-stu-id="60bd6-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="60bd6-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="60bd6-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="60bd6-134">URL-адрес KeyVault для KeyEncryptionKey, использованный для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="60bd6-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="60bd6-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="60bd6-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="60bd6-136">ResourceID of KeyVault, который содержит KeyEncryptionKey, используемый для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="60bd6-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="60bd6-137">-Парольную фразу</span><span class="sxs-lookup"><span data-stu-id="60bd6-137">-Passphrase</span></span>
<span data-ttu-id="60bd6-138">Парольная фраза, указанная в параметрах.</span><span class="sxs-lookup"><span data-stu-id="60bd6-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="60bd6-139">Этот параметр действует только для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="60bd6-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="60bd6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60bd6-140">-ResourceGroupName</span></span>
<span data-ttu-id="60bd6-141">Имя группы ресурсов, к которой относится параметр масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60bd6-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="60bd6-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="60bd6-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="60bd6-143">Версия обработчика типа.</span><span class="sxs-lookup"><span data-stu-id="60bd6-143">The type handler version.</span></span>

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

### <span data-ttu-id="60bd6-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="60bd6-144">-VMScaleSetName</span></span>
<span data-ttu-id="60bd6-145">Имя набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="60bd6-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="60bd6-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="60bd6-146">-VolumeType</span></span>
<span data-ttu-id="60bd6-147">Указывает тип томов виртуальных машин, для которых требуется выполнить операцию шифрования: ОС, данные или все.</span><span class="sxs-lookup"><span data-stu-id="60bd6-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="60bd6-148">Linux: параметр **VolumeType** должен быть представлен и для него должно быть задано значение Data.</span><span class="sxs-lookup"><span data-stu-id="60bd6-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="60bd6-149">Windows: параметр **VolumeType** , если он есть, должен иметь значение либо ALL, либо OS.</span><span class="sxs-lookup"><span data-stu-id="60bd6-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="60bd6-150">Если параметр **VolumeType** опущен, по умолчанию используется значение "все".</span><span class="sxs-lookup"><span data-stu-id="60bd6-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="60bd6-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60bd6-151">-Confirm</span></span>
<span data-ttu-id="60bd6-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60bd6-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60bd6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60bd6-153">-WhatIf</span></span>
<span data-ttu-id="60bd6-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60bd6-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60bd6-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60bd6-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60bd6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60bd6-156">CommonParameters</span></span>
<span data-ttu-id="60bd6-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60bd6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60bd6-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60bd6-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60bd6-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60bd6-159">INPUTS</span></span>

### <span data-ttu-id="60bd6-160">System. String</span><span class="sxs-lookup"><span data-stu-id="60bd6-160">System.String</span></span>

### <span data-ttu-id="60bd6-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="60bd6-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60bd6-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60bd6-162">OUTPUTS</span></span>

### <span data-ttu-id="60bd6-163">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="60bd6-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="60bd6-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="60bd6-164">NOTES</span></span>

## <span data-ttu-id="60bd6-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60bd6-165">RELATED LINKS</span></span>
