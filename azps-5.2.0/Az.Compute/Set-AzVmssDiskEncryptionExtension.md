---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409988"
---
# <span data-ttu-id="1ff93-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1ff93-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="1ff93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ff93-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff93-103">Включает шифрование диска для набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="1ff93-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="1ff93-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ff93-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ff93-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ff93-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff93-106">С **помощью cmdlet Set-AzVmssDiskEncryptionExtension** можно использовать шифрование в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="1ff93-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="1ff93-107">Этот cmdlet включает шифрование, устанавливая расширение шифрования диска в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="1ff93-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="1ff93-108">Для виртуальных машин Linux параметр *VolumeType* должен быть задан как "Data" (Данные).</span><span class="sxs-lookup"><span data-stu-id="1ff93-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="1ff93-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ff93-109">EXAMPLES</span></span>

### <span data-ttu-id="1ff93-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1ff93-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="1ff93-111">Эта команда позволяет шифровать на всех дисках всех ВМ-файлов Windows в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="1ff93-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="1ff93-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1ff93-112">Example 2</span></span>
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

<span data-ttu-id="1ff93-113">Эта команда позволяет шифровать на дисках данных всех VMs Linux в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="1ff93-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="1ff93-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ff93-114">PARAMETERS</span></span>

### <span data-ttu-id="1ff93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff93-115">-DefaultProfile</span></span>
<span data-ttu-id="1ff93-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff93-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ff93-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1ff93-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1ff93-118">Отключение автоматического обновления незначительных версий</span><span class="sxs-lookup"><span data-stu-id="1ff93-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="1ff93-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1ff93-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="1ff93-120">ResourceID ключаVault, в который будет помещен сгенерированная ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="1ff93-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="1ff93-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="1ff93-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="1ff93-122">URL-адрес KeyVault, в который будет помещен сгенерированная ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="1ff93-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="1ff93-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="1ff93-123">-ExtensionName</span></span>
<span data-ttu-id="1ff93-124">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="1ff93-124">The extension name.</span></span>
<span data-ttu-id="1ff93-125">Если этот параметр не задан, по умолчанию используются значения AzureDiskEncryption для windows VMs и AzureDiskEncryptionForLinux для VMs для Linux</span><span class="sxs-lookup"><span data-stu-id="1ff93-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="1ff93-126">-Force</span><span class="sxs-lookup"><span data-stu-id="1ff93-126">-Force</span></span>
<span data-ttu-id="1ff93-127">Принудительное включение шифрования в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1ff93-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="1ff93-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="1ff93-128">-ForceUpdate</span></span>
<span data-ttu-id="1ff93-129">Создать тег для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="1ff93-129">Generate a tag for force update.</span></span>  <span data-ttu-id="1ff93-130">Эта возможность предоставляется для выполнения повторяюных операций шифрования на том же VM-</span><span class="sxs-lookup"><span data-stu-id="1ff93-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="1ff93-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1ff93-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="1ff93-132">Алгоритм шифрования ключа, используемый для шифрования ключа шифрования тома</span><span class="sxs-lookup"><span data-stu-id="1ff93-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="1ff93-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="1ff93-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="1ff93-134">URL-адрес ключа KeyEncryptionKey, используемого для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="1ff93-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="1ff93-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1ff93-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="1ff93-136">ResourceID ключаVault, содержащего ключEncryptionKey, используемого для шифрования ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="1ff93-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="1ff93-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="1ff93-137">-Passphrase</span></span>
<span data-ttu-id="1ff93-138">Passphrase specified in parameters (Passphrase specified in parameters).</span><span class="sxs-lookup"><span data-stu-id="1ff93-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="1ff93-139">Этот параметр работает только для Linux VM.</span><span class="sxs-lookup"><span data-stu-id="1ff93-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="1ff93-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff93-140">-ResourceGroupName</span></span>
<span data-ttu-id="1ff93-141">Имя группы ресурсов, к которой относится набор масштаба VM</span><span class="sxs-lookup"><span data-stu-id="1ff93-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="1ff93-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1ff93-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="1ff93-143">Версия обработера типов.</span><span class="sxs-lookup"><span data-stu-id="1ff93-143">The type handler version.</span></span>

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

### <span data-ttu-id="1ff93-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1ff93-144">-VMScaleSetName</span></span>
<span data-ttu-id="1ff93-145">Имя набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1ff93-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="1ff93-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="1ff93-146">-VolumeType</span></span>
<span data-ttu-id="1ff93-147">Определяет тип томов виртуальной машины, с которыми выполняется операция шифрования: ОС, Data или All.</span><span class="sxs-lookup"><span data-stu-id="1ff93-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="1ff93-148">Linux: параметр **VolumeType** должен быть задан в параметре Data.</span><span class="sxs-lookup"><span data-stu-id="1ff93-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="1ff93-149">Windows: параметр **VolumeType** при его отобразить должен быть задан в параметре All или OS.</span><span class="sxs-lookup"><span data-stu-id="1ff93-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="1ff93-150">Если параметр **VolumeType** опущен, по умолчанию он имеет значение "Все".</span><span class="sxs-lookup"><span data-stu-id="1ff93-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="1ff93-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ff93-151">-Confirm</span></span>
<span data-ttu-id="1ff93-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ff93-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ff93-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff93-153">-WhatIf</span></span>
<span data-ttu-id="1ff93-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ff93-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ff93-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1ff93-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ff93-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff93-156">CommonParameters</span></span>
<span data-ttu-id="1ff93-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff93-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff93-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ff93-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff93-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ff93-159">INPUTS</span></span>

### <span data-ttu-id="1ff93-160">System.String</span><span class="sxs-lookup"><span data-stu-id="1ff93-160">System.String</span></span>

### <span data-ttu-id="1ff93-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ff93-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ff93-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ff93-162">OUTPUTS</span></span>

### <span data-ttu-id="1ff93-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="1ff93-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="1ff93-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ff93-164">NOTES</span></span>

## <span data-ttu-id="1ff93-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ff93-165">RELATED LINKS</span></span>
