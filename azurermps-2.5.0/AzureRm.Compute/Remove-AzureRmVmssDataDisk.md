---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: 411e822153c0b95bbf30829f8da915039d01ea32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913392"
---
# <span data-ttu-id="90656-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="90656-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="90656-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90656-102">SYNOPSIS</span></span>
<span data-ttu-id="90656-103">Удаляет диск с данными из VMSS.</span><span class="sxs-lookup"><span data-stu-id="90656-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90656-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90656-104">SYNTAX</span></span>

### <span data-ttu-id="90656-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="90656-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90656-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="90656-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90656-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90656-107">DESCRIPTION</span></span>
<span data-ttu-id="90656-108">Командлет **Remove-AzureRmVmssDataDisk** удаляет диск с данными из экземпляра установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="90656-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="90656-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90656-109">EXAMPLES</span></span>

### <span data-ttu-id="90656-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90656-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="90656-111">Эта команда удаляет диск данных с именем "DataDisk1" из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="90656-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="90656-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="90656-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="90656-113">Эта команда удаляет диск с данными LUN 0 из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="90656-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="90656-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90656-114">PARAMETERS</span></span>

### <span data-ttu-id="90656-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90656-115">-DefaultProfile</span></span>
<span data-ttu-id="90656-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90656-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90656-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="90656-117">-Lun</span></span>
<span data-ttu-id="90656-118">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="90656-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="90656-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90656-119">-Name</span></span>
<span data-ttu-id="90656-120">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="90656-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="90656-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="90656-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="90656-122">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="90656-122">Specify the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90656-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90656-123">-Confirm</span></span>
<span data-ttu-id="90656-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90656-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90656-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90656-125">-WhatIf</span></span>
<span data-ttu-id="90656-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90656-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90656-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90656-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90656-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90656-128">CommonParameters</span></span>
<span data-ttu-id="90656-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90656-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90656-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90656-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90656-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90656-131">INPUTS</span></span>

### <span data-ttu-id="90656-132">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="90656-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="90656-133">System. String System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="90656-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="90656-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90656-134">OUTPUTS</span></span>

### <span data-ttu-id="90656-135">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="90656-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="90656-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="90656-136">NOTES</span></span>

## <span data-ttu-id="90656-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90656-137">RELATED LINKS</span></span>

