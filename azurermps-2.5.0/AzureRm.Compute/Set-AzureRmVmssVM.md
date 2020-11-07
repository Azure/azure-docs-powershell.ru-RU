---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915358"
---
# <span data-ttu-id="32284-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="32284-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="32284-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32284-102">SYNOPSIS</span></span>
<span data-ttu-id="32284-103">Изменяет состояние экземпляра VMSS.</span><span class="sxs-lookup"><span data-stu-id="32284-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32284-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32284-104">SYNTAX</span></span>

### <span data-ttu-id="32284-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32284-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32284-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="32284-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32284-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32284-107">DESCRIPTION</span></span>
<span data-ttu-id="32284-108">Командлет **Set-AzureRmVmssVM** изменяет состояние экземпляра набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="32284-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="32284-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32284-109">EXAMPLES</span></span>

## <span data-ttu-id="32284-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32284-110">PARAMETERS</span></span>

### <span data-ttu-id="32284-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32284-111">-AsJob</span></span>
<span data-ttu-id="32284-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="32284-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32284-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32284-113">-DefaultProfile</span></span>
<span data-ttu-id="32284-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32284-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32284-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="32284-115">-InstanceId</span></span>
<span data-ttu-id="32284-116">Указывает идентификатор экземпляра VMSS, для которого этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="32284-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="32284-117">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="32284-117">-Reimage</span></span>
<span data-ttu-id="32284-118">Указывает на то, что этот командлет переобразировать экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="32284-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32284-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="32284-119">-ReimageAll</span></span>
<span data-ttu-id="32284-120">Указывает, что командлет переобразует все диски в экземпляре VMSS.</span><span class="sxs-lookup"><span data-stu-id="32284-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32284-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32284-121">-ResourceGroupName</span></span>
<span data-ttu-id="32284-122">Указывает имя группы ресурсов, которая содержит экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="32284-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="32284-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="32284-123">-VMScaleSetName</span></span>
<span data-ttu-id="32284-124">Указывает имя экземпляра VMSS, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="32284-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="32284-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32284-125">-Confirm</span></span>
<span data-ttu-id="32284-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32284-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32284-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32284-127">-WhatIf</span></span>
<span data-ttu-id="32284-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32284-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32284-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32284-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32284-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32284-130">CommonParameters</span></span>
<span data-ttu-id="32284-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32284-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32284-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32284-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32284-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32284-133">INPUTS</span></span>

### <span data-ttu-id="32284-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="32284-134">None</span></span>
<span data-ttu-id="32284-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="32284-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32284-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32284-136">OUTPUTS</span></span>

### <span data-ttu-id="32284-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="32284-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="32284-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="32284-138">NOTES</span></span>

## <span data-ttu-id="32284-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32284-139">RELATED LINKS</span></span>

[<span data-ttu-id="32284-140">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="32284-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
