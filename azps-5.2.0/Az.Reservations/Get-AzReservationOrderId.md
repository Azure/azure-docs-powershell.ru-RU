---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416535"
---
# <span data-ttu-id="e5693-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e5693-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="e5693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5693-102">SYNOPSIS</span></span>
<span data-ttu-id="e5693-103">Получите список соответствующих `ReservationOrder` ИД.</span><span class="sxs-lookup"><span data-stu-id="e5693-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="e5693-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5693-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5693-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5693-105">DESCRIPTION</span></span>
<span data-ttu-id="e5693-106">Получите ids applicable `ReservationOrder` s, которые можно применить к этой подписке.</span><span class="sxs-lookup"><span data-stu-id="e5693-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="e5693-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5693-107">EXAMPLES</span></span>

### <span data-ttu-id="e5693-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5693-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="e5693-109">Применить для подписки `ReservationOrder` по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e5693-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="e5693-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5693-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="e5693-111">Применить для `ReservationOrder` указанной подписки</span><span class="sxs-lookup"><span data-stu-id="e5693-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="e5693-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5693-112">PARAMETERS</span></span>

### <span data-ttu-id="e5693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5693-113">-DefaultProfile</span></span>
<span data-ttu-id="e5693-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5693-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5693-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5693-115">-SubscriptionId</span></span>
<span data-ttu-id="e5693-116">Id of the subscription to get the applied `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="e5693-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5693-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5693-117">CommonParameters</span></span>
<span data-ttu-id="e5693-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5693-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5693-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5693-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5693-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5693-120">INPUTS</span></span>

### <span data-ttu-id="e5693-121">Нет</span><span class="sxs-lookup"><span data-stu-id="e5693-121">None</span></span>

## <span data-ttu-id="e5693-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5693-122">OUTPUTS</span></span>

### <span data-ttu-id="e5693-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="e5693-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="e5693-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5693-124">NOTES</span></span>

## <span data-ttu-id="e5693-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5693-125">RELATED LINKS</span></span>
