---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315743"
---
# <span data-ttu-id="37905-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="37905-101">Get-AzReservation</span></span>

## <span data-ttu-id="37905-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37905-102">SYNOPSIS</span></span>
<span data-ttu-id="37905-103">Получить `Reservation` s в заданном заказе на резервирование</span><span class="sxs-lookup"><span data-stu-id="37905-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="37905-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37905-104">SYNTAX</span></span>

### <span data-ttu-id="37905-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37905-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37905-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="37905-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37905-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="37905-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37905-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37905-108">DESCRIPTION</span></span>
<span data-ttu-id="37905-109">Список `Reservation` s в одном `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="37905-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="37905-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37905-110">EXAMPLES</span></span>

### <span data-ttu-id="37905-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37905-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="37905-112">Список `Reservation` s в указанном диапазоне `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="37905-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="37905-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="37905-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="37905-114">Получить определенные `Reservation` сведения.</span><span class="sxs-lookup"><span data-stu-id="37905-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="37905-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37905-115">PARAMETERS</span></span>

### <span data-ttu-id="37905-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37905-116">-DefaultProfile</span></span>
<span data-ttu-id="37905-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37905-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37905-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="37905-118">-ReservationId</span></span>
<span data-ttu-id="37905-119">Идентификатор `Reservation` поиска</span><span class="sxs-lookup"><span data-stu-id="37905-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37905-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="37905-120">-ReservationOrder</span></span>
<span data-ttu-id="37905-121">Параметр объекта pipe для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="37905-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37905-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="37905-122">-ReservationOrderId</span></span>
<span data-ttu-id="37905-123">Идентификатор элемента `ReservationOrder` , содержащего `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="37905-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="37905-124">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="37905-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37905-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="37905-125">-ReservationOrderPage</span></span>
<span data-ttu-id="37905-126">Параметр объекта pipe для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="37905-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37905-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37905-127">CommonParameters</span></span>
<span data-ttu-id="37905-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37905-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37905-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37905-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37905-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37905-130">INPUTS</span></span>

### <span data-ttu-id="37905-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="37905-131">System.Guid</span></span>

### <span data-ttu-id="37905-132">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="37905-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="37905-133">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="37905-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="37905-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37905-134">OUTPUTS</span></span>

### <span data-ttu-id="37905-135">Microsoft. Azure. Commands. резервирования. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="37905-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="37905-136">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="37905-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="37905-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="37905-137">NOTES</span></span>

## <span data-ttu-id="37905-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37905-138">RELATED LINKS</span></span>
