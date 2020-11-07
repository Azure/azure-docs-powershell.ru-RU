---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 17da84f942b5911d8302b62ec8b8cecdbe080c43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732799"
---
# <span data-ttu-id="97549-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="97549-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="97549-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97549-102">SYNOPSIS</span></span>
<span data-ttu-id="97549-103">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="97549-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97549-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97549-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97549-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97549-105">DESCRIPTION</span></span>
<span data-ttu-id="97549-106">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="97549-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="97549-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97549-107">EXAMPLES</span></span>

### <span data-ttu-id="97549-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="97549-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="97549-109">Отключение шифрования дисков на множестве виртуальных машин с именем VMSS001, который принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="97549-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="97549-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97549-110">PARAMETERS</span></span>

### <span data-ttu-id="97549-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97549-111">-AsJob</span></span>
<span data-ttu-id="97549-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="97549-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97549-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97549-113">-DefaultProfile</span></span>
<span data-ttu-id="97549-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97549-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97549-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="97549-115">-ExtensionName</span></span>
<span data-ttu-id="97549-116">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="97549-116">The extension name.</span></span>
<span data-ttu-id="97549-117">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="97549-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97549-118">-Force</span><span class="sxs-lookup"><span data-stu-id="97549-118">-Force</span></span>
<span data-ttu-id="97549-119">Чтобы принудительно удалить расширение с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="97549-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="97549-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="97549-120">-ForceUpdate</span></span>
<span data-ttu-id="97549-121">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="97549-121">Generate a tag for force update.</span></span>  <span data-ttu-id="97549-122">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="97549-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="97549-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97549-123">-ResourceGroupName</span></span>
<span data-ttu-id="97549-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97549-124">The resource group name.</span></span>

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

### <span data-ttu-id="97549-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="97549-125">-VMScaleSetName</span></span>
<span data-ttu-id="97549-126">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="97549-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="97549-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="97549-127">-VolumeType</span></span>
<span data-ttu-id="97549-128">Тип тома (ОС или данных) для выполнения операции шифрования</span><span class="sxs-lookup"><span data-stu-id="97549-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="97549-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97549-129">-Confirm</span></span>
<span data-ttu-id="97549-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="97549-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97549-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97549-131">-WhatIf</span></span>
<span data-ttu-id="97549-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="97549-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97549-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="97549-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97549-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97549-134">CommonParameters</span></span>
<span data-ttu-id="97549-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97549-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97549-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97549-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97549-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97549-137">INPUTS</span></span>

### <span data-ttu-id="97549-138">System. String</span><span class="sxs-lookup"><span data-stu-id="97549-138">System.String</span></span>

### <span data-ttu-id="97549-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97549-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97549-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97549-140">OUTPUTS</span></span>

### <span data-ttu-id="97549-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="97549-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="97549-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="97549-142">NOTES</span></span>

## <span data-ttu-id="97549-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97549-143">RELATED LINKS</span></span>
