---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243101"
---
# <span data-ttu-id="baf9b-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="baf9b-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="baf9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="baf9b-102">SYNOPSIS</span></span>
<span data-ttu-id="baf9b-103">Удаляет диск с данными из VMSS.</span><span class="sxs-lookup"><span data-stu-id="baf9b-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="baf9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="baf9b-104">SYNTAX</span></span>

### <span data-ttu-id="baf9b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="baf9b-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baf9b-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="baf9b-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf9b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baf9b-107">DESCRIPTION</span></span>
<span data-ttu-id="baf9b-108">Командлет **Remove-AzVmssDataDisk** удаляет диск с данными из экземпляра установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="baf9b-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="baf9b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="baf9b-109">EXAMPLES</span></span>

### <span data-ttu-id="baf9b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="baf9b-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="baf9b-111">Эта команда удаляет диск данных с именем "DataDisk1" из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="baf9b-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="baf9b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="baf9b-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="baf9b-113">Эта команда удаляет диск с данными LUN 0 из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="baf9b-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="baf9b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="baf9b-114">PARAMETERS</span></span>

### <span data-ttu-id="baf9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf9b-115">-DefaultProfile</span></span>
<span data-ttu-id="baf9b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baf9b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baf9b-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="baf9b-117">-Lun</span></span>
<span data-ttu-id="baf9b-118">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="baf9b-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf9b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="baf9b-119">-Name</span></span>
<span data-ttu-id="baf9b-120">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="baf9b-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf9b-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="baf9b-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="baf9b-122">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="baf9b-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="baf9b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baf9b-123">-Confirm</span></span>
<span data-ttu-id="baf9b-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="baf9b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf9b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf9b-125">-WhatIf</span></span>
<span data-ttu-id="baf9b-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="baf9b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf9b-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="baf9b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf9b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf9b-128">CommonParameters</span></span>
<span data-ttu-id="baf9b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="baf9b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf9b-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baf9b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf9b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="baf9b-131">INPUTS</span></span>

### <span data-ttu-id="baf9b-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="baf9b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="baf9b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="baf9b-133">System.String</span></span>

### <span data-ttu-id="baf9b-134">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="baf9b-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="baf9b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="baf9b-135">OUTPUTS</span></span>

### <span data-ttu-id="baf9b-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="baf9b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="baf9b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="baf9b-137">NOTES</span></span>

## <span data-ttu-id="baf9b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baf9b-138">RELATED LINKS</span></span>
