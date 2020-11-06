---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563347"
---
# <span data-ttu-id="489c4-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="489c4-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="489c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="489c4-102">SYNOPSIS</span></span>
<span data-ttu-id="489c4-103">Разделение а `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="489c4-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="489c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="489c4-104">SYNTAX</span></span>

### <span data-ttu-id="489c4-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="489c4-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="489c4-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="489c4-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="489c4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="489c4-107">DESCRIPTION</span></span>
<span data-ttu-id="489c4-108">Разделите элемент на `Reservation` две `Reservation` s с указанным распределением количества.</span><span class="sxs-lookup"><span data-stu-id="489c4-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="489c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="489c4-109">EXAMPLES</span></span>

### <span data-ttu-id="489c4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="489c4-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="489c4-111">Разделение заданной `Reservation` `Reservation` величины на две с помощью соответствующих количеств</span><span class="sxs-lookup"><span data-stu-id="489c4-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="489c4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="489c4-112">PARAMETERS</span></span>

### <span data-ttu-id="489c4-113">-Количество</span><span class="sxs-lookup"><span data-stu-id="489c4-113">-Quantity</span></span>
<span data-ttu-id="489c4-114">Целые числа, разделенные запятыми, в поле количества двух `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="489c4-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="489c4-115">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="489c4-115">-Reservation</span></span>
<span data-ttu-id="489c4-116">Параметр объекта pipe для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="489c4-116">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="489c4-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="489c4-117">-ReservationId</span></span>
<span data-ttu-id="489c4-118">Идентификатор `Reservation` для разделения</span><span class="sxs-lookup"><span data-stu-id="489c4-118">Id of the `Reservation` to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="489c4-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="489c4-119">-ReservationOrderId</span></span>
<span data-ttu-id="489c4-120">Идентификатор элемента, `ReservationOrder` содержащего сведения о том `Reservation` , что пользователь хочет разделить</span><span class="sxs-lookup"><span data-stu-id="489c4-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="489c4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="489c4-121">-Confirm</span></span>
<span data-ttu-id="489c4-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="489c4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="489c4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="489c4-123">-WhatIf</span></span>
<span data-ttu-id="489c4-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="489c4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="489c4-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="489c4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="489c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="489c4-126">CommonParameters</span></span>
<span data-ttu-id="489c4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="489c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="489c4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="489c4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="489c4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="489c4-129">INPUTS</span></span>

### <span data-ttu-id="489c4-130">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="489c4-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="489c4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="489c4-131">OUTPUTS</span></span>

### <span data-ttu-id="489c4-132">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. резервирования. Models. PSReservation, Microsoft. Azure. Commands. резервирования, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="489c4-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="489c4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="489c4-133">NOTES</span></span>

## <span data-ttu-id="489c4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="489c4-134">RELATED LINKS</span></span>

