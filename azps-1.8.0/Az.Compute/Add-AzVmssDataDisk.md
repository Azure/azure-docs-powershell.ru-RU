---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: df4a3676d86027c4b2e8627e8eae87dcb84644c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731377"
---
# <span data-ttu-id="34ad6-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="34ad6-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="34ad6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="34ad6-103">Добавляет диск с данными в VMSS.</span><span class="sxs-lookup"><span data-stu-id="34ad6-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="34ad6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34ad6-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34ad6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="34ad6-106">Командлет **Add-AzVmssDataDisk** добавляет диск с данными в экземпляр "Установка масштаба виртуальной машины (VMSS)".</span><span class="sxs-lookup"><span data-stu-id="34ad6-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="34ad6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34ad6-107">EXAMPLES</span></span>

### <span data-ttu-id="34ad6-108">Пример 1: Добавление диска с данными</span><span class="sxs-lookup"><span data-stu-id="34ad6-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="34ad6-109">Эта команда добавляет пустой диск данных в объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="34ad6-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="34ad6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34ad6-110">PARAMETERS</span></span>

### <span data-ttu-id="34ad6-111">-Caching</span><span class="sxs-lookup"><span data-stu-id="34ad6-111">-Caching</span></span>
<span data-ttu-id="34ad6-112">Указывает тип кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="34ad6-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad6-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="34ad6-113">-CreateOption</span></span>
<span data-ttu-id="34ad6-114">Задает параметр создания диска.</span><span class="sxs-lookup"><span data-stu-id="34ad6-114">Specifies the create option of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ad6-115">-DefaultProfile</span></span>
<span data-ttu-id="34ad6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34ad6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34ad6-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="34ad6-117">-DiskSizeGB</span></span>
<span data-ttu-id="34ad6-118">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="34ad6-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad6-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="34ad6-119">-Lun</span></span>
<span data-ttu-id="34ad6-120">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="34ad6-120">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad6-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34ad6-121">-Name</span></span>
<span data-ttu-id="34ad6-122">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="34ad6-122">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad6-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="34ad6-123">-StorageAccountType</span></span>
<span data-ttu-id="34ad6-124">Указывает тип учетной записи хранения диска.</span><span class="sxs-lookup"><span data-stu-id="34ad6-124">Specifies the storage account type of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad6-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34ad6-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="34ad6-126">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="34ad6-126">Specify the VMSS object.</span></span>
<span data-ttu-id="34ad6-127">Для создания объекта можно использовать командлет [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="34ad6-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad6-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="34ad6-128">-WriteAccelerator</span></span>
<span data-ttu-id="34ad6-129">Указывает, следует ли включить или отключить WriteAccelerator на диске с данными.</span><span class="sxs-lookup"><span data-stu-id="34ad6-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="34ad6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34ad6-130">-Confirm</span></span>
<span data-ttu-id="34ad6-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34ad6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ad6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ad6-132">-WhatIf</span></span>
<span data-ttu-id="34ad6-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34ad6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34ad6-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34ad6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ad6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ad6-135">CommonParameters</span></span>
<span data-ttu-id="34ad6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34ad6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ad6-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ad6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ad6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34ad6-138">INPUTS</span></span>

### <span data-ttu-id="34ad6-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34ad6-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="34ad6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="34ad6-140">System.String</span></span>

### <span data-ttu-id="34ad6-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="34ad6-141">System.Int32</span></span>

### <span data-ttu-id="34ad6-142">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="34ad6-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="34ad6-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34ad6-143">OUTPUTS</span></span>

### <span data-ttu-id="34ad6-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34ad6-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="34ad6-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="34ad6-145">NOTES</span></span>

## <span data-ttu-id="34ad6-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34ad6-146">RELATED LINKS</span></span>
