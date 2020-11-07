---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 6a14a8472ca33fe9dbb15aa2ddf58208764a5a6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911568"
---
# <span data-ttu-id="1ee9c-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1ee9c-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="1ee9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ee9c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee9c-103">Отключение шифрования на виртуальной машине IaaS.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="1ee9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ee9c-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ee9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee9c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee9c-106">Командлет **Disable-AzVMDiskEncryption** отключает шифрование инфраструктуры в качестве виртуальной машины службы (IaaS).</span><span class="sxs-lookup"><span data-stu-id="1ee9c-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="1ee9c-107">Этот командлет поддерживается только на виртуальных машинах Windows и не виртуальных машинах Linux.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="1ee9c-108">Этот командлет устанавливает расширение на виртуальной машине, чтобы отключить шифрование.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="1ee9c-109">Если параметр *Name* не указан, создается расширение с именем по умолчанию "AzureDiskEncryption для Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="1ee9c-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="1ee9c-110">Предупреждение: Этот командлет перезагружает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="1ee9c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ee9c-111">EXAMPLES</span></span>

### <span data-ttu-id="1ee9c-112">Пример 1: отключение шифрования для всех томов на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="1ee9c-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="1ee9c-113">Эта команда отключает шифрование для томов типа ALL для виртуальной машины с именем VM002, которая входит в группу ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="1ee9c-114">Так как параметр *VolumeType* не указан, командлет задает значение ALL.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="1ee9c-115">Пример 2: отключение шифрования для томов данных на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="1ee9c-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="1ee9c-116">Эта команда отключает шифрование томов типа "данные" для виртуальной машины с именем VM004, которая входит в группу ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="1ee9c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ee9c-117">PARAMETERS</span></span>

### <span data-ttu-id="1ee9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee9c-118">-DefaultProfile</span></span>
<span data-ttu-id="1ee9c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ee9c-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1ee9c-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1ee9c-121">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="1ee9c-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="1ee9c-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="1ee9c-123">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-123">The extension publisher name.</span></span> <span data-ttu-id="1ee9c-124">Указывайте этот параметр только для переопределения значения по умолчанию Microsoft. Azure. Security.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="1ee9c-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="1ee9c-125">-ExtensionType</span></span>
<span data-ttu-id="1ee9c-126">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-126">The extension type.</span></span> <span data-ttu-id="1ee9c-127">Укажите этот параметр для переопределения значения по умолчанию "AzureDiskEncryption" для виртуальных машин и "AzureDiskEncryptionForLinux" для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="1ee9c-128">-Force</span><span class="sxs-lookup"><span data-stu-id="1ee9c-128">-Force</span></span>
<span data-ttu-id="1ee9c-129">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ee9c-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ee9c-130">-Name</span></span>
<span data-ttu-id="1ee9c-131">Specifes. имя ресурса диспетчера ресурсов Azure (ARM), представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-131">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="1ee9c-132">Если этот параметр не указан, этот командлет по умолчанию имеет значение "AzureDiskEncryption для ВМ для Windows".</span><span class="sxs-lookup"><span data-stu-id="1ee9c-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee9c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ee9c-133">-ResourceGroupName</span></span>
<span data-ttu-id="1ee9c-134">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="1ee9c-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1ee9c-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="1ee9c-136">Задает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="1ee9c-137">Если значение для этого параметра не задано, используется самая свежая версия расширения.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee9c-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="1ee9c-138">-VMName</span></span>
<span data-ttu-id="1ee9c-139">Указывает имя виртуальной машины, для которой этот командлет отключает шифрование.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee9c-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="1ee9c-140">-VolumeType</span></span>
<span data-ttu-id="1ee9c-141">Указывает тип томов виртуальной машины для выполнения операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="1ee9c-142">Для виртуальных машин Windows допустимыми являются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1ee9c-142">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="1ee9c-143">Весь</span><span class="sxs-lookup"><span data-stu-id="1ee9c-143">All</span></span>
- <span data-ttu-id="1ee9c-144">ОПЕРАЦИОН</span><span class="sxs-lookup"><span data-stu-id="1ee9c-144">OS</span></span>
- <span data-ttu-id="1ee9c-145">Сведения.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-145">Data.</span></span>
<span data-ttu-id="1ee9c-146">Если значение для этого параметра не задано, по умолчанию используется значение ALL.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="1ee9c-147">Отключение шифрования в настоящее время не поддерживается для Linux.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee9c-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ee9c-148">-Confirm</span></span>
<span data-ttu-id="1ee9c-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee9c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee9c-150">-WhatIf</span></span>
<span data-ttu-id="1ee9c-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1ee9c-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee9c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee9c-153">CommonParameters</span></span>
<span data-ttu-id="1ee9c-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee9c-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee9c-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee9c-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ee9c-156">INPUTS</span></span>

### <span data-ttu-id="1ee9c-157">Ничего</span><span class="sxs-lookup"><span data-stu-id="1ee9c-157">None</span></span>
<span data-ttu-id="1ee9c-158">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ee9c-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee9c-159">OUTPUTS</span></span>

### <span data-ttu-id="1ee9c-160">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-160">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1ee9c-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ee9c-161">NOTES</span></span>

## <span data-ttu-id="1ee9c-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ee9c-162">RELATED LINKS</span></span>

[<span data-ttu-id="1ee9c-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="1ee9c-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="1ee9c-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1ee9c-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="1ee9c-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1ee9c-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


