---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: 224b0302da76fd1c748cd77a183aa9a302dd3c9b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913391"
---
# <span data-ttu-id="8d939-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8d939-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="8d939-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d939-102">SYNOPSIS</span></span>
<span data-ttu-id="8d939-103">Удаляет расширение из VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d939-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d939-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d939-104">SYNTAX</span></span>

### <span data-ttu-id="8d939-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d939-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d939-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d939-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d939-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d939-107">DESCRIPTION</span></span>
<span data-ttu-id="8d939-108">Командлет **Remove-AzureRmVmssExtension** удаляет расширение из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8d939-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8d939-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d939-109">EXAMPLES</span></span>

## <span data-ttu-id="8d939-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d939-110">PARAMETERS</span></span>

### <span data-ttu-id="8d939-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d939-111">-DefaultProfile</span></span>
<span data-ttu-id="8d939-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d939-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d939-113">-ID</span><span class="sxs-lookup"><span data-stu-id="8d939-113">-Id</span></span>
<span data-ttu-id="8d939-114">Указывает идентификатор расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d939-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="8d939-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d939-115">-Name</span></span>
<span data-ttu-id="8d939-116">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d939-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="8d939-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d939-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d939-118">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="8d939-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="8d939-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d939-119">-Confirm</span></span>
<span data-ttu-id="8d939-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d939-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d939-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d939-121">-WhatIf</span></span>
<span data-ttu-id="8d939-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d939-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d939-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d939-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d939-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d939-124">CommonParameters</span></span>
<span data-ttu-id="8d939-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d939-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d939-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d939-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d939-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d939-127">INPUTS</span></span>

### <span data-ttu-id="8d939-128">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d939-128">VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d939-129">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8d939-129">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="8d939-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d939-130">OUTPUTS</span></span>

### <span data-ttu-id="8d939-131">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8d939-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8d939-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d939-132">NOTES</span></span>

## <span data-ttu-id="8d939-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d939-133">RELATED LINKS</span></span>

[<span data-ttu-id="8d939-134">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8d939-134">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
