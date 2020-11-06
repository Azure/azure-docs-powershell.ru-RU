---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 8cb68b45637496cb87e387c6755fe861fe3e21f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569659"
---
# <span data-ttu-id="60228-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="60228-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="60228-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60228-102">SYNOPSIS</span></span>
<span data-ttu-id="60228-103">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60228-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60228-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60228-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60228-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60228-105">DESCRIPTION</span></span>
<span data-ttu-id="60228-106">Отключение шифрования дисков на наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="60228-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="60228-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60228-107">EXAMPLES</span></span>

### <span data-ttu-id="60228-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60228-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="60228-109">Отключение шифрования дисков на множестве виртуальных машин с именем VMSS001, который принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="60228-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="60228-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60228-110">PARAMETERS</span></span>

### <span data-ttu-id="60228-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60228-111">-DefaultProfile</span></span>
<span data-ttu-id="60228-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60228-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60228-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="60228-113">-ExtensionName</span></span>
<span data-ttu-id="60228-114">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="60228-114">The extension name.</span></span>
<span data-ttu-id="60228-115">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="60228-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="60228-116">-Force</span><span class="sxs-lookup"><span data-stu-id="60228-116">-Force</span></span>
<span data-ttu-id="60228-117">Чтобы принудительно удалить расширение с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="60228-117">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="60228-118">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="60228-118">-ForceUpdate</span></span>
<span data-ttu-id="60228-119">Создание тега для принудительного обновления.</span><span class="sxs-lookup"><span data-stu-id="60228-119">Generate a tag for force update.</span></span>  <span data-ttu-id="60228-120">Это должно быть предоставлено для выполнения повторяющихся операций шифрования в той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="60228-120">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="60228-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60228-121">-ResourceGroupName</span></span>
<span data-ttu-id="60228-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60228-122">The resource group name.</span></span>

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

### <span data-ttu-id="60228-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="60228-123">-VMScaleSetName</span></span>
<span data-ttu-id="60228-124">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="60228-124">The virtual machine name.</span></span>

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

### <span data-ttu-id="60228-125">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="60228-125">-VolumeType</span></span>
<span data-ttu-id="60228-126">Тип тома (ОС или данных) для выполнения операции шифрования</span><span class="sxs-lookup"><span data-stu-id="60228-126">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="60228-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60228-127">-Confirm</span></span>
<span data-ttu-id="60228-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60228-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60228-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60228-129">-WhatIf</span></span>
<span data-ttu-id="60228-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60228-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60228-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60228-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60228-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60228-132">CommonParameters</span></span>
<span data-ttu-id="60228-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60228-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60228-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60228-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60228-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60228-135">INPUTS</span></span>

### <span data-ttu-id="60228-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60228-136">System.String</span></span>

## <span data-ttu-id="60228-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60228-137">OUTPUTS</span></span>

### <span data-ttu-id="60228-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="60228-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="60228-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="60228-139">NOTES</span></span>

## <span data-ttu-id="60228-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60228-140">RELATED LINKS</span></span>

