---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: a97ea07332b7ae5e7638ca0f1871d26286423f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731221"
---
# <span data-ttu-id="41cc4-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="41cc4-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="41cc4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="41cc4-103">Настройка профиля диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="41cc4-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="41cc4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41cc4-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41cc4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="41cc4-106">Настройка профиля диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="41cc4-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="41cc4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41cc4-107">EXAMPLES</span></span>

### <span data-ttu-id="41cc4-108">Пример 1: Настройка свойства профиля диагностики загрузки для VMSS</span><span class="sxs-lookup"><span data-stu-id="41cc4-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="41cc4-109">Эта команда задает свойство профиля диагностики загрузки для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="41cc4-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="41cc4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41cc4-110">PARAMETERS</span></span>

### <span data-ttu-id="41cc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cc4-111">-DefaultProfile</span></span>
<span data-ttu-id="41cc4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41cc4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41cc4-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="41cc4-113">-Enabled</span></span>
<span data-ttu-id="41cc4-114">Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="41cc4-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="41cc4-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="41cc4-115">-StorageUri</span></span>
<span data-ttu-id="41cc4-116">Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="41cc4-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="41cc4-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41cc4-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="41cc4-118">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="41cc4-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="41cc4-119">Для создания объекта можно использовать командлет New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="41cc4-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="41cc4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41cc4-120">-Confirm</span></span>
<span data-ttu-id="41cc4-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41cc4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41cc4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cc4-122">-WhatIf</span></span>
<span data-ttu-id="41cc4-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41cc4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41cc4-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41cc4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41cc4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cc4-125">CommonParameters</span></span>
<span data-ttu-id="41cc4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41cc4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cc4-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41cc4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cc4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41cc4-128">INPUTS</span></span>

### <span data-ttu-id="41cc4-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41cc4-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="41cc4-130">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="41cc4-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="41cc4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="41cc4-131">System.String</span></span>

## <span data-ttu-id="41cc4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41cc4-132">OUTPUTS</span></span>

### <span data-ttu-id="41cc4-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41cc4-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="41cc4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="41cc4-134">NOTES</span></span>

## <span data-ttu-id="41cc4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41cc4-135">RELATED LINKS</span></span>
