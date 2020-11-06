---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566920"
---
# <span data-ttu-id="de51f-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="de51f-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="de51f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de51f-102">SYNOPSIS</span></span>
<span data-ttu-id="de51f-103">Получение `Reservation` журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="de51f-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de51f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de51f-104">SYNTAX</span></span>

### <span data-ttu-id="de51f-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de51f-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="de51f-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="de51f-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="de51f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de51f-107">DESCRIPTION</span></span>
<span data-ttu-id="de51f-108">Список всех исправлений для `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="de51f-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="de51f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de51f-109">EXAMPLES</span></span>

### <span data-ttu-id="de51f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de51f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="de51f-111">Получение истории исправлений для определенного резервирования</span><span class="sxs-lookup"><span data-stu-id="de51f-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="de51f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de51f-112">PARAMETERS</span></span>

### <span data-ttu-id="de51f-113">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="de51f-113">-Reservation</span></span>
<span data-ttu-id="de51f-114">Параметр объекта pipe для `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="de51f-114">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="de51f-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="de51f-115">-ReservationId</span></span>
<span data-ttu-id="de51f-116">ReservationId, в `Reservation` котором будет отображаться история</span><span class="sxs-lookup"><span data-stu-id="de51f-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="de51f-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="de51f-117">-ReservationOrderId</span></span>
<span data-ttu-id="de51f-118">ReservationOrderId `ReservationOrder` , где находится `Reservation`</span><span class="sxs-lookup"><span data-stu-id="de51f-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="de51f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de51f-119">CommonParameters</span></span>
<span data-ttu-id="de51f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de51f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de51f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de51f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de51f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de51f-122">INPUTS</span></span>

### <span data-ttu-id="de51f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="de51f-123">System.String</span></span>
<span data-ttu-id="de51f-124">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="de51f-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="de51f-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de51f-125">OUTPUTS</span></span>

### <span data-ttu-id="de51f-126">Microsoft. Azure. Commands. резервирования. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="de51f-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="de51f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="de51f-127">NOTES</span></span>

## <span data-ttu-id="de51f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de51f-128">RELATED LINKS</span></span>

