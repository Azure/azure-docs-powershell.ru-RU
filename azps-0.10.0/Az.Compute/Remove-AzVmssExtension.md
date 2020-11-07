---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911390"
---
# <span data-ttu-id="4b18a-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4b18a-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="4b18a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b18a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b18a-103">Удаляет расширение из VMSS.</span><span class="sxs-lookup"><span data-stu-id="4b18a-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="4b18a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b18a-104">SYNTAX</span></span>

### <span data-ttu-id="4b18a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b18a-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b18a-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b18a-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b18a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b18a-107">DESCRIPTION</span></span>
<span data-ttu-id="4b18a-108">Командлет **Remove-AzVmssExtension** удаляет расширение из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4b18a-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4b18a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b18a-109">EXAMPLES</span></span>

### <span data-ttu-id="4b18a-110">Пример 1: удаление расширения из VMSS</span><span class="sxs-lookup"><span data-stu-id="4b18a-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="4b18a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b18a-111">PARAMETERS</span></span>

### <span data-ttu-id="4b18a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b18a-112">-DefaultProfile</span></span>
<span data-ttu-id="4b18a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b18a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b18a-114">-ID</span><span class="sxs-lookup"><span data-stu-id="4b18a-114">-Id</span></span>
<span data-ttu-id="4b18a-115">Указывает идентификатор расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="4b18a-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b18a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4b18a-116">-Name</span></span>
<span data-ttu-id="4b18a-117">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="4b18a-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b18a-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4b18a-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4b18a-119">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="4b18a-119">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="4b18a-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b18a-120">-Confirm</span></span>
<span data-ttu-id="4b18a-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b18a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b18a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b18a-122">-WhatIf</span></span>
<span data-ttu-id="4b18a-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b18a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b18a-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b18a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b18a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b18a-125">CommonParameters</span></span>
<span data-ttu-id="4b18a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b18a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b18a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b18a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b18a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b18a-128">INPUTS</span></span>

### <span data-ttu-id="4b18a-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4b18a-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="4b18a-130">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4b18a-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="4b18a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b18a-131">OUTPUTS</span></span>

### <span data-ttu-id="4b18a-132">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4b18a-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4b18a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b18a-133">NOTES</span></span>

## <span data-ttu-id="4b18a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b18a-134">RELATED LINKS</span></span>

[<span data-ttu-id="4b18a-135">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4b18a-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
