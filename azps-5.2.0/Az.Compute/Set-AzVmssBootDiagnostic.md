---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393919"
---
# <span data-ttu-id="fd6c1-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fd6c1-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="fd6c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6c1-103">Задает профиль диагностики загрузки в масштабе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="fd6c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd6c1-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd6c1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd6c1-105">DESCRIPTION</span></span>
<span data-ttu-id="fd6c1-106">Задает профиль диагностики загрузки в масштабе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="fd6c1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd6c1-107">EXAMPLES</span></span>

### <span data-ttu-id="fd6c1-108">Пример 1. Настройка свойства профиля диагностики загрузки для VMSS</span><span class="sxs-lookup"><span data-stu-id="fd6c1-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="fd6c1-109">Эта команда задает свойство профиля загрузки для VMSS ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="fd6c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd6c1-110">PARAMETERS</span></span>

### <span data-ttu-id="fd6c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6c1-111">-DefaultProfile</span></span>
<span data-ttu-id="fd6c1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd6c1-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="fd6c1-113">-Enabled</span></span>
<span data-ttu-id="fd6c1-114">Следует ли включить диагностику загрузки в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c1-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="fd6c1-115">-StorageUri</span></span>
<span data-ttu-id="fd6c1-116">URI учетной записи хранения, используемой для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c1-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd6c1-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fd6c1-118">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="fd6c1-119">Для создания объекта New-AzVmssConfig можно использовать New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="fd6c1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd6c1-120">-Confirm</span></span>
<span data-ttu-id="fd6c1-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd6c1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd6c1-122">-WhatIf</span></span>
<span data-ttu-id="fd6c1-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd6c1-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd6c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6c1-125">CommonParameters</span></span>
<span data-ttu-id="fd6c1-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6c1-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd6c1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6c1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd6c1-128">INPUTS</span></span>

### <span data-ttu-id="fd6c1-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd6c1-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fd6c1-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd6c1-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fd6c1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fd6c1-131">System.String</span></span>

## <span data-ttu-id="fd6c1-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd6c1-132">OUTPUTS</span></span>

### <span data-ttu-id="fd6c1-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd6c1-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fd6c1-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd6c1-134">NOTES</span></span>

## <span data-ttu-id="fd6c1-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd6c1-135">RELATED LINKS</span></span>
