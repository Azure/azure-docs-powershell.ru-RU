---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325824"
---
# <span data-ttu-id="71246-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="71246-101">Split-AzReservation</span></span>

## <span data-ttu-id="71246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71246-102">SYNOPSIS</span></span>
<span data-ttu-id="71246-103">Разделение `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="71246-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="71246-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="71246-104">SYNTAX</span></span>

### <span data-ttu-id="71246-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71246-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71246-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="71246-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71246-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71246-107">DESCRIPTION</span></span>
<span data-ttu-id="71246-108">Разделить `Reservation` 1 на два `Reservation` с помощью указанного распределения количества.</span><span class="sxs-lookup"><span data-stu-id="71246-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="71246-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="71246-109">EXAMPLES</span></span>

### <span data-ttu-id="71246-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71246-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="71246-111">Разделение указанного количества `Reservation` на два с соответствующим `Reservation` количеством</span><span class="sxs-lookup"><span data-stu-id="71246-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="71246-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71246-112">PARAMETERS</span></span>

### <span data-ttu-id="71246-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71246-113">-DefaultProfile</span></span>
<span data-ttu-id="71246-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71246-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71246-115">-Quantity</span><span class="sxs-lookup"><span data-stu-id="71246-115">-Quantity</span></span>
<span data-ttu-id="71246-116">С разделителем — запятые для поля "Количество" двух `Reservation`</span><span class="sxs-lookup"><span data-stu-id="71246-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71246-117">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="71246-117">-Reservation</span></span>
<span data-ttu-id="71246-118">Параметр "Pipe object for" (Объект-труба) для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="71246-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71246-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="71246-119">-ReservationId</span></span>
<span data-ttu-id="71246-120">Id of the `Reservation` split</span><span class="sxs-lookup"><span data-stu-id="71246-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71246-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="71246-121">-ReservationOrderId</span></span>
<span data-ttu-id="71246-122">Id of the `ReservationOrder` that contains the user wants to `Reservation` split</span><span class="sxs-lookup"><span data-stu-id="71246-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71246-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71246-123">-Confirm</span></span>
<span data-ttu-id="71246-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71246-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71246-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71246-125">-WhatIf</span></span>
<span data-ttu-id="71246-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71246-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71246-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="71246-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71246-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71246-128">CommonParameters</span></span>
<span data-ttu-id="71246-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71246-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71246-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71246-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71246-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71246-131">INPUTS</span></span>

### <span data-ttu-id="71246-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="71246-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="71246-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71246-133">OUTPUTS</span></span>

### <span data-ttu-id="71246-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="71246-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="71246-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="71246-135">NOTES</span></span>

## <span data-ttu-id="71246-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71246-136">RELATED LINKS</span></span>
