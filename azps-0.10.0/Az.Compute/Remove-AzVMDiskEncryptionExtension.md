---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 51b1273e5c44756df56177878dbe4fbc9563ec2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911413"
---
# <span data-ttu-id="4e177-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="4e177-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="4e177-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e177-102">SYNOPSIS</span></span>
<span data-ttu-id="4e177-103">Удаляет расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e177-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="4e177-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e177-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e177-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e177-105">DESCRIPTION</span></span>
<span data-ttu-id="4e177-106">Командлет **Remove-AzVMDiskEncryptionExtension** удаляет расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e177-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="4e177-107">Если имя расширения не задано, этот командлет удаляет расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="4e177-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="4e177-108">Этот командлет не отключает шифрование на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4e177-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="4e177-109">Она удаляет расширение и связанную конфигурацию расширения из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e177-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="4e177-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e177-110">EXAMPLES</span></span>

### <span data-ttu-id="4e177-111">Пример 1: Удалите расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e177-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="4e177-112">Эта команда удаляет расширение с именем по умолчанию AzureDiskEncryption для виртуальной машины под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальной машины на базе Linux с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="4e177-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="4e177-113">Пример 2: удаление определенного расширения шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e177-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="4e177-114">Эта команда удаляет расширение шифрования с именем MyDiskEncryptionExtension из виртуальной машины с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="4e177-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="4e177-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e177-115">PARAMETERS</span></span>

### <span data-ttu-id="4e177-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e177-116">-DefaultProfile</span></span>
<span data-ttu-id="4e177-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e177-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e177-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4e177-118">-Force</span></span>
<span data-ttu-id="4e177-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e177-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4e177-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e177-120">-Name</span></span>
<span data-ttu-id="4e177-121">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="4e177-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="4e177-122">Командлет Set-AzVMDiskEncryptionExtension задает для этого имени имя AzureDiskEncryption виртуальных машин, работающих под управлением операционной системы Windows и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="4e177-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="4e177-123">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете **Set-AzVMDiskEncryptionExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e177-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e177-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e177-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e177-125">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e177-125">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="4e177-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="4e177-126">-VMName</span></span>
<span data-ttu-id="4e177-127">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e177-127">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="4e177-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e177-128">-Confirm</span></span>
<span data-ttu-id="4e177-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e177-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e177-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e177-130">-WhatIf</span></span>
<span data-ttu-id="4e177-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e177-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4e177-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e177-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e177-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e177-133">CommonParameters</span></span>
<span data-ttu-id="4e177-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e177-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e177-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e177-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e177-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e177-136">INPUTS</span></span>

### <span data-ttu-id="4e177-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="4e177-137">None</span></span>
<span data-ttu-id="4e177-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4e177-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e177-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e177-139">OUTPUTS</span></span>

### <span data-ttu-id="4e177-140">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4e177-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4e177-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e177-141">NOTES</span></span>

## <span data-ttu-id="4e177-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e177-142">RELATED LINKS</span></span>

[<span data-ttu-id="4e177-143">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="4e177-143">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="4e177-144">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="4e177-144">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


