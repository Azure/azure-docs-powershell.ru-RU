---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: f99df428f99ec0e75eb4b1b220dde657be6f7458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557859"
---
# <span data-ttu-id="ab963-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ab963-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="ab963-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab963-102">SYNOPSIS</span></span>
<span data-ttu-id="ab963-103">Удаляет расширение из VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab963-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab963-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab963-104">SYNTAX</span></span>

### <span data-ttu-id="ab963-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab963-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab963-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab963-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab963-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab963-107">DESCRIPTION</span></span>
<span data-ttu-id="ab963-108">Командлет **Remove-AzureRmVmssExtension** удаляет расширение из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ab963-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ab963-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab963-109">EXAMPLES</span></span>

## <span data-ttu-id="ab963-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab963-110">PARAMETERS</span></span>

### <span data-ttu-id="ab963-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab963-111">-DefaultProfile</span></span>
<span data-ttu-id="ab963-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab963-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab963-113">-ID</span><span class="sxs-lookup"><span data-stu-id="ab963-113">-Id</span></span>
<span data-ttu-id="ab963-114">Указывает идентификатор расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab963-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab963-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ab963-115">-Name</span></span>
<span data-ttu-id="ab963-116">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab963-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="ab963-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ab963-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ab963-118">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="ab963-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="ab963-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab963-119">-Confirm</span></span>
<span data-ttu-id="ab963-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ab963-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab963-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab963-121">-WhatIf</span></span>
<span data-ttu-id="ab963-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ab963-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab963-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ab963-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab963-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab963-124">CommonParameters</span></span>
<span data-ttu-id="ab963-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab963-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab963-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab963-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab963-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab963-127">INPUTS</span></span>

## <span data-ttu-id="ab963-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab963-128">OUTPUTS</span></span>

### <span data-ttu-id="ab963-129">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab963-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ab963-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab963-130">NOTES</span></span>

## <span data-ttu-id="ab963-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab963-131">RELATED LINKS</span></span>

[<span data-ttu-id="ab963-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ab963-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
