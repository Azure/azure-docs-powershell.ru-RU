---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217804"
---
# <span data-ttu-id="af16f-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="af16f-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="af16f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af16f-102">SYNOPSIS</span></span>
<span data-ttu-id="af16f-103">Получить `Reservation` историю изменений.</span><span class="sxs-lookup"><span data-stu-id="af16f-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="af16f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af16f-104">SYNTAX</span></span>

### <span data-ttu-id="af16f-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af16f-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af16f-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="af16f-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af16f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af16f-107">DESCRIPTION</span></span>
<span data-ttu-id="af16f-108">Список всех изменений для `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="af16f-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="af16f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af16f-109">EXAMPLES</span></span>

### <span data-ttu-id="af16f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af16f-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="af16f-111">Получить историю изменений для определенного резервирования</span><span class="sxs-lookup"><span data-stu-id="af16f-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="af16f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af16f-112">PARAMETERS</span></span>

### <span data-ttu-id="af16f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af16f-113">-DefaultProfile</span></span>
<span data-ttu-id="af16f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af16f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af16f-115">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="af16f-115">-Reservation</span></span>
<span data-ttu-id="af16f-116">Параметр "Объект-труба" для `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="af16f-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="af16f-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="af16f-117">-ReservationId</span></span>
<span data-ttu-id="af16f-118">ReservationId `Reservation` of which history is to be shown</span><span class="sxs-lookup"><span data-stu-id="af16f-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="af16f-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="af16f-119">-ReservationOrderId</span></span>
<span data-ttu-id="af16f-120">ReservationOrderId для `ReservationOrder` того, что содержит `Reservation`</span><span class="sxs-lookup"><span data-stu-id="af16f-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="af16f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af16f-121">CommonParameters</span></span>
<span data-ttu-id="af16f-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af16f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af16f-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af16f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af16f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af16f-124">INPUTS</span></span>

### <span data-ttu-id="af16f-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="af16f-125">System.Guid</span></span>

### <span data-ttu-id="af16f-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="af16f-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="af16f-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af16f-127">OUTPUTS</span></span>

### <span data-ttu-id="af16f-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="af16f-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="af16f-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af16f-129">NOTES</span></span>

## <span data-ttu-id="af16f-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af16f-130">RELATED LINKS</span></span>
