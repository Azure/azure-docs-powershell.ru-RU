---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 1e0c04bd7283bc2a741b5e2a7130e83b35d00133
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567799"
---
# <span data-ttu-id="10e9a-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="10e9a-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="10e9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="10e9a-103">Удаляет диск с данными из VMSS.</span><span class="sxs-lookup"><span data-stu-id="10e9a-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10e9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10e9a-104">SYNTAX</span></span>

### <span data-ttu-id="10e9a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10e9a-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10e9a-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="10e9a-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e9a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10e9a-107">DESCRIPTION</span></span>
<span data-ttu-id="10e9a-108">Командлет **Remove-AzureRmVmssDataDisk** удаляет диск с данными из экземпляра установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="10e9a-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="10e9a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10e9a-109">EXAMPLES</span></span>

### <span data-ttu-id="10e9a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10e9a-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="10e9a-111">Эта команда удаляет диск данных с именем "DataDisk1" из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="10e9a-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="10e9a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="10e9a-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="10e9a-113">Эта команда удаляет диск с данными LUN 0 из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="10e9a-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="10e9a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10e9a-114">PARAMETERS</span></span>

### <span data-ttu-id="10e9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e9a-115">-DefaultProfile</span></span>
<span data-ttu-id="10e9a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10e9a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10e9a-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="10e9a-117">-Lun</span></span>
<span data-ttu-id="10e9a-118">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="10e9a-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="10e9a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10e9a-119">-Name</span></span>
<span data-ttu-id="10e9a-120">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="10e9a-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="10e9a-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="10e9a-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="10e9a-122">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="10e9a-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="10e9a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10e9a-123">-Confirm</span></span>
<span data-ttu-id="10e9a-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="10e9a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e9a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e9a-125">-WhatIf</span></span>
<span data-ttu-id="10e9a-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="10e9a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e9a-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="10e9a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e9a-128">CommonParameters</span></span>
<span data-ttu-id="10e9a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10e9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e9a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10e9a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e9a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10e9a-131">INPUTS</span></span>

### <span data-ttu-id="10e9a-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="10e9a-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="10e9a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="10e9a-133">System.String</span></span>

### <span data-ttu-id="10e9a-134">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="10e9a-134">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="10e9a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10e9a-135">OUTPUTS</span></span>

### <span data-ttu-id="10e9a-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="10e9a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="10e9a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="10e9a-137">NOTES</span></span>

## <span data-ttu-id="10e9a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10e9a-138">RELATED LINKS</span></span>
