---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235634"
---
# <span data-ttu-id="717cb-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="717cb-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="717cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="717cb-102">SYNOPSIS</span></span>
<span data-ttu-id="717cb-103">Включает шифрование дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="717cb-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="717cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="717cb-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="717cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="717cb-105">DESCRIPTION</span></span>
<span data-ttu-id="717cb-106">Командлет **Set-AzVmssDiskEncryptionExtension** включает шифрование на МНОЖЕСТВЕ виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="717cb-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="717cb-107">Этот командлет включает шифрование, устанавливая расширение шифрования диска в установленном масштабе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="717cb-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="717cb-108">Для виртуальных машин Linux параметр *VolumeType* должен быть представлен и для него должно быть задано значение Data.</span><span class="sxs-lookup"><span data-stu-id="717cb-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="717cb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="717cb-109">EXAMPLES</span></span>

### <span data-ttu-id="717cb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="717cb-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="717cb-111">Эта команда обеспечивает шифрование на всех дисках всех виртуальных машин Windows в наборе масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="717cb-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="717cb-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="717cb-112">Example 2</span></span>
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

<span data-ttu-id="717cb-113">Эта команда обеспечивает шифрование на дисках с данными всех виртуальных машин Linux в наборе масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="717cb-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="717cb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="717cb-114">PARAMETERS</span></span>

### <span data-ttu-id="717cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717cb-115">-DefaultProfile</span></span>
<span data-ttu-id="717cb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="717cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="717cb-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="717cb-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="717cb-118">Отключение автоматического обновления дополнительной версии</span><span class="sxs-lookup"><span data-stu-id="717cb-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="717cb-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="717cb-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="717cb-120">ResourceID класса KeyVault, в который будет помещен созданный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="717cb-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="717cb-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="717cb-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="717cb-122">URL-адрес KeyVault, в котором будет размещен созданный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="717cb-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="717cb-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="717cb-123">-ExtensionName</span></span>
<span data-ttu-id="717cb-124">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="717cb-124">The extension name.</span></span>
<span data-ttu-id="717cb-125">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux</span><span class="sxs-lookup"><span data-stu-id="717cb-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="717cb-126">-Force</span><span class="sxs-lookup"><span data-stu-id="717cb-126">-Force</span></span>
<span data-ttu-id="717cb-127">Чтобы принудительно включить шифрование на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="717cb-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="717cb-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="717cb-128">-ForceUpdate</span></span>
<span data-ttu-id="717cb-129">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="717cb-129">Generate a tag for force update.</span></span>  <span data-ttu-id="717cb-130">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="717cb-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="717cb-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="717cb-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="717cb-132">Алгоритм KeyEncryption, используемый для шифрования ключа шифрования тома</span><span class="sxs-lookup"><span data-stu-id="717cb-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="717cb-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="717cb-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="717cb-134">URL-адрес KeyVault для KeyEncryptionKey, использованный для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="717cb-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="717cb-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="717cb-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="717cb-136">ResourceID of KeyVault, который содержит KeyEncryptionKey, используемый для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="717cb-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="717cb-137">-Парольную фразу</span><span class="sxs-lookup"><span data-stu-id="717cb-137">-Passphrase</span></span>
<span data-ttu-id="717cb-138">Парольная фраза, указанная в параметрах.</span><span class="sxs-lookup"><span data-stu-id="717cb-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="717cb-139">Этот параметр действует только для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="717cb-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="717cb-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="717cb-140">-ResourceGroupName</span></span>
<span data-ttu-id="717cb-141">Имя группы ресурсов, к которой относится параметр масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="717cb-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="717cb-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="717cb-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="717cb-143">Версия обработчика типа.</span><span class="sxs-lookup"><span data-stu-id="717cb-143">The type handler version.</span></span>

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

### <span data-ttu-id="717cb-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="717cb-144">-VMScaleSetName</span></span>
<span data-ttu-id="717cb-145">Имя набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="717cb-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="717cb-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="717cb-146">-VolumeType</span></span>
<span data-ttu-id="717cb-147">Указывает тип томов виртуальных машин, для которых требуется выполнить операцию шифрования: ОС, данные или все.</span><span class="sxs-lookup"><span data-stu-id="717cb-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="717cb-148">Linux: параметр **VolumeType** должен быть представлен и для него должно быть задано значение Data.</span><span class="sxs-lookup"><span data-stu-id="717cb-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="717cb-149">Windows: параметр **VolumeType** , если он есть, должен иметь значение либо ALL, либо OS.</span><span class="sxs-lookup"><span data-stu-id="717cb-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="717cb-150">Если параметр **VolumeType** опущен, по умолчанию используется значение "все".</span><span class="sxs-lookup"><span data-stu-id="717cb-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="717cb-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="717cb-151">-Confirm</span></span>
<span data-ttu-id="717cb-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="717cb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="717cb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="717cb-153">-WhatIf</span></span>
<span data-ttu-id="717cb-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="717cb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="717cb-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="717cb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="717cb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717cb-156">CommonParameters</span></span>
<span data-ttu-id="717cb-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="717cb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717cb-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="717cb-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717cb-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="717cb-159">INPUTS</span></span>

### <span data-ttu-id="717cb-160">System. String</span><span class="sxs-lookup"><span data-stu-id="717cb-160">System.String</span></span>

### <span data-ttu-id="717cb-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="717cb-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="717cb-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="717cb-162">OUTPUTS</span></span>

### <span data-ttu-id="717cb-163">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="717cb-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="717cb-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="717cb-164">NOTES</span></span>

## <span data-ttu-id="717cb-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="717cb-165">RELATED LINKS</span></span>
