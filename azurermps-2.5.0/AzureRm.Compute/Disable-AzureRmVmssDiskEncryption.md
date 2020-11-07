---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: b130be059432a6ca21fb0c1669660ebed34c670e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914629"
---
# <span data-ttu-id="b4689-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b4689-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="b4689-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4689-102">SYNOPSIS</span></span>
<span data-ttu-id="b4689-103">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b4689-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4689-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4689-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4689-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4689-105">DESCRIPTION</span></span>
<span data-ttu-id="b4689-106">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b4689-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="b4689-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4689-107">EXAMPLES</span></span>

### <span data-ttu-id="b4689-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4689-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b4689-109">Отключение шифрования дисков на множестве виртуальных машин с именем VMSS001, который принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="b4689-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b4689-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4689-110">PARAMETERS</span></span>

### <span data-ttu-id="b4689-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4689-111">-AsJob</span></span>
<span data-ttu-id="b4689-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b4689-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4689-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4689-113">-DefaultProfile</span></span>
<span data-ttu-id="b4689-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4689-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4689-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="b4689-115">-ExtensionName</span></span>
<span data-ttu-id="b4689-116">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="b4689-116">The extension name.</span></span>
<span data-ttu-id="b4689-117">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="b4689-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="b4689-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b4689-118">-Force</span></span>
<span data-ttu-id="b4689-119">Чтобы принудительно удалить расширение с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b4689-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="b4689-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="b4689-120">-ForceUpdate</span></span>
<span data-ttu-id="b4689-121">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="b4689-121">Generate a tag for force update.</span></span>  <span data-ttu-id="b4689-122">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b4689-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="b4689-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4689-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4689-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4689-124">The resource group name.</span></span>

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

### <span data-ttu-id="b4689-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b4689-125">-VMScaleSetName</span></span>
<span data-ttu-id="b4689-126">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b4689-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="b4689-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="b4689-127">-VolumeType</span></span>
<span data-ttu-id="b4689-128">Тип тома (ОС или данных) для выполнения операции шифрования</span><span class="sxs-lookup"><span data-stu-id="b4689-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="b4689-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4689-129">-Confirm</span></span>
<span data-ttu-id="b4689-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4689-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4689-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4689-131">-WhatIf</span></span>
<span data-ttu-id="b4689-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4689-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4689-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4689-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4689-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4689-134">CommonParameters</span></span>
<span data-ttu-id="b4689-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4689-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4689-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4689-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4689-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4689-137">INPUTS</span></span>

### <span data-ttu-id="b4689-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b4689-138">System.String</span></span>

## <span data-ttu-id="b4689-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4689-139">OUTPUTS</span></span>

### <span data-ttu-id="b4689-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4689-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b4689-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4689-141">NOTES</span></span>

## <span data-ttu-id="b4689-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4689-142">RELATED LINKS</span></span>

