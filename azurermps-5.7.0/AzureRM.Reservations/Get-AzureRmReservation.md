---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557196"
---
# <span data-ttu-id="5d924-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="5d924-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="5d924-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d924-102">SYNOPSIS</span></span>
<span data-ttu-id="5d924-103">Получить `Reservation` s в заданном заказе на резервирование</span><span class="sxs-lookup"><span data-stu-id="5d924-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d924-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d924-104">SYNTAX</span></span>

### <span data-ttu-id="5d924-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d924-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="5d924-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="5d924-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="5d924-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d924-107">DESCRIPTION</span></span>
<span data-ttu-id="5d924-108">Список `Reservation` s в одном `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="5d924-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="5d924-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d924-109">EXAMPLES</span></span>

### <span data-ttu-id="5d924-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d924-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="5d924-111">Список `Reservation` s в указанном диапазоне `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="5d924-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="5d924-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5d924-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="5d924-113">Получить определенные `Reservation` сведения.</span><span class="sxs-lookup"><span data-stu-id="5d924-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="5d924-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d924-114">PARAMETERS</span></span>

### <span data-ttu-id="5d924-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="5d924-115">-ReservationId</span></span>
<span data-ttu-id="5d924-116">Идентификатор `Reservation` поиска</span><span class="sxs-lookup"><span data-stu-id="5d924-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d924-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="5d924-117">-ReservationOrder</span></span>
<span data-ttu-id="5d924-118">Параметр объекта pipe для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="5d924-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d924-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5d924-119">-ReservationOrderId</span></span>
<span data-ttu-id="5d924-120">Идентификатор элемента `ReservationOrder` , содержащего `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5d924-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="5d924-121">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="5d924-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d924-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="5d924-122">-ReservationOrderPage</span></span>
<span data-ttu-id="5d924-123">Параметр объекта pipe для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="5d924-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d924-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d924-124">CommonParameters</span></span>
<span data-ttu-id="5d924-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d924-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d924-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d924-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d924-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d924-127">INPUTS</span></span>

### <span data-ttu-id="5d924-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5d924-128">System.String</span></span>
<span data-ttu-id="5d924-129">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrder Microsoft. Azure. Commands. резервирования. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="5d924-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="5d924-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d924-130">OUTPUTS</span></span>

### <span data-ttu-id="5d924-131">Microsoft. Azure. Commands. резервирования. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="5d924-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="5d924-132">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5d924-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5d924-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d924-133">NOTES</span></span>

## <span data-ttu-id="5d924-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d924-134">RELATED LINKS</span></span>

