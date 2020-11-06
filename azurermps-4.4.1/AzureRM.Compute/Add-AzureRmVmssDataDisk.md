---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 5e04013ee8f9452ee28cf7975066f512e2eae1c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557936"
---
# <span data-ttu-id="c1567-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="c1567-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="c1567-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1567-102">SYNOPSIS</span></span>
<span data-ttu-id="c1567-103">Добавляет диск с данными в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c1567-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1567-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1567-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1567-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1567-105">DESCRIPTION</span></span>
<span data-ttu-id="c1567-106">Командлет **Add-AzureRmVmssDataDisk** добавляет диск с данными в экземпляр "Установка масштаба виртуальной машины (VMSS)".</span><span class="sxs-lookup"><span data-stu-id="c1567-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c1567-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1567-107">EXAMPLES</span></span>

### <span data-ttu-id="c1567-108">Пример 1: Добавление диска с данными</span><span class="sxs-lookup"><span data-stu-id="c1567-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="c1567-109">Эта команда добавляет пустой диск данных в объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="c1567-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="c1567-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1567-110">PARAMETERS</span></span>

### <span data-ttu-id="c1567-111">-Caching</span><span class="sxs-lookup"><span data-stu-id="c1567-111">-Caching</span></span>
<span data-ttu-id="c1567-112">Указывает тип кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="c1567-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="c1567-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="c1567-113">-CreateOption</span></span>
<span data-ttu-id="c1567-114">Задает параметр создания диска.</span><span class="sxs-lookup"><span data-stu-id="c1567-114">Specifies the create option of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1567-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1567-115">-DefaultProfile</span></span>
<span data-ttu-id="c1567-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1567-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1567-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c1567-117">-DiskSizeGB</span></span>
<span data-ttu-id="c1567-118">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="c1567-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1567-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="c1567-119">-Lun</span></span>
<span data-ttu-id="c1567-120">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="c1567-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="c1567-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1567-121">-Name</span></span>
<span data-ttu-id="c1567-122">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="c1567-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="c1567-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c1567-123">-StorageAccountType</span></span>
<span data-ttu-id="c1567-124">Указывает тип учетной записи хранения диска.</span><span class="sxs-lookup"><span data-stu-id="c1567-124">Specifies the storage account type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1567-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c1567-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c1567-126">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="c1567-126">Specify the VMSS object.</span></span>
<span data-ttu-id="c1567-127">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="c1567-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="c1567-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1567-128">-Confirm</span></span>
<span data-ttu-id="c1567-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1567-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1567-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1567-130">-WhatIf</span></span>
<span data-ttu-id="c1567-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1567-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1567-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1567-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1567-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1567-133">CommonParameters</span></span>
<span data-ttu-id="c1567-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1567-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1567-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1567-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1567-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1567-136">INPUTS</span></span>

### <span data-ttu-id="c1567-137">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c1567-137">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="c1567-138">System. String System. Int32. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Model. DiskCreateOptionTypes, Microsoft. Azure.,. COMPUTE. Version = 14.0.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]] System. Nullable 1 [[Microsoft. Azure. Management. COMPUTE `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` . Version = 14.0.0.0, культура = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c1567-138">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c1567-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1567-139">OUTPUTS</span></span>

### <span data-ttu-id="c1567-140">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c1567-140">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="c1567-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1567-141">NOTES</span></span>

## <span data-ttu-id="c1567-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1567-142">RELATED LINKS</span></span>

