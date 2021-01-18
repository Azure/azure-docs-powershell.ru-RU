---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519519"
---
# <span data-ttu-id="a7d70-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a7d70-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="a7d70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d70-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d70-103">Удаляет расширение шифрования диска с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7d70-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="a7d70-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7d70-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7d70-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7d70-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d70-106">При **этом из виртуальной** машины удаляются расширение шифрования диска и связанная с ней конфигурация расширения.</span><span class="sxs-lookup"><span data-stu-id="a7d70-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="a7d70-107">Если имя расширения не задано, этот cmdlet удаляет расширение со стандартным именем AzureDiskEncryption для виртуальных машин, которые запускают операционную систему Windows или виртуальные машины на базе AzureDiskEncryptionForLinux для Linux.</span><span class="sxs-lookup"><span data-stu-id="a7d70-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="a7d70-108">Если шифрование на виртуальной машине не было сначала отключено, происходит сбой этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d70-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="a7d70-109">Чтобы отключить шифрование на виртуальной машине, используйте [disable-AzVMDiskEncryption.](./Disable-AzVMDiskEncryption.md)</span><span class="sxs-lookup"><span data-stu-id="a7d70-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="a7d70-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7d70-110">EXAMPLES</span></span>

### <span data-ttu-id="a7d70-111">Пример 1. Удаление расширения шифрования диска с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7d70-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="a7d70-112">Эта команда удаляет расширение со стандартным именем AzureDiskEncryption для виртуальной машины, которая работает в операционной системе Windows, или виртуальной машины На базе AzureDiskEncryptionForLinux для Linux с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="a7d70-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="a7d70-113">Пример 2. Удаление определенного расширения шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7d70-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="a7d70-114">Эта команда удаляет расширение шифрования MyDiskEncryptionExtension с виртуальной машины MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="a7d70-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="a7d70-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7d70-115">PARAMETERS</span></span>

### <span data-ttu-id="a7d70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d70-116">-DefaultProfile</span></span>
<span data-ttu-id="a7d70-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d70-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d70-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a7d70-118">-Force</span></span>
<span data-ttu-id="a7d70-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a7d70-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7d70-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a7d70-120">-Name</span></span>
<span data-ttu-id="a7d70-121">Имя ресурса Диспетчера ресурсов Azure, представляюца расширение.</span><span class="sxs-lookup"><span data-stu-id="a7d70-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="a7d70-122">Этот Set-AzVMDiskEncryptionExtension задает для этого имени службу AzureDiskEncryption для виртуальных машин, работающих с операционной системой Windows и виртуальными машинами AzureDiskEncryptionForLinux для Linux.</span><span class="sxs-lookup"><span data-stu-id="a7d70-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="a7d70-123">Укажите этот параметр только в том случае, если вы изменили имя по умолчанию в проектлете **Set-AzVMDiskEncryptionExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7d70-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="a7d70-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7d70-124">-NoWait</span></span>
<span data-ttu-id="a7d70-125">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="a7d70-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a7d70-126">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="a7d70-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a7d70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d70-127">-ResourceGroupName</span></span>
<span data-ttu-id="a7d70-128">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7d70-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="a7d70-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="a7d70-129">-VMName</span></span>
<span data-ttu-id="a7d70-130">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7d70-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="a7d70-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7d70-131">-Confirm</span></span>
<span data-ttu-id="a7d70-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a7d70-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d70-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d70-133">-WhatIf</span></span>
<span data-ttu-id="a7d70-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d70-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7d70-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7d70-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7d70-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d70-136">CommonParameters</span></span>
<span data-ttu-id="a7d70-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d70-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d70-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7d70-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d70-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7d70-139">INPUTS</span></span>

### <span data-ttu-id="a7d70-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d70-140">System.String</span></span>

## <span data-ttu-id="a7d70-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7d70-141">OUTPUTS</span></span>

### <span data-ttu-id="a7d70-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a7d70-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a7d70-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7d70-143">NOTES</span></span>

## <span data-ttu-id="a7d70-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7d70-144">RELATED LINKS</span></span>

[<span data-ttu-id="a7d70-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="a7d70-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="a7d70-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a7d70-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


