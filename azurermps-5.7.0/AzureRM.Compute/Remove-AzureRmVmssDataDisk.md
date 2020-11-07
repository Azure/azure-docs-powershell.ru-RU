---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732033"
---
# <span data-ttu-id="0f002-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="0f002-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="0f002-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f002-102">SYNOPSIS</span></span>
<span data-ttu-id="0f002-103">Удаляет диск с данными из VMSS.</span><span class="sxs-lookup"><span data-stu-id="0f002-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f002-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f002-104">SYNTAX</span></span>

### <span data-ttu-id="0f002-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f002-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f002-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f002-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f002-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f002-107">DESCRIPTION</span></span>
<span data-ttu-id="0f002-108">Командлет **Remove-AzureRmVmssDataDisk** удаляет диск с данными из экземпляра установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0f002-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0f002-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f002-109">EXAMPLES</span></span>

### <span data-ttu-id="0f002-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f002-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="0f002-111">Эта команда удаляет диск данных с именем "DataDisk1" из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="0f002-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="0f002-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0f002-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="0f002-113">Эта команда удаляет диск с данными LUN 0 из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="0f002-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="0f002-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f002-114">PARAMETERS</span></span>

### <span data-ttu-id="0f002-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="0f002-115">-Lun</span></span>
<span data-ttu-id="0f002-116">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="0f002-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f002-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f002-117">-Name</span></span>
<span data-ttu-id="0f002-118">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="0f002-118">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f002-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0f002-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0f002-120">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="0f002-120">Specify the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f002-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f002-121">-Confirm</span></span>
<span data-ttu-id="0f002-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f002-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f002-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f002-123">-WhatIf</span></span>
<span data-ttu-id="0f002-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f002-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f002-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f002-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f002-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f002-126">CommonParameters</span></span>
<span data-ttu-id="0f002-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f002-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f002-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f002-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f002-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f002-129">INPUTS</span></span>

### <span data-ttu-id="0f002-130">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0f002-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="0f002-131">System. String System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0f002-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0f002-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f002-132">OUTPUTS</span></span>

### <span data-ttu-id="0f002-133">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0f002-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="0f002-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f002-134">NOTES</span></span>

## <span data-ttu-id="0f002-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f002-135">RELATED LINKS</span></span>

