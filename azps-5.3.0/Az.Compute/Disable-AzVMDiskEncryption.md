---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519647"
---
# <span data-ttu-id="f00d3-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f00d3-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="f00d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f00d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f00d3-103">Отключает шифрование на виртуальной машине IaaS.</span><span class="sxs-lookup"><span data-stu-id="f00d3-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="f00d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f00d3-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f00d3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f00d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f00d3-106">**Cmdlet Disable-AzVMDiskEncryption** отключает шифрование в инфраструктуре в качестве виртуальной машины (IaaS).</span><span class="sxs-lookup"><span data-stu-id="f00d3-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="f00d3-107">Этот cmdlet поддерживается только на виртуальных машинах Windows, а не на виртуальных машинах Linux.</span><span class="sxs-lookup"><span data-stu-id="f00d3-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="f00d3-108">Этот cmdlet устанавливает расширение на виртуальной машине, чтобы отключить шифрование.</span><span class="sxs-lookup"><span data-stu-id="f00d3-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="f00d3-109">Если параметр *Name* не указан, создается расширение со стандартным именем AzureDiskEncryption для VMs Windows.</span><span class="sxs-lookup"><span data-stu-id="f00d3-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="f00d3-110">Внимание! Этот cmdlet перезагружает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f00d3-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="f00d3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f00d3-111">EXAMPLES</span></span>

### <span data-ttu-id="f00d3-112">Пример 1. Отключение шифрования для всех томов на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="f00d3-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="f00d3-113">Эта команда отключает шифрование для объемов типов виртуальных машин с именем VM002, принадлежащих группе ресурсов Group001.</span><span class="sxs-lookup"><span data-stu-id="f00d3-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="f00d3-114">Так как *параметр VolumeType* не указан, для параметра Cmdlet задано значение All.</span><span class="sxs-lookup"><span data-stu-id="f00d3-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="f00d3-115">Пример 2. Отключение шифрования для томов данных на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="f00d3-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="f00d3-116">Эта команда отключает шифрование для объемов данных типа виртуальной машины с именем VM004, которая принадлежит к группе ресурсов Group002.</span><span class="sxs-lookup"><span data-stu-id="f00d3-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="f00d3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f00d3-117">PARAMETERS</span></span>

### <span data-ttu-id="f00d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00d3-118">-DefaultProfile</span></span>
<span data-ttu-id="f00d3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f00d3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f00d3-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f00d3-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f00d3-121">Указывает на то, что этот cmdlet отключает автоматическое обновление незначительных версий расширения.</span><span class="sxs-lookup"><span data-stu-id="f00d3-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="f00d3-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="f00d3-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="f00d3-123">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="f00d3-123">The extension publisher name.</span></span> <span data-ttu-id="f00d3-124">Укажите этот параметр только для переопределения значения по умолчанию microsoft.Azure.Security.</span><span class="sxs-lookup"><span data-stu-id="f00d3-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="f00d3-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f00d3-125">-ExtensionType</span></span>
<span data-ttu-id="f00d3-126">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="f00d3-126">The extension type.</span></span> <span data-ttu-id="f00d3-127">Укажите этот параметр, чтобы переопречить стандартное значение AzureDiskEncryption для VMs Windows и AzureDiskEncryptionForLinux для VMs для Linux.</span><span class="sxs-lookup"><span data-stu-id="f00d3-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="f00d3-128">-Force</span><span class="sxs-lookup"><span data-stu-id="f00d3-128">-Force</span></span>
<span data-ttu-id="f00d3-129">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f00d3-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f00d3-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f00d3-130">-Name</span></span>
<span data-ttu-id="f00d3-131">Указывает имя ресурса Azure Resource Manager (ARM), представляюного расширение.</span><span class="sxs-lookup"><span data-stu-id="f00d3-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="f00d3-132">Если этот параметр не указан, этот cmdlet по умолчанию имеет значение AzureDiskEncryption для VMs Windows.</span><span class="sxs-lookup"><span data-stu-id="f00d3-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00d3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f00d3-133">-ResourceGroupName</span></span>
<span data-ttu-id="f00d3-134">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f00d3-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="f00d3-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f00d3-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="f00d3-136">Указывает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="f00d3-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="f00d3-137">Если значение для этого параметра не задано, используется последняя версия расширения.</span><span class="sxs-lookup"><span data-stu-id="f00d3-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00d3-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="f00d3-138">-VMName</span></span>
<span data-ttu-id="f00d3-139">Указывает имя виртуальной машины, на которую этот cmdlet отключает шифрование.</span><span class="sxs-lookup"><span data-stu-id="f00d3-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00d3-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="f00d3-140">-VolumeType</span></span>
<span data-ttu-id="f00d3-141">Определяет тип томов виртуальной машины для выполнения операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="f00d3-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="f00d3-142">На виртуальных машинах Windows допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f00d3-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="f00d3-143">Все</span><span class="sxs-lookup"><span data-stu-id="f00d3-143">All</span></span>
- <span data-ttu-id="f00d3-144">ОС</span><span class="sxs-lookup"><span data-stu-id="f00d3-144">OS</span></span>
- <span data-ttu-id="f00d3-145">"Данные".</span><span class="sxs-lookup"><span data-stu-id="f00d3-145">Data.</span></span>
<span data-ttu-id="f00d3-146">Если значение для этого параметра не задано, по умолчанию будет указано значение "Все".</span><span class="sxs-lookup"><span data-stu-id="f00d3-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="f00d3-147">Отключение шифрования в настоящее время не поддерживается в Linux.</span><span class="sxs-lookup"><span data-stu-id="f00d3-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00d3-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f00d3-148">-Confirm</span></span>
<span data-ttu-id="f00d3-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f00d3-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00d3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f00d3-150">-WhatIf</span></span>
<span data-ttu-id="f00d3-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f00d3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f00d3-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f00d3-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00d3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00d3-153">CommonParameters</span></span>
<span data-ttu-id="f00d3-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00d3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00d3-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f00d3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00d3-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f00d3-156">INPUTS</span></span>

### <span data-ttu-id="f00d3-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f00d3-157">System.String</span></span>

### <span data-ttu-id="f00d3-158">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f00d3-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f00d3-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f00d3-159">OUTPUTS</span></span>

### <span data-ttu-id="f00d3-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f00d3-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f00d3-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f00d3-161">NOTES</span></span>

## <span data-ttu-id="f00d3-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f00d3-162">RELATED LINKS</span></span>

[<span data-ttu-id="f00d3-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="f00d3-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="f00d3-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f00d3-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="f00d3-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f00d3-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


