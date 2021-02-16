---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215620"
---
# <span data-ttu-id="2e712-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="2e712-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="2e712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e712-102">SYNOPSIS</span></span>
<span data-ttu-id="2e712-103">Удаляет диск данных из VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e712-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="2e712-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e712-104">SYNTAX</span></span>

### <span data-ttu-id="2e712-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e712-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e712-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e712-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e712-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e712-107">DESCRIPTION</span></span>
<span data-ttu-id="2e712-108">Для удаления диска данных из экземпляра набора виртуальных машин (VMSS) удаляется диск **данных.**</span><span class="sxs-lookup"><span data-stu-id="2e712-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="2e712-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e712-109">EXAMPLES</span></span>

### <span data-ttu-id="2e712-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e712-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="2e712-111">Эта команда удаляет диск данных с именем DataDisk1 из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e712-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="2e712-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2e712-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="2e712-113">Эта команда удаляет диск данных LUN 0 из объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e712-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="2e712-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e712-114">PARAMETERS</span></span>

### <span data-ttu-id="2e712-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e712-115">-DefaultProfile</span></span>
<span data-ttu-id="2e712-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e712-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e712-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="2e712-117">-Lun</span></span>
<span data-ttu-id="2e712-118">Определяет логическую единицу диска.</span><span class="sxs-lookup"><span data-stu-id="2e712-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="2e712-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2e712-119">-Name</span></span>
<span data-ttu-id="2e712-120">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="2e712-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="2e712-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e712-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2e712-122">Укажите объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e712-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="2e712-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e712-123">-Confirm</span></span>
<span data-ttu-id="2e712-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e712-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e712-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e712-125">-WhatIf</span></span>
<span data-ttu-id="2e712-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e712-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e712-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2e712-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e712-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e712-128">CommonParameters</span></span>
<span data-ttu-id="2e712-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e712-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e712-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e712-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e712-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e712-131">INPUTS</span></span>

### <span data-ttu-id="2e712-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e712-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2e712-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2e712-133">System.String</span></span>

### <span data-ttu-id="2e712-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2e712-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2e712-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e712-135">OUTPUTS</span></span>

### <span data-ttu-id="2e712-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e712-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2e712-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e712-137">NOTES</span></span>

## <span data-ttu-id="2e712-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e712-138">RELATED LINKS</span></span>
