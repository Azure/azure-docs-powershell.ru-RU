---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 2227193923b014f69da0ddb60ae9ee00bdc14b6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569660"
---
# <span data-ttu-id="b441e-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b441e-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="b441e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b441e-102">SYNOPSIS</span></span>
<span data-ttu-id="b441e-103">Отключение шифрования на виртуальной машине IaaS.</span><span class="sxs-lookup"><span data-stu-id="b441e-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b441e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b441e-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b441e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b441e-105">DESCRIPTION</span></span>
<span data-ttu-id="b441e-106">Командлет **Disable-AzureRmVMDiskEncryption** отключает шифрование инфраструктуры в качестве виртуальной машины службы (IaaS).</span><span class="sxs-lookup"><span data-stu-id="b441e-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="b441e-107">Этот командлет поддерживается только на виртуальных машинах Windows и не виртуальных машинах Linux.</span><span class="sxs-lookup"><span data-stu-id="b441e-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="b441e-108">Этот командлет устанавливает расширение на виртуальной машине, чтобы отключить шифрование.</span><span class="sxs-lookup"><span data-stu-id="b441e-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="b441e-109">Если параметр *Name* не указан, создается расширение с именем по умолчанию "AzureDiskEncryption для Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="b441e-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="b441e-110">Предупреждение: Этот командлет перезагружает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b441e-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="b441e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b441e-111">EXAMPLES</span></span>

### <span data-ttu-id="b441e-112">Пример 1: отключение шифрования для всех томов на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="b441e-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="b441e-113">Эта команда отключает шифрование для томов типа ALL для виртуальной машины с именем VM002, которая входит в группу ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="b441e-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="b441e-114">Так как параметр *VolumeType* не указан, командлет задает значение ALL.</span><span class="sxs-lookup"><span data-stu-id="b441e-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="b441e-115">Пример 2: отключение шифрования для томов данных на виртуальной машине Windows</span><span class="sxs-lookup"><span data-stu-id="b441e-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="b441e-116">Эта команда отключает шифрование томов типа "данные" для виртуальной машины с именем VM004, которая входит в группу ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="b441e-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="b441e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b441e-117">PARAMETERS</span></span>

### <span data-ttu-id="b441e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b441e-118">-DefaultProfile</span></span>
<span data-ttu-id="b441e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b441e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b441e-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b441e-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b441e-121">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="b441e-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b441e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b441e-122">-Force</span></span>
<span data-ttu-id="b441e-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b441e-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b441e-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b441e-124">-Name</span></span>
<span data-ttu-id="b441e-125">Specifes. имя ресурса диспетчера ресурсов Azure (ARM), представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="b441e-125">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="b441e-126">Если этот параметр не указан, этот командлет по умолчанию имеет значение "AzureDiskEncryption для ВМ для Windows".</span><span class="sxs-lookup"><span data-stu-id="b441e-126">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="b441e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b441e-127">-ResourceGroupName</span></span>
<span data-ttu-id="b441e-128">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b441e-128">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="b441e-129">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b441e-129">-TypeHandlerVersion</span></span>
<span data-ttu-id="b441e-130">Задает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="b441e-130">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="b441e-131">Если значение для этого параметра не задано, используется самая свежая версия расширения.</span><span class="sxs-lookup"><span data-stu-id="b441e-131">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="b441e-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="b441e-132">-VMName</span></span>
<span data-ttu-id="b441e-133">Указывает имя виртуальной машины, для которой этот командлет отключает шифрование.</span><span class="sxs-lookup"><span data-stu-id="b441e-133">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="b441e-134">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="b441e-134">-VolumeType</span></span>
<span data-ttu-id="b441e-135">Указывает тип томов виртуальной машины для выполнения операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="b441e-135">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="b441e-136">Для виртуальных машин Windows допустимыми являются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b441e-136">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="b441e-137">Весь</span><span class="sxs-lookup"><span data-stu-id="b441e-137">All</span></span>
- <span data-ttu-id="b441e-138">ОПЕРАЦИОН</span><span class="sxs-lookup"><span data-stu-id="b441e-138">OS</span></span>
- <span data-ttu-id="b441e-139">Сведения.</span><span class="sxs-lookup"><span data-stu-id="b441e-139">Data.</span></span>
<span data-ttu-id="b441e-140">Если значение для этого параметра не задано, по умолчанию используется значение ALL.</span><span class="sxs-lookup"><span data-stu-id="b441e-140">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="b441e-141">Отключение шифрования в настоящее время не поддерживается для Linux.</span><span class="sxs-lookup"><span data-stu-id="b441e-141">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="b441e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b441e-142">-Confirm</span></span>
<span data-ttu-id="b441e-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b441e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b441e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b441e-144">-WhatIf</span></span>
<span data-ttu-id="b441e-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b441e-145">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b441e-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b441e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b441e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b441e-147">CommonParameters</span></span>
<span data-ttu-id="b441e-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b441e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b441e-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b441e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b441e-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b441e-150">INPUTS</span></span>

## <span data-ttu-id="b441e-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b441e-151">OUTPUTS</span></span>

### <span data-ttu-id="b441e-152">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b441e-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b441e-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="b441e-153">NOTES</span></span>

## <span data-ttu-id="b441e-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b441e-154">RELATED LINKS</span></span>

[<span data-ttu-id="b441e-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="b441e-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="b441e-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="b441e-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="b441e-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="b441e-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


