---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: e2eca141678c5455df0e443c155693c3c1445e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732871"
---
# <span data-ttu-id="f7529-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="f7529-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="f7529-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7529-102">SYNOPSIS</span></span>
<span data-ttu-id="f7529-103">Добавляет диск с данными в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7529-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7529-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7529-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7529-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7529-105">DESCRIPTION</span></span>
<span data-ttu-id="f7529-106">Командлет **Add-AzureRmVmssDataDisk** добавляет диск с данными в экземпляр "Установка масштаба виртуальной машины (VMSS)".</span><span class="sxs-lookup"><span data-stu-id="f7529-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="f7529-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7529-107">EXAMPLES</span></span>

### <span data-ttu-id="f7529-108">Пример 1: Добавление диска с данными</span><span class="sxs-lookup"><span data-stu-id="f7529-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="f7529-109">Эта команда добавляет пустой диск данных в объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7529-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="f7529-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7529-110">PARAMETERS</span></span>

### <span data-ttu-id="f7529-111">-Caching</span><span class="sxs-lookup"><span data-stu-id="f7529-111">-Caching</span></span>
<span data-ttu-id="f7529-112">Указывает тип кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="f7529-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7529-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f7529-113">-CreateOption</span></span>
<span data-ttu-id="f7529-114">Задает параметр создания диска.</span><span class="sxs-lookup"><span data-stu-id="f7529-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7529-115">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f7529-115">-DiskSizeGB</span></span>
<span data-ttu-id="f7529-116">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="f7529-116">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7529-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="f7529-117">-Lun</span></span>
<span data-ttu-id="f7529-118">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="f7529-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7529-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7529-119">-Name</span></span>
<span data-ttu-id="f7529-120">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="f7529-120">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7529-121">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f7529-121">-StorageAccountType</span></span>
<span data-ttu-id="f7529-122">Указывает тип учетной записи хранения диска.</span><span class="sxs-lookup"><span data-stu-id="f7529-122">Specifies the storage account type of the disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7529-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7529-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f7529-124">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7529-124">Specify the VMSS object.</span></span>
<span data-ttu-id="f7529-125">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="f7529-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="f7529-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7529-126">-Confirm</span></span>
<span data-ttu-id="f7529-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7529-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7529-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7529-128">-WhatIf</span></span>
<span data-ttu-id="f7529-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7529-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7529-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7529-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7529-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7529-131">CommonParameters</span></span>
<span data-ttu-id="f7529-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7529-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7529-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7529-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7529-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7529-134">INPUTS</span></span>

### <span data-ttu-id="f7529-135">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7529-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="f7529-136">System. String System. Int32. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Model. DiskCreateOptionTypes, Microsoft. Azure.,. COMPUTE. Version = 14.0.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]] System. Nullable 1 [[Microsoft. Azure. Management. COMPUTE `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` . Version = 14.0.0.0, культура = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f7529-136">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f7529-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7529-137">OUTPUTS</span></span>

### <span data-ttu-id="f7529-138">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7529-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="f7529-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7529-139">NOTES</span></span>

## <span data-ttu-id="f7529-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7529-140">RELATED LINKS</span></span>
