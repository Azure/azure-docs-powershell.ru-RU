---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 14f29bb7097f584c89fa1bf92bf816cf4ca3d511
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074652"
---
# <span data-ttu-id="34b2a-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="34b2a-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="34b2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="34b2a-103">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="34b2a-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="34b2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34b2a-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34b2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34b2a-105">DESCRIPTION</span></span>
<span data-ttu-id="34b2a-106">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="34b2a-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="34b2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34b2a-107">EXAMPLES</span></span>

### <span data-ttu-id="34b2a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34b2a-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="34b2a-109">Отключение шифрования дисков на множестве виртуальных машин с именем VMSS001, который принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="34b2a-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="34b2a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34b2a-110">PARAMETERS</span></span>

### <span data-ttu-id="34b2a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34b2a-111">-AsJob</span></span>
<span data-ttu-id="34b2a-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="34b2a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34b2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b2a-113">-DefaultProfile</span></span>
<span data-ttu-id="34b2a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34b2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34b2a-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="34b2a-115">-ExtensionName</span></span>
<span data-ttu-id="34b2a-116">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="34b2a-116">The extension name.</span></span>
<span data-ttu-id="34b2a-117">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="34b2a-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="34b2a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="34b2a-118">-Force</span></span>
<span data-ttu-id="34b2a-119">Чтобы принудительно удалить расширение с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="34b2a-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="34b2a-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="34b2a-120">-ForceUpdate</span></span>
<span data-ttu-id="34b2a-121">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="34b2a-121">Generate a tag for force update.</span></span>  <span data-ttu-id="34b2a-122">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="34b2a-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="34b2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="34b2a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34b2a-124">The resource group name.</span></span>

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

### <span data-ttu-id="34b2a-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="34b2a-125">-VMScaleSetName</span></span>
<span data-ttu-id="34b2a-126">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="34b2a-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="34b2a-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="34b2a-127">-VolumeType</span></span>
<span data-ttu-id="34b2a-128">Тип тома (ОС или данных) для выполнения операции шифрования</span><span class="sxs-lookup"><span data-stu-id="34b2a-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="34b2a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34b2a-129">-Confirm</span></span>
<span data-ttu-id="34b2a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34b2a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34b2a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b2a-131">-WhatIf</span></span>
<span data-ttu-id="34b2a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34b2a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34b2a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34b2a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34b2a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b2a-134">CommonParameters</span></span>
<span data-ttu-id="34b2a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34b2a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b2a-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34b2a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b2a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34b2a-137">INPUTS</span></span>

### <span data-ttu-id="34b2a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="34b2a-138">System.String</span></span>

### <span data-ttu-id="34b2a-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="34b2a-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="34b2a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34b2a-140">OUTPUTS</span></span>

### <span data-ttu-id="34b2a-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34b2a-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="34b2a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="34b2a-142">NOTES</span></span>

## <span data-ttu-id="34b2a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34b2a-143">RELATED LINKS</span></span>
