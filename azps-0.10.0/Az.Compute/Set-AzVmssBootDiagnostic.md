---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 482398d3ba0934f17b1381edc5dac08fb22bd75a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911317"
---
# <span data-ttu-id="65b2b-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="65b2b-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="65b2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="65b2b-103">Настройка профиля диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="65b2b-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="65b2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65b2b-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="65b2b-106">Настройка профиля диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="65b2b-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="65b2b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65b2b-107">EXAMPLES</span></span>

### <span data-ttu-id="65b2b-108">Пример 1: Настройка свойства профиля диагностики загрузки для VMSS</span><span class="sxs-lookup"><span data-stu-id="65b2b-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="65b2b-109">Эта команда задает свойство профиля диагностики загрузки для VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="65b2b-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="65b2b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65b2b-110">PARAMETERS</span></span>

### <span data-ttu-id="65b2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b2b-111">-DefaultProfile</span></span>
<span data-ttu-id="65b2b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65b2b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65b2b-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="65b2b-113">-Enabled</span></span>
<span data-ttu-id="65b2b-114">Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="65b2b-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="65b2b-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="65b2b-115">-StorageUri</span></span>
<span data-ttu-id="65b2b-116">Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="65b2b-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="65b2b-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65b2b-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="65b2b-118">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="65b2b-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="65b2b-119">Для создания объекта можно использовать командлет New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="65b2b-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="65b2b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65b2b-120">-Confirm</span></span>
<span data-ttu-id="65b2b-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65b2b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65b2b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b2b-122">-WhatIf</span></span>
<span data-ttu-id="65b2b-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65b2b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65b2b-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65b2b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65b2b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b2b-125">CommonParameters</span></span>
<span data-ttu-id="65b2b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65b2b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b2b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b2b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b2b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65b2b-128">INPUTS</span></span>

### <span data-ttu-id="65b2b-129">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65b2b-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="65b2b-130">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="65b2b-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="65b2b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65b2b-131">OUTPUTS</span></span>

### <span data-ttu-id="65b2b-132">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65b2b-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="65b2b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="65b2b-133">NOTES</span></span>

## <span data-ttu-id="65b2b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65b2b-134">RELATED LINKS</span></span>

