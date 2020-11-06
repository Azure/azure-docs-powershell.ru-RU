---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565554"
---
# <span data-ttu-id="d90cd-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d90cd-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="d90cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d90cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d90cd-103">Задает определенные действия в указанном VMSS.</span><span class="sxs-lookup"><span data-stu-id="d90cd-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d90cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d90cd-104">SYNTAX</span></span>

### <span data-ttu-id="d90cd-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d90cd-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d90cd-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d90cd-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d90cd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d90cd-107">DESCRIPTION</span></span>
<span data-ttu-id="d90cd-108">Командлет **Set-AzureRmVmss** задает определенные действия в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d90cd-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d90cd-109">Единственным действием, поддерживаемым этим командлетом, является переобраз.</span><span class="sxs-lookup"><span data-stu-id="d90cd-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="d90cd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d90cd-110">EXAMPLES</span></span>

### <span data-ttu-id="d90cd-111">Пример 1: переизображение VMSS</span><span class="sxs-lookup"><span data-stu-id="d90cd-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d90cd-112">Эта команда позволяет переобразировать VMSS с именем ContosoVMSS, которое принадлежит группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="d90cd-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="d90cd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d90cd-113">PARAMETERS</span></span>

### <span data-ttu-id="d90cd-114">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="d90cd-114">-Reimage</span></span>
<span data-ttu-id="d90cd-115">Указывает на то, что командлет переобразует VMSS.</span><span class="sxs-lookup"><span data-stu-id="d90cd-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d90cd-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="d90cd-116">-ReimageAll</span></span>
<span data-ttu-id="d90cd-117">Указывает на то, что командлет переобразовать все диски в VMSS.</span><span class="sxs-lookup"><span data-stu-id="d90cd-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d90cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="d90cd-119">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="d90cd-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d90cd-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d90cd-120">-VMScaleSetName</span></span>
<span data-ttu-id="d90cd-121">Форель имя VMSS, для которого этот командлет задает действия.</span><span class="sxs-lookup"><span data-stu-id="d90cd-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d90cd-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d90cd-122">-Confirm</span></span>
<span data-ttu-id="d90cd-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d90cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90cd-124">-WhatIf</span></span>
<span data-ttu-id="d90cd-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d90cd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d90cd-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d90cd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90cd-127">CommonParameters</span></span>
<span data-ttu-id="d90cd-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d90cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90cd-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d90cd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90cd-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d90cd-130">INPUTS</span></span>

### <span data-ttu-id="d90cd-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="d90cd-131">None</span></span>
<span data-ttu-id="d90cd-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d90cd-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d90cd-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d90cd-133">OUTPUTS</span></span>

### <span data-ttu-id="d90cd-134">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d90cd-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d90cd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d90cd-135">NOTES</span></span>

## <span data-ttu-id="d90cd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d90cd-136">RELATED LINKS</span></span>

[<span data-ttu-id="d90cd-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d90cd-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="d90cd-138">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d90cd-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="d90cd-139">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d90cd-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="d90cd-140">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d90cd-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="d90cd-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d90cd-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="d90cd-142">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d90cd-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="d90cd-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d90cd-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


