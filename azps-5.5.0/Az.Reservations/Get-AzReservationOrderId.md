---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217801"
---
# <span data-ttu-id="4e232-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="4e232-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="4e232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e232-102">SYNOPSIS</span></span>
<span data-ttu-id="4e232-103">Получите список соответствующих `ReservationOrder` ИД.</span><span class="sxs-lookup"><span data-stu-id="4e232-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="4e232-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e232-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e232-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e232-105">DESCRIPTION</span></span>
<span data-ttu-id="4e232-106">Получите ids applicable `ReservationOrder` s, которые можно применить к этой подписке.</span><span class="sxs-lookup"><span data-stu-id="4e232-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="4e232-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e232-107">EXAMPLES</span></span>

### <span data-ttu-id="4e232-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e232-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="4e232-109">Применить для подписки `ReservationOrder` по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4e232-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="4e232-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4e232-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="4e232-111">Применить для `ReservationOrder` указанной подписки</span><span class="sxs-lookup"><span data-stu-id="4e232-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="4e232-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e232-112">PARAMETERS</span></span>

### <span data-ttu-id="4e232-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e232-113">-DefaultProfile</span></span>
<span data-ttu-id="4e232-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e232-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e232-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e232-115">-SubscriptionId</span></span>
<span data-ttu-id="4e232-116">Id of the subscription to get the applied `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="4e232-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="4e232-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e232-117">CommonParameters</span></span>
<span data-ttu-id="4e232-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e232-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e232-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e232-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e232-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e232-120">INPUTS</span></span>

### <span data-ttu-id="4e232-121">Нет</span><span class="sxs-lookup"><span data-stu-id="4e232-121">None</span></span>

## <span data-ttu-id="4e232-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e232-122">OUTPUTS</span></span>

### <span data-ttu-id="4e232-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="4e232-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="4e232-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e232-124">NOTES</span></span>

## <span data-ttu-id="4e232-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e232-125">RELATED LINKS</span></span>
