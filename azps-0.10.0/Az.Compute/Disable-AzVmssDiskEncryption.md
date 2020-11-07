---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 43a8f6efc69113888454511faa346aea7baa837a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911565"
---
# <span data-ttu-id="da719-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="da719-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="da719-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da719-102">SYNOPSIS</span></span>
<span data-ttu-id="da719-103">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="da719-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="da719-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da719-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da719-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da719-105">DESCRIPTION</span></span>
<span data-ttu-id="da719-106">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="da719-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="da719-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da719-107">EXAMPLES</span></span>

### <span data-ttu-id="da719-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da719-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="da719-109">Отключение шифрования дисков на множестве виртуальных машин с именем VMSS001, который принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="da719-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="da719-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da719-110">PARAMETERS</span></span>

### <span data-ttu-id="da719-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da719-111">-AsJob</span></span>
<span data-ttu-id="da719-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="da719-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da719-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da719-113">-DefaultProfile</span></span>
<span data-ttu-id="da719-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da719-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da719-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="da719-115">-ExtensionName</span></span>
<span data-ttu-id="da719-116">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="da719-116">The extension name.</span></span>
<span data-ttu-id="da719-117">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="da719-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da719-118">-Force</span><span class="sxs-lookup"><span data-stu-id="da719-118">-Force</span></span>
<span data-ttu-id="da719-119">Чтобы принудительно удалить расширение с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="da719-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="da719-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="da719-120">-ForceUpdate</span></span>
<span data-ttu-id="da719-121">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="da719-121">Generate a tag for force update.</span></span>  <span data-ttu-id="da719-122">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="da719-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="da719-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da719-123">-ResourceGroupName</span></span>
<span data-ttu-id="da719-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da719-124">The resource group name.</span></span>

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

### <span data-ttu-id="da719-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="da719-125">-VMScaleSetName</span></span>
<span data-ttu-id="da719-126">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="da719-126">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da719-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="da719-127">-VolumeType</span></span>
<span data-ttu-id="da719-128">Тип тома (ОС или данных) для выполнения операции шифрования</span><span class="sxs-lookup"><span data-stu-id="da719-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da719-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da719-129">-Confirm</span></span>
<span data-ttu-id="da719-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da719-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da719-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da719-131">-WhatIf</span></span>
<span data-ttu-id="da719-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da719-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da719-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da719-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da719-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da719-134">CommonParameters</span></span>
<span data-ttu-id="da719-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da719-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da719-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da719-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da719-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da719-137">INPUTS</span></span>

### <span data-ttu-id="da719-138">System. String</span><span class="sxs-lookup"><span data-stu-id="da719-138">System.String</span></span>

## <span data-ttu-id="da719-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da719-139">OUTPUTS</span></span>

### <span data-ttu-id="da719-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="da719-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="da719-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="da719-141">NOTES</span></span>

## <span data-ttu-id="da719-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da719-142">RELATED LINKS</span></span>

