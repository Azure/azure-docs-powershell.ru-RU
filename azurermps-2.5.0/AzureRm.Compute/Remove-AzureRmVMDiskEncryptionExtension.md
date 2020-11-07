---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 6c580b862ed2c8a420e8f203131ff9d18d187443
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914214"
---
# <span data-ttu-id="bc5d9-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bc5d9-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="bc5d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5d9-103">Удаляет расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc5d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc5d9-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5d9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5d9-106">Командлет **Remove-AzureRmVMDiskEncryptionExtension** удаляет расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="bc5d9-107">Если имя расширения не задано, этот командлет удаляет расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="bc5d9-108">Этот командлет не отключает шифрование на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="bc5d9-109">Она удаляет расширение и связанную конфигурацию расширения из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="bc5d9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc5d9-110">EXAMPLES</span></span>

### <span data-ttu-id="bc5d9-111">Пример 1: Удалите расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="bc5d9-112">Эта команда удаляет расширение с именем по умолчанию AzureDiskEncryption для виртуальной машины под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальной машины на базе Linux с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="bc5d9-113">Пример 2: удаление определенного расширения шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="bc5d9-114">Эта команда удаляет расширение шифрования с именем MyDiskEncryptionExtension из виртуальной машины с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="bc5d9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc5d9-115">PARAMETERS</span></span>

### <span data-ttu-id="bc5d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5d9-116">-DefaultProfile</span></span>
<span data-ttu-id="bc5d9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc5d9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bc5d9-118">-Force</span></span>
<span data-ttu-id="bc5d9-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc5d9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc5d9-120">-Name</span></span>
<span data-ttu-id="bc5d9-121">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="bc5d9-122">Командлет Set-AzureRmVMDiskEncryptionExtension задает для этого имени имя AzureDiskEncryption виртуальных машин, работающих под управлением операционной системы Windows и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="bc5d9-123">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете **Set-AzureRmVMDiskEncryptionExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="bc5d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc5d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc5d9-125">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-125">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="bc5d9-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="bc5d9-126">-VMName</span></span>
<span data-ttu-id="bc5d9-127">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-127">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="bc5d9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc5d9-128">-Confirm</span></span>
<span data-ttu-id="bc5d9-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc5d9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5d9-130">-WhatIf</span></span>
<span data-ttu-id="bc5d9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bc5d9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc5d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5d9-133">CommonParameters</span></span>
<span data-ttu-id="bc5d9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5d9-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc5d9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5d9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc5d9-136">INPUTS</span></span>

### <span data-ttu-id="bc5d9-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="bc5d9-137">None</span></span>
<span data-ttu-id="bc5d9-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc5d9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc5d9-139">OUTPUTS</span></span>

### <span data-ttu-id="bc5d9-140">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bc5d9-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bc5d9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc5d9-141">NOTES</span></span>

## <span data-ttu-id="bc5d9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc5d9-142">RELATED LINKS</span></span>

[<span data-ttu-id="bc5d9-143">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="bc5d9-143">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="bc5d9-144">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bc5d9-144">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


