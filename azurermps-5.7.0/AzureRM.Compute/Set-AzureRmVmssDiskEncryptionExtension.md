---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
ms.openlocfilehash: 541e9df84fb0142ba6bcb43b429b77f64d685dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565550"
---
# <span data-ttu-id="7ffad-101">Set-AzureRmVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="7ffad-101">Set-AzureRmVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="7ffad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ffad-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffad-103">Включает шифрование дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7ffad-103">Enables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ffad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ffad-104">SYNTAX</span></span>

```
Set-AzureRmVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ffad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ffad-105">DESCRIPTION</span></span>
<span data-ttu-id="7ffad-106">Командлет **Set-AzureRmVmssDiskEncryptionExtension** включает шифрование на МНОЖЕСТВЕ виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7ffad-106">The **Set-AzureRmVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="7ffad-107">Этот командлет включает шифрование, устанавливая расширение шифрования диска в установленном масштабе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7ffad-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="7ffad-108">Если параметр *Name* не указан, устанавливается расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="7ffad-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="7ffad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ffad-109">EXAMPLES</span></span>

### <span data-ttu-id="7ffad-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ffad-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzureRmVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="7ffad-111">Эта команда обеспечивает шифрование на всех дисках всех виртуальных машин в наборе масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7ffad-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="7ffad-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ffad-112">PARAMETERS</span></span>

### <span data-ttu-id="7ffad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffad-113">-DefaultProfile</span></span>
<span data-ttu-id="7ffad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ffad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7ffad-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7ffad-116">Отключение автоматического обновления дополнительной версии</span><span class="sxs-lookup"><span data-stu-id="7ffad-116">Disable auto-upgrade of minor version</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="7ffad-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="7ffad-118">ResourceID класса KeyVault, в который будет помещен созданный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="7ffad-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="7ffad-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="7ffad-120">URL-адрес KeyVault, в котором будет размещен созданный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="7ffad-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="7ffad-121">-ExtensionName</span></span>
<span data-ttu-id="7ffad-122">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="7ffad-122">The extension name.</span></span>
<span data-ttu-id="7ffad-123">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux</span><span class="sxs-lookup"><span data-stu-id="7ffad-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7ffad-124">-Force</span></span>
<span data-ttu-id="7ffad-125">Чтобы принудительно включить шифрование на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7ffad-125">To force enabling encryption on the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="7ffad-126">-ForceUpdate</span></span>
<span data-ttu-id="7ffad-127">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="7ffad-127">Generate a tag for force update.</span></span>  <span data-ttu-id="7ffad-128">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7ffad-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7ffad-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="7ffad-130">Алгоритм KeyEncryption, используемый для шифрования ключа шифрования тома</span><span class="sxs-lookup"><span data-stu-id="7ffad-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="7ffad-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="7ffad-132">URL-адрес KeyVault для KeyEncryptionKey, использованный для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="7ffad-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="7ffad-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="7ffad-134">ResourceID of KeyVault, который содержит KeyEncryptionKey, используемый для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="7ffad-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-135">-Парольную фразу</span><span class="sxs-lookup"><span data-stu-id="7ffad-135">-Passphrase</span></span>
<span data-ttu-id="7ffad-136">Парольная фраза, указанная в параметрах.</span><span class="sxs-lookup"><span data-stu-id="7ffad-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="7ffad-137">Этот параметр действует только для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="7ffad-137">This parameter only works for Linux VM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffad-138">-ResourceGroupName</span></span>
<span data-ttu-id="7ffad-139">Имя группы ресурсов, к которой относится параметр масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7ffad-139">The resource group name to which the VM Scale Set belongs to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7ffad-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="7ffad-141">Версия обработчика типа.</span><span class="sxs-lookup"><span data-stu-id="7ffad-141">The type handler version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7ffad-142">-VMScaleSetName</span></span>
<span data-ttu-id="7ffad-143">Имя набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="7ffad-143">Name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-144">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="7ffad-144">-VolumeType</span></span>
<span data-ttu-id="7ffad-145">Тип тома (ОС или данных) для выполнения операции шифрования</span><span class="sxs-lookup"><span data-stu-id="7ffad-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ffad-146">-Confirm</span></span>
<span data-ttu-id="7ffad-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ffad-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ffad-148">-WhatIf</span></span>
<span data-ttu-id="7ffad-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ffad-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ffad-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ffad-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffad-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffad-151">CommonParameters</span></span>
<span data-ttu-id="7ffad-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ffad-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffad-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffad-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffad-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ffad-154">INPUTS</span></span>

### <span data-ttu-id="7ffad-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7ffad-155">System.String</span></span>
<span data-ttu-id="7ffad-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7ffad-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7ffad-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ffad-157">OUTPUTS</span></span>

### <span data-ttu-id="7ffad-158">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="7ffad-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="7ffad-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ffad-159">NOTES</span></span>

## <span data-ttu-id="7ffad-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ffad-160">RELATED LINKS</span></span>
