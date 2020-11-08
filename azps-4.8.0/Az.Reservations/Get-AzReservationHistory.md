---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235464"
---
# <span data-ttu-id="c95dd-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="c95dd-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="c95dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c95dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c95dd-103">Получение `Reservation` журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="c95dd-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="c95dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c95dd-104">SYNTAX</span></span>

### <span data-ttu-id="c95dd-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c95dd-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c95dd-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="c95dd-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c95dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c95dd-107">DESCRIPTION</span></span>
<span data-ttu-id="c95dd-108">Список всех исправлений для `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c95dd-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="c95dd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c95dd-109">EXAMPLES</span></span>

### <span data-ttu-id="c95dd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c95dd-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="c95dd-111">Получение истории исправлений для определенного резервирования</span><span class="sxs-lookup"><span data-stu-id="c95dd-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="c95dd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c95dd-112">PARAMETERS</span></span>

### <span data-ttu-id="c95dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c95dd-113">-DefaultProfile</span></span>
<span data-ttu-id="c95dd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c95dd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c95dd-115">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="c95dd-115">-Reservation</span></span>
<span data-ttu-id="c95dd-116">Параметр объекта pipe для `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="c95dd-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="c95dd-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="c95dd-117">-ReservationId</span></span>
<span data-ttu-id="c95dd-118">ReservationId, в `Reservation` котором будет отображаться история</span><span class="sxs-lookup"><span data-stu-id="c95dd-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="c95dd-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c95dd-119">-ReservationOrderId</span></span>
<span data-ttu-id="c95dd-120">ReservationOrderId `ReservationOrder` , где находится `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c95dd-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="c95dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c95dd-121">CommonParameters</span></span>
<span data-ttu-id="c95dd-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c95dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c95dd-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c95dd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c95dd-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c95dd-124">INPUTS</span></span>

### <span data-ttu-id="c95dd-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c95dd-125">System.Guid</span></span>

### <span data-ttu-id="c95dd-126">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c95dd-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c95dd-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c95dd-127">OUTPUTS</span></span>

### <span data-ttu-id="c95dd-128">Microsoft. Azure. Commands. резервирования. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="c95dd-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="c95dd-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c95dd-129">NOTES</span></span>

## <span data-ttu-id="c95dd-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c95dd-130">RELATED LINKS</span></span>