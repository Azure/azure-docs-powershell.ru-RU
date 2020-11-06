---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564992"
---
# <span data-ttu-id="c2c37-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c2c37-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="c2c37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2c37-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c37-103">Отключение шифрования на виртуальной машине IaaS.</span><span class="sxs-lookup"><span data-stu-id="c2c37-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2c37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2c37-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2c37-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2c37-105">DESCRIPTION</span></span>
<span data-ttu-id="c2c37-106">Командлет **Disable-AzureRmVMDiskEncryption** отключает шифрование инфраструктуры в качестве виртуальной машины службы (IaaS).</span><span class="sxs-lookup"><span data-stu-id="c2c37-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="c2c37-107">Этот командлет поддерживается только на виртуальных машинах Windows и не виртуальных машинах Linux.</span><span class="sxs-lookup"><span data-stu-id="c2c37-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="c2c37-108">Этот командлет устанавливает расширение на виртуальной машине, чтобы отключить шифрование.</span><span class="sxs-lookup"><span data-stu-id="c2c37-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="c2c37-109">Если параметр *Name* не указан, создается расширение с именем по умолчанию "AzureDiskEncryption для Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="c2c37-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="c2c37-110">Предупреждение: Этот командлет перезагружает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="c2c37-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="c2c37-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2c37-111">EXAMPLES</span></span>

### <span data-ttu-id="c2c37-112">Пример 1: отключение шифрования для всех томов на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="c2c37-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="c2c37-113">Эта команда отключает шифрование для томов типа ALL для виртуальной машины с именем VM002, которая входит в группу ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="c2c37-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="c2c37-114">Так как параметр *VolumeType* не указан, командлет задает значение ALL.</span><span class="sxs-lookup"><span data-stu-id="c2c37-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="c2c37-115">Пример 2: отключение шифрования для томов данных на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="c2c37-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="c2c37-116">Эта команда отключает шифрование томов типа "данные" для виртуальной машины с именем VM004, которая входит в группу ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="c2c37-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="c2c37-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2c37-117">PARAMETERS</span></span>

### <span data-ttu-id="c2c37-118">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c2c37-118">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c2c37-119">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="c2c37-119">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c37-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c2c37-120">-Force</span></span>
<span data-ttu-id="c2c37-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2c37-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2c37-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2c37-122">-Name</span></span>
<span data-ttu-id="c2c37-123">Specifes. имя ресурса диспетчера ресурсов Azure (ARM), представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="c2c37-123">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="c2c37-124">Если этот параметр не указан, этот командлет по умолчанию имеет значение "AzureDiskEncryption для ВМ для Windows".</span><span class="sxs-lookup"><span data-stu-id="c2c37-124">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="c2c37-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c37-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2c37-126">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c2c37-126">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="c2c37-127">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c2c37-127">-TypeHandlerVersion</span></span>
<span data-ttu-id="c2c37-128">Задает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="c2c37-128">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="c2c37-129">Если значение для этого параметра не задано, используется самая свежая версия расширения.</span><span class="sxs-lookup"><span data-stu-id="c2c37-129">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="c2c37-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="c2c37-130">-VMName</span></span>
<span data-ttu-id="c2c37-131">Указывает имя виртуальной машины, для которой этот командлет отключает шифрование.</span><span class="sxs-lookup"><span data-stu-id="c2c37-131">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="c2c37-132">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="c2c37-132">-VolumeType</span></span>
<span data-ttu-id="c2c37-133">Указывает тип томов виртуальной машины для выполнения операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="c2c37-133">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="c2c37-134">Для виртуальных машин Windows допустимыми являются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2c37-134">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="c2c37-135">Весь</span><span class="sxs-lookup"><span data-stu-id="c2c37-135">All</span></span>
- <span data-ttu-id="c2c37-136">ОПЕРАЦИОН</span><span class="sxs-lookup"><span data-stu-id="c2c37-136">OS</span></span>
- <span data-ttu-id="c2c37-137">Сведения.</span><span class="sxs-lookup"><span data-stu-id="c2c37-137">Data.</span></span>
<span data-ttu-id="c2c37-138">Если значение для этого параметра не задано, по умолчанию используется значение ALL.</span><span class="sxs-lookup"><span data-stu-id="c2c37-138">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="c2c37-139">Отключение шифрования в настоящее время не поддерживается для Linux.</span><span class="sxs-lookup"><span data-stu-id="c2c37-139">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="c2c37-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2c37-140">-Confirm</span></span>
<span data-ttu-id="c2c37-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2c37-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2c37-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c37-142">-WhatIf</span></span>
<span data-ttu-id="c2c37-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2c37-143">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c2c37-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2c37-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2c37-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c37-145">CommonParameters</span></span>
<span data-ttu-id="c2c37-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2c37-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c37-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c37-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c37-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2c37-148">INPUTS</span></span>

### <span data-ttu-id="c2c37-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="c2c37-149">None</span></span>
<span data-ttu-id="c2c37-150">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c2c37-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c2c37-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2c37-151">OUTPUTS</span></span>

### <span data-ttu-id="c2c37-152">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c2c37-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c2c37-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2c37-153">NOTES</span></span>

## <span data-ttu-id="c2c37-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2c37-154">RELATED LINKS</span></span>

[<span data-ttu-id="c2c37-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="c2c37-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="c2c37-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c2c37-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="c2c37-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c2c37-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


