---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565546"
---
# <span data-ttu-id="dfc28-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="dfc28-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="dfc28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfc28-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc28-103">Изменяет состояние экземпляра VMSS.</span><span class="sxs-lookup"><span data-stu-id="dfc28-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfc28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfc28-104">SYNTAX</span></span>

### <span data-ttu-id="dfc28-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfc28-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfc28-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="dfc28-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfc28-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfc28-107">DESCRIPTION</span></span>
<span data-ttu-id="dfc28-108">Командлет **Set-AzureRmVmssVM** изменяет состояние экземпляра набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="dfc28-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="dfc28-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfc28-109">EXAMPLES</span></span>

## <span data-ttu-id="dfc28-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfc28-110">PARAMETERS</span></span>

### <span data-ttu-id="dfc28-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="dfc28-111">-InstanceId</span></span>
<span data-ttu-id="dfc28-112">Указывает идентификатор экземпляра VMSS, для которого этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="dfc28-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc28-113">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="dfc28-113">-Reimage</span></span>
<span data-ttu-id="dfc28-114">Указывает на то, что этот командлет переобразировать экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="dfc28-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc28-115">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="dfc28-115">-ReimageAll</span></span>
<span data-ttu-id="dfc28-116">Указывает, что командлет переобразует все диски в экземпляре VMSS.</span><span class="sxs-lookup"><span data-stu-id="dfc28-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc28-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfc28-118">Указывает имя группы ресурсов, которая содержит экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="dfc28-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="dfc28-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="dfc28-119">-VMScaleSetName</span></span>
<span data-ttu-id="dfc28-120">Указывает имя экземпляра VMSS, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dfc28-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="dfc28-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfc28-121">-Confirm</span></span>
<span data-ttu-id="dfc28-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dfc28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfc28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc28-123">-WhatIf</span></span>
<span data-ttu-id="dfc28-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dfc28-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfc28-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dfc28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfc28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc28-126">CommonParameters</span></span>
<span data-ttu-id="dfc28-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfc28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc28-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfc28-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc28-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfc28-129">INPUTS</span></span>

### <span data-ttu-id="dfc28-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="dfc28-130">None</span></span>
<span data-ttu-id="dfc28-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="dfc28-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dfc28-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfc28-132">OUTPUTS</span></span>

## <span data-ttu-id="dfc28-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfc28-133">NOTES</span></span>

## <span data-ttu-id="dfc28-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfc28-134">RELATED LINKS</span></span>

[<span data-ttu-id="dfc28-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="dfc28-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
