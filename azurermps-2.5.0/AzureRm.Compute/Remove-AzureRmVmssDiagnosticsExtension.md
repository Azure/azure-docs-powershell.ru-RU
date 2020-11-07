---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 74bb0bee84615618f464cfbfd86dcb2b7dde387b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914513"
---
# <span data-ttu-id="7b8b8-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7b8b8-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="7b8b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8b8-103">Удаляет расширение диагностики из VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b8b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b8b8-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b8b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b8b8-105">DESCRIPTION</span></span>
<span data-ttu-id="7b8b8-106">Командлет **Remove-AzureRmVmssDiagnosticsExtension** удаляет расширение диагностики из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7b8b8-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7b8b8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b8b8-107">EXAMPLES</span></span>

### <span data-ttu-id="7b8b8-108">Пример 1: удаление расширения диагностики из VMSS</span><span class="sxs-lookup"><span data-stu-id="7b8b8-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="7b8b8-109">Эта команда удаляет расширение диагностики из VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="7b8b8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b8b8-110">PARAMETERS</span></span>

### <span data-ttu-id="7b8b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8b8-111">-DefaultProfile</span></span>
<span data-ttu-id="7b8b8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b8b8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b8b8-113">-Name</span></span>
<span data-ttu-id="7b8b8-114">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8b8-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7b8b8-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7b8b8-116">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="7b8b8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b8b8-117">-Confirm</span></span>
<span data-ttu-id="7b8b8-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8b8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b8b8-119">-WhatIf</span></span>
<span data-ttu-id="7b8b8-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7b8b8-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8b8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8b8-122">CommonParameters</span></span>
<span data-ttu-id="7b8b8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8b8-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b8b8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8b8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b8b8-125">INPUTS</span></span>

### <span data-ttu-id="7b8b8-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7b8b8-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="7b8b8-127">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="7b8b8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b8b8-128">OUTPUTS</span></span>

###  
<span data-ttu-id="7b8b8-129">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7b8b8-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b8b8-130">NOTES</span></span>

## <span data-ttu-id="7b8b8-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b8b8-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b8b8-132">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7b8b8-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="7b8b8-133">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7b8b8-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="7b8b8-134">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7b8b8-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


