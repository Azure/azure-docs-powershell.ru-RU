---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 15453163918854dd0efa7440209164007335aced
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911311"
---
# <span data-ttu-id="187b0-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="187b0-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="187b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="187b0-102">SYNOPSIS</span></span>
<span data-ttu-id="187b0-103">Включает шифрование дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="187b0-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="187b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="187b0-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="187b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="187b0-105">DESCRIPTION</span></span>
<span data-ttu-id="187b0-106">Командлет **Set-AzVmssDiskEncryptionExtension** включает шифрование на МНОЖЕСТВЕ виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="187b0-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="187b0-107">Этот командлет включает шифрование, устанавливая расширение шифрования диска в установленном масштабе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="187b0-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="187b0-108">Если параметр *Name* не указан, устанавливается расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="187b0-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="187b0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="187b0-109">EXAMPLES</span></span>

### <span data-ttu-id="187b0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="187b0-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="187b0-111">Эта команда обеспечивает шифрование на всех дисках всех виртуальных машин в наборе масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="187b0-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="187b0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="187b0-112">PARAMETERS</span></span>

### <span data-ttu-id="187b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187b0-113">-DefaultProfile</span></span>
<span data-ttu-id="187b0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="187b0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="187b0-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="187b0-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="187b0-116">Отключение автоматического обновления дополнительной версии</span><span class="sxs-lookup"><span data-stu-id="187b0-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="187b0-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="187b0-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="187b0-118">ResourceID класса KeyVault, в который будет помещен созданный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="187b0-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="187b0-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="187b0-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="187b0-120">URL-адрес KeyVault, в котором будет размещен созданный ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="187b0-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="187b0-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="187b0-121">-ExtensionName</span></span>
<span data-ttu-id="187b0-122">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="187b0-122">The extension name.</span></span>
<span data-ttu-id="187b0-123">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux</span><span class="sxs-lookup"><span data-stu-id="187b0-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="187b0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="187b0-124">-Force</span></span>
<span data-ttu-id="187b0-125">Чтобы принудительно включить шифрование на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="187b0-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="187b0-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="187b0-126">-ForceUpdate</span></span>
<span data-ttu-id="187b0-127">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="187b0-127">Generate a tag for force update.</span></span>  <span data-ttu-id="187b0-128">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="187b0-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="187b0-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="187b0-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="187b0-130">Алгоритм KeyEncryption, используемый для шифрования ключа шифрования тома</span><span class="sxs-lookup"><span data-stu-id="187b0-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="187b0-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="187b0-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="187b0-132">URL-адрес KeyVault для KeyEncryptionKey, использованный для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="187b0-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="187b0-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="187b0-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="187b0-134">ResourceID of KeyVault, который содержит KeyEncryptionKey, используемый для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="187b0-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="187b0-135">-Парольную фразу</span><span class="sxs-lookup"><span data-stu-id="187b0-135">-Passphrase</span></span>
<span data-ttu-id="187b0-136">Парольная фраза, указанная в параметрах.</span><span class="sxs-lookup"><span data-stu-id="187b0-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="187b0-137">Этот параметр действует только для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="187b0-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="187b0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187b0-138">-ResourceGroupName</span></span>
<span data-ttu-id="187b0-139">Имя группы ресурсов, к которой относится параметр масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="187b0-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="187b0-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="187b0-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="187b0-141">Версия обработчика типа.</span><span class="sxs-lookup"><span data-stu-id="187b0-141">The type handler version.</span></span>

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

### <span data-ttu-id="187b0-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="187b0-142">-VMScaleSetName</span></span>
<span data-ttu-id="187b0-143">Имя набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="187b0-143">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="187b0-144">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="187b0-144">-VolumeType</span></span>
<span data-ttu-id="187b0-145">Тип тома (ОС или данных) для выполнения операции шифрования</span><span class="sxs-lookup"><span data-stu-id="187b0-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="187b0-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="187b0-146">-Confirm</span></span>
<span data-ttu-id="187b0-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="187b0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="187b0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187b0-148">-WhatIf</span></span>
<span data-ttu-id="187b0-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="187b0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="187b0-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="187b0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="187b0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187b0-151">CommonParameters</span></span>
<span data-ttu-id="187b0-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="187b0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187b0-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187b0-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187b0-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="187b0-154">INPUTS</span></span>

### <span data-ttu-id="187b0-155">System. String</span><span class="sxs-lookup"><span data-stu-id="187b0-155">System.String</span></span>
<span data-ttu-id="187b0-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="187b0-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="187b0-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="187b0-157">OUTPUTS</span></span>

### <span data-ttu-id="187b0-158">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="187b0-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="187b0-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="187b0-159">NOTES</span></span>

## <span data-ttu-id="187b0-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="187b0-160">RELATED LINKS</span></span>

