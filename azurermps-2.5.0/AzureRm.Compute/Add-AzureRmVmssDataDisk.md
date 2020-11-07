---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: c91b9dc68bcc0cdecda9ced83a9b3c64452d6413
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913697"
---
# <span data-ttu-id="0a7c4-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="0a7c4-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="0a7c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7c4-103">Добавляет диск с данными в VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a7c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a7c4-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a7c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a7c4-105">DESCRIPTION</span></span>
<span data-ttu-id="0a7c4-106">Командлет **Add-AzureRmVmssDataDisk** добавляет диск с данными в экземпляр "Установка масштаба виртуальной машины (VMSS)".</span><span class="sxs-lookup"><span data-stu-id="0a7c4-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0a7c4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a7c4-107">EXAMPLES</span></span>

### <span data-ttu-id="0a7c4-108">Пример 1: Добавление диска с данными</span><span class="sxs-lookup"><span data-stu-id="0a7c4-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="0a7c4-109">Эта команда добавляет пустой диск данных в объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="0a7c4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a7c4-110">PARAMETERS</span></span>

### <span data-ttu-id="0a7c4-111">-Caching</span><span class="sxs-lookup"><span data-stu-id="0a7c4-111">-Caching</span></span>
<span data-ttu-id="0a7c4-112">Указывает тип кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="0a7c4-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="0a7c4-113">-CreateOption</span></span>
<span data-ttu-id="0a7c4-114">Задает параметр создания диска.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="0a7c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7c4-115">-DefaultProfile</span></span>
<span data-ttu-id="0a7c4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a7c4-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0a7c4-117">-DiskSizeGB</span></span>
<span data-ttu-id="0a7c4-118">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0a7c4-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="0a7c4-119">-Lun</span></span>
<span data-ttu-id="0a7c4-120">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="0a7c4-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a7c4-121">-Name</span></span>
<span data-ttu-id="0a7c4-122">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="0a7c4-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0a7c4-123">-StorageAccountType</span></span>
<span data-ttu-id="0a7c4-124">Указывает тип учетной записи хранения диска.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="0a7c4-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0a7c4-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0a7c4-126">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-126">Specify the VMSS object.</span></span>
<span data-ttu-id="0a7c4-127">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="0a7c4-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="0a7c4-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0a7c4-128">-WriteAccelerator</span></span>
<span data-ttu-id="0a7c4-129">Указывает, следует ли включить или отключить WriteAccelerator на диске с данными.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="0a7c4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a7c4-130">-Confirm</span></span>
<span data-ttu-id="0a7c4-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a7c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a7c4-132">-WhatIf</span></span>
<span data-ttu-id="0a7c4-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a7c4-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a7c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7c4-135">CommonParameters</span></span>
<span data-ttu-id="0a7c4-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a7c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7c4-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a7c4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7c4-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a7c4-138">INPUTS</span></span>

### <span data-ttu-id="0a7c4-139">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0a7c4-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="0a7c4-140">System. String System. Int32. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Model. DiskCreateOptionTypes, Microsoft. Azure.,. COMPUTE. Version = 14.0.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]] System. Nullable 1 [[Microsoft. Azure. Management. COMPUTE `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` . Version = 14.0.0.0, культура = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0a7c4-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="0a7c4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a7c4-141">OUTPUTS</span></span>

### <span data-ttu-id="0a7c4-142">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0a7c4-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="0a7c4-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a7c4-143">NOTES</span></span>

## <span data-ttu-id="0a7c4-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a7c4-144">RELATED LINKS</span></span>

