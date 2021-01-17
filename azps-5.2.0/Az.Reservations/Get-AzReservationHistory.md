---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416572"
---
# <span data-ttu-id="1be8c-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="1be8c-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="1be8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be8c-102">SYNOPSIS</span></span>
<span data-ttu-id="1be8c-103">Получить `Reservation` историю версий.</span><span class="sxs-lookup"><span data-stu-id="1be8c-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="1be8c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1be8c-104">SYNTAX</span></span>

### <span data-ttu-id="1be8c-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1be8c-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1be8c-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="1be8c-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1be8c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1be8c-107">DESCRIPTION</span></span>
<span data-ttu-id="1be8c-108">Список всех изменений для `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="1be8c-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="1be8c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1be8c-109">EXAMPLES</span></span>

### <span data-ttu-id="1be8c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1be8c-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="1be8c-111">Получить историю изменений за определенное резервирование</span><span class="sxs-lookup"><span data-stu-id="1be8c-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="1be8c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1be8c-112">PARAMETERS</span></span>

### <span data-ttu-id="1be8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be8c-113">-DefaultProfile</span></span>
<span data-ttu-id="1be8c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1be8c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1be8c-115">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="1be8c-115">-Reservation</span></span>
<span data-ttu-id="1be8c-116">Параметр "Pipe object for `Reservation` s"</span><span class="sxs-lookup"><span data-stu-id="1be8c-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="1be8c-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="1be8c-117">-ReservationId</span></span>
<span data-ttu-id="1be8c-118">ReservationId `Reservation` of which history is to be shown</span><span class="sxs-lookup"><span data-stu-id="1be8c-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="1be8c-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="1be8c-119">-ReservationOrderId</span></span>
<span data-ttu-id="1be8c-120">ReservationOrderId для `ReservationOrder` того, который содержит `Reservation`</span><span class="sxs-lookup"><span data-stu-id="1be8c-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="1be8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be8c-121">CommonParameters</span></span>
<span data-ttu-id="1be8c-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be8c-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1be8c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be8c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1be8c-124">INPUTS</span></span>

### <span data-ttu-id="1be8c-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1be8c-125">System.Guid</span></span>

### <span data-ttu-id="1be8c-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="1be8c-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="1be8c-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1be8c-127">OUTPUTS</span></span>

### <span data-ttu-id="1be8c-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="1be8c-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="1be8c-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1be8c-129">NOTES</span></span>

## <span data-ttu-id="1be8c-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1be8c-130">RELATED LINKS</span></span>
