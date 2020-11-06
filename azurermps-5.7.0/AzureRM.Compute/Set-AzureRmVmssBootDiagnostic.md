---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565552"
---
# <span data-ttu-id="c0aa8-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c0aa8-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="c0aa8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="c0aa8-103">Настройка профиля диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0aa8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0aa8-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0aa8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="c0aa8-106">Настройка профиля диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="c0aa8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0aa8-107">EXAMPLES</span></span>

### <span data-ttu-id="c0aa8-108">Пример 1: Настройка свойства профиля диагностики загрузки для VMSS</span><span class="sxs-lookup"><span data-stu-id="c0aa8-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="c0aa8-109">Эта команда задает свойство профиля диагностики загрузки для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c0aa8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0aa8-110">PARAMETERS</span></span>

### <span data-ttu-id="c0aa8-111">-Включено</span><span class="sxs-lookup"><span data-stu-id="c0aa8-111">-Enabled</span></span>
<span data-ttu-id="c0aa8-112">Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-112">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa8-113">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="c0aa8-113">-StorageUri</span></span>
<span data-ttu-id="c0aa8-114">Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-114">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa8-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c0aa8-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c0aa8-116">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-116">Specifies the VMSS object.</span></span>
<span data-ttu-id="c0aa8-117">Для создания объекта можно использовать командлет New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-117">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="c0aa8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0aa8-118">-Confirm</span></span>
<span data-ttu-id="c0aa8-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0aa8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0aa8-120">-WhatIf</span></span>
<span data-ttu-id="c0aa8-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0aa8-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0aa8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0aa8-123">CommonParameters</span></span>
<span data-ttu-id="c0aa8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0aa8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0aa8-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0aa8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0aa8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0aa8-126">INPUTS</span></span>

### <span data-ttu-id="c0aa8-127">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c0aa8-127">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="c0aa8-128">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="c0aa8-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="c0aa8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0aa8-129">OUTPUTS</span></span>

### <span data-ttu-id="c0aa8-130">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c0aa8-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="c0aa8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0aa8-131">NOTES</span></span>

## <span data-ttu-id="c0aa8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0aa8-132">RELATED LINKS</span></span>

