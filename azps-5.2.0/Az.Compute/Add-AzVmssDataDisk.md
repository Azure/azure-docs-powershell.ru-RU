---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406623"
---
# <span data-ttu-id="b5e30-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="b5e30-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="b5e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5e30-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e30-103">Добавляет диск данных в VMSS.</span><span class="sxs-lookup"><span data-stu-id="b5e30-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="b5e30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5e30-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5e30-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5e30-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e30-106">**Cmdlet Add-AzVmssDataDisk** добавляет диск данных в экземпляр набора виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b5e30-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b5e30-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5e30-107">EXAMPLES</span></span>

### <span data-ttu-id="b5e30-108">Пример 1. Добавление диска данных</span><span class="sxs-lookup"><span data-stu-id="b5e30-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="b5e30-109">Эта команда добавляет пустой диск данных в объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="b5e30-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="b5e30-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5e30-110">PARAMETERS</span></span>

### <span data-ttu-id="b5e30-111">-Кэшинг</span><span class="sxs-lookup"><span data-stu-id="b5e30-111">-Caching</span></span>
<span data-ttu-id="b5e30-112">Определяет тип кэшинга диска.</span><span class="sxs-lookup"><span data-stu-id="b5e30-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="b5e30-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b5e30-113">-CreateOption</span></span>
<span data-ttu-id="b5e30-114">Определяет параметр создания диска.</span><span class="sxs-lookup"><span data-stu-id="b5e30-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="b5e30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e30-115">-DefaultProfile</span></span>
<span data-ttu-id="b5e30-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5e30-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b5e30-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b5e30-118">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="b5e30-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="b5e30-119">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="b5e30-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="b5e30-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5e30-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="b5e30-121">Определяет, Read-Write IOPS для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="b5e30-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="b5e30-122">Следует использовать только в том случае, если StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="b5e30-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="b5e30-123">Если не указано иное, значение по умолчанию будет назначено на основе размера дискового размера ГБ.</span><span class="sxs-lookup"><span data-stu-id="b5e30-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e30-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5e30-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="b5e30-125">Указывает пропускную способность (в МБ в секунду) для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="b5e30-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="b5e30-126">Следует использовать только в том случае, если StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="b5e30-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="b5e30-127">Если не указано иное, значение по умолчанию будет назначено на основе размера дискового размера ГБ.</span><span class="sxs-lookup"><span data-stu-id="b5e30-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e30-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b5e30-128">-DiskSizeGB</span></span>
<span data-ttu-id="b5e30-129">Определяет размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="b5e30-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b5e30-130">-Lun</span><span class="sxs-lookup"><span data-stu-id="b5e30-130">-Lun</span></span>
<span data-ttu-id="b5e30-131">Определяет логическую единицу диска.</span><span class="sxs-lookup"><span data-stu-id="b5e30-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="b5e30-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b5e30-132">-Name</span></span>
<span data-ttu-id="b5e30-133">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="b5e30-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="b5e30-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b5e30-134">-StorageAccountType</span></span>
<span data-ttu-id="b5e30-135">Определяет тип учетной записи хранения диска.</span><span class="sxs-lookup"><span data-stu-id="b5e30-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="b5e30-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b5e30-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b5e30-137">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="b5e30-137">Specify the VMSS object.</span></span>
<span data-ttu-id="b5e30-138">Для создания объекта можно использовать [cmdlet New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="b5e30-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="b5e30-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b5e30-139">-WriteAccelerator</span></span>
<span data-ttu-id="b5e30-140">Указывает, следует ли включить или отключить WriteAccelerator на диске данных.</span><span class="sxs-lookup"><span data-stu-id="b5e30-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="b5e30-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5e30-141">-Confirm</span></span>
<span data-ttu-id="b5e30-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5e30-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5e30-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e30-143">-WhatIf</span></span>
<span data-ttu-id="b5e30-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5e30-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e30-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b5e30-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5e30-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e30-146">CommonParameters</span></span>
<span data-ttu-id="b5e30-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e30-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e30-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5e30-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e30-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5e30-149">INPUTS</span></span>

### <span data-ttu-id="b5e30-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="b5e30-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b5e30-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b5e30-151">System.String</span></span>

### <span data-ttu-id="b5e30-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b5e30-152">System.Int32</span></span>

### <span data-ttu-id="b5e30-153">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b5e30-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b5e30-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5e30-154">OUTPUTS</span></span>

### <span data-ttu-id="b5e30-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="b5e30-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b5e30-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5e30-156">NOTES</span></span>

## <span data-ttu-id="b5e30-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5e30-157">RELATED LINKS</span></span>