---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911401"
---
# <span data-ttu-id="0a5b3-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="0a5b3-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="0a5b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a5b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5b3-103">Удаляет диск с данными из VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="0a5b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a5b3-104">SYNTAX</span></span>

### <span data-ttu-id="0a5b3-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a5b3-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a5b3-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a5b3-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a5b3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5b3-107">DESCRIPTION</span></span>
<span data-ttu-id="0a5b3-108">Командлет **Remove-AzVmssDataDisk** удаляет диск с данными из экземпляра установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0a5b3-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0a5b3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a5b3-109">EXAMPLES</span></span>

### <span data-ttu-id="0a5b3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a5b3-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="0a5b3-111">Эта команда удаляет диск данных с именем "DataDisk1" из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="0a5b3-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0a5b3-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="0a5b3-113">Эта команда удаляет диск с данными LUN 0 из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="0a5b3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a5b3-114">PARAMETERS</span></span>

### <span data-ttu-id="0a5b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5b3-115">-DefaultProfile</span></span>
<span data-ttu-id="0a5b3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a5b3-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="0a5b3-117">-Lun</span></span>
<span data-ttu-id="0a5b3-118">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="0a5b3-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a5b3-119">-Name</span></span>
<span data-ttu-id="0a5b3-120">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="0a5b3-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0a5b3-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0a5b3-122">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="0a5b3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a5b3-123">-Confirm</span></span>
<span data-ttu-id="0a5b3-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5b3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a5b3-125">-WhatIf</span></span>
<span data-ttu-id="0a5b3-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a5b3-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5b3-128">CommonParameters</span></span>
<span data-ttu-id="0a5b3-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a5b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5b3-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a5b3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5b3-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a5b3-131">INPUTS</span></span>

### <span data-ttu-id="0a5b3-132">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0a5b3-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="0a5b3-133">System. String System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0a5b3-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0a5b3-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5b3-134">OUTPUTS</span></span>

### <span data-ttu-id="0a5b3-135">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0a5b3-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="0a5b3-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a5b3-136">NOTES</span></span>

## <span data-ttu-id="0a5b3-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a5b3-137">RELATED LINKS</span></span>

