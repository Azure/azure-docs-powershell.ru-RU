---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 084775812a887e0cc6fe497a0e0cef46ec464956
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721762"
---
# <span data-ttu-id="567e9-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="567e9-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="567e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="567e9-102">SYNOPSIS</span></span>
<span data-ttu-id="567e9-103">Удаляет расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="567e9-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="567e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="567e9-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="567e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="567e9-105">DESCRIPTION</span></span>
<span data-ttu-id="567e9-106">Командлет **Remove-AzVMDiskEncryptionExtension** удаляет расширение шифрования диска и связанную конфигурацию расширения с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="567e9-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="567e9-107">Если имя расширения не задано, этот командлет удаляет расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="567e9-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="567e9-108">Этот командлет завершится сбоем, если шифрование на виртуальной машине не было первоначально отключено.</span><span class="sxs-lookup"><span data-stu-id="567e9-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="567e9-109">Чтобы отключить шифрование на виртуальной машине, используйте команду [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span><span class="sxs-lookup"><span data-stu-id="567e9-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="567e9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="567e9-110">EXAMPLES</span></span>

### <span data-ttu-id="567e9-111">Пример 1: Удалите расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="567e9-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="567e9-112">Эта команда удаляет расширение с именем по умолчанию AzureDiskEncryption для виртуальной машины под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальной машины на базе Linux с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="567e9-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="567e9-113">Пример 2: удаление определенного расширения шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="567e9-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="567e9-114">Эта команда удаляет расширение шифрования с именем MyDiskEncryptionExtension из виртуальной машины с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="567e9-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="567e9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="567e9-115">PARAMETERS</span></span>

### <span data-ttu-id="567e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567e9-116">-DefaultProfile</span></span>
<span data-ttu-id="567e9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="567e9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="567e9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="567e9-118">-Force</span></span>
<span data-ttu-id="567e9-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="567e9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="567e9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="567e9-120">-Name</span></span>
<span data-ttu-id="567e9-121">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="567e9-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="567e9-122">Командлет Set-AzVMDiskEncryptionExtension задает для этого имени имя AzureDiskEncryption виртуальных машин, работающих под управлением операционной системы Windows и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="567e9-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="567e9-123">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете **Set-AzVMDiskEncryptionExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="567e9-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567e9-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="567e9-124">-NoWait</span></span>
<span data-ttu-id="567e9-125">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="567e9-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="567e9-126">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="567e9-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="567e9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567e9-127">-ResourceGroupName</span></span>
<span data-ttu-id="567e9-128">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="567e9-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="567e9-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="567e9-129">-VMName</span></span>
<span data-ttu-id="567e9-130">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="567e9-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="567e9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="567e9-131">-Confirm</span></span>
<span data-ttu-id="567e9-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="567e9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="567e9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="567e9-133">-WhatIf</span></span>
<span data-ttu-id="567e9-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="567e9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="567e9-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="567e9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="567e9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567e9-136">CommonParameters</span></span>
<span data-ttu-id="567e9-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="567e9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567e9-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="567e9-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567e9-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="567e9-139">INPUTS</span></span>

### <span data-ttu-id="567e9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="567e9-140">System.String</span></span>

## <span data-ttu-id="567e9-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="567e9-141">OUTPUTS</span></span>

### <span data-ttu-id="567e9-142">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="567e9-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="567e9-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="567e9-143">NOTES</span></span>

## <span data-ttu-id="567e9-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="567e9-144">RELATED LINKS</span></span>

[<span data-ttu-id="567e9-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="567e9-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="567e9-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="567e9-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


