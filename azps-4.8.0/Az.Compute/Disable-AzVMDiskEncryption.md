---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242571"
---
# <span data-ttu-id="19ec8-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="19ec8-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="19ec8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="19ec8-103">Отключение шифрования на виртуальной машине IaaS.</span><span class="sxs-lookup"><span data-stu-id="19ec8-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="19ec8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19ec8-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19ec8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19ec8-105">DESCRIPTION</span></span>
<span data-ttu-id="19ec8-106">Командлет **Disable-AzVMDiskEncryption** отключает шифрование инфраструктуры в качестве виртуальной машины службы (IaaS).</span><span class="sxs-lookup"><span data-stu-id="19ec8-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="19ec8-107">Этот командлет поддерживается только на виртуальных машинах Windows и не виртуальных машинах Linux.</span><span class="sxs-lookup"><span data-stu-id="19ec8-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="19ec8-108">Этот командлет устанавливает расширение на виртуальной машине, чтобы отключить шифрование.</span><span class="sxs-lookup"><span data-stu-id="19ec8-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="19ec8-109">Если параметр *Name* не указан, создается расширение с именем по умолчанию "AzureDiskEncryption для Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="19ec8-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="19ec8-110">Предупреждение: Этот командлет перезагружает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="19ec8-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="19ec8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19ec8-111">EXAMPLES</span></span>

### <span data-ttu-id="19ec8-112">Пример 1: отключение шифрования для всех томов на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="19ec8-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="19ec8-113">Эта команда отключает шифрование для томов типа ALL для виртуальной машины с именем VM002, которая входит в группу ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="19ec8-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="19ec8-114">Так как параметр *VolumeType* не указан, командлет задает значение ALL.</span><span class="sxs-lookup"><span data-stu-id="19ec8-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="19ec8-115">Пример 2: отключение шифрования для томов данных на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="19ec8-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="19ec8-116">Эта команда отключает шифрование томов типа "данные" для виртуальной машины с именем VM004, которая входит в группу ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="19ec8-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="19ec8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19ec8-117">PARAMETERS</span></span>

### <span data-ttu-id="19ec8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ec8-118">-DefaultProfile</span></span>
<span data-ttu-id="19ec8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19ec8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19ec8-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="19ec8-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="19ec8-121">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="19ec8-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="19ec8-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="19ec8-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="19ec8-123">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="19ec8-123">The extension publisher name.</span></span> <span data-ttu-id="19ec8-124">Указывайте этот параметр только для переопределения значения по умолчанию Microsoft. Azure. Security.</span><span class="sxs-lookup"><span data-stu-id="19ec8-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="19ec8-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="19ec8-125">-ExtensionType</span></span>
<span data-ttu-id="19ec8-126">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="19ec8-126">The extension type.</span></span> <span data-ttu-id="19ec8-127">Укажите этот параметр для переопределения значения по умолчанию "AzureDiskEncryption" для виртуальных машин и "AzureDiskEncryptionForLinux" для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="19ec8-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="19ec8-128">-Force</span><span class="sxs-lookup"><span data-stu-id="19ec8-128">-Force</span></span>
<span data-ttu-id="19ec8-129">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="19ec8-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19ec8-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19ec8-130">-Name</span></span>
<span data-ttu-id="19ec8-131">Указывает имя ресурса диспетчера ресурсов Azure (ARM), представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="19ec8-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="19ec8-132">Если этот параметр не указан, этот командлет по умолчанию имеет значение "AzureDiskEncryption для ВМ для Windows".</span><span class="sxs-lookup"><span data-stu-id="19ec8-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="19ec8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19ec8-133">-ResourceGroupName</span></span>
<span data-ttu-id="19ec8-134">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="19ec8-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="19ec8-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="19ec8-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="19ec8-136">Задает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="19ec8-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="19ec8-137">Если значение для этого параметра не задано, используется самая свежая версия расширения.</span><span class="sxs-lookup"><span data-stu-id="19ec8-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="19ec8-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="19ec8-138">-VMName</span></span>
<span data-ttu-id="19ec8-139">Указывает имя виртуальной машины, для которой этот командлет отключает шифрование.</span><span class="sxs-lookup"><span data-stu-id="19ec8-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="19ec8-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="19ec8-140">-VolumeType</span></span>
<span data-ttu-id="19ec8-141">Указывает тип томов виртуальной машины для выполнения операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="19ec8-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="19ec8-142">Для виртуальных машин Windows допустимыми являются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="19ec8-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="19ec8-143">Весь</span><span class="sxs-lookup"><span data-stu-id="19ec8-143">All</span></span>
- <span data-ttu-id="19ec8-144">ОПЕРАЦИОН</span><span class="sxs-lookup"><span data-stu-id="19ec8-144">OS</span></span>
- <span data-ttu-id="19ec8-145">Сведения.</span><span class="sxs-lookup"><span data-stu-id="19ec8-145">Data.</span></span>
<span data-ttu-id="19ec8-146">Если значение для этого параметра не задано, по умолчанию используется значение ALL.</span><span class="sxs-lookup"><span data-stu-id="19ec8-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="19ec8-147">Отключение шифрования в настоящее время не поддерживается для Linux.</span><span class="sxs-lookup"><span data-stu-id="19ec8-147">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="19ec8-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19ec8-148">-Confirm</span></span>
<span data-ttu-id="19ec8-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19ec8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19ec8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19ec8-150">-WhatIf</span></span>
<span data-ttu-id="19ec8-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19ec8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19ec8-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19ec8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19ec8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ec8-153">CommonParameters</span></span>
<span data-ttu-id="19ec8-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19ec8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ec8-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19ec8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ec8-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19ec8-156">INPUTS</span></span>

### <span data-ttu-id="19ec8-157">System. String</span><span class="sxs-lookup"><span data-stu-id="19ec8-157">System.String</span></span>

### <span data-ttu-id="19ec8-158">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19ec8-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19ec8-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19ec8-159">OUTPUTS</span></span>

### <span data-ttu-id="19ec8-160">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="19ec8-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="19ec8-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="19ec8-161">NOTES</span></span>

## <span data-ttu-id="19ec8-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19ec8-162">RELATED LINKS</span></span>

[<span data-ttu-id="19ec8-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="19ec8-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="19ec8-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="19ec8-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="19ec8-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="19ec8-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


