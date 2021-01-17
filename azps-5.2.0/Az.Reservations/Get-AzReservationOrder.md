---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416559"
---
# <span data-ttu-id="1a1e7-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="1a1e7-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="1a1e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a1e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1e7-103">Получить `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="1a1e7-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="1a1e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a1e7-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a1e7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a1e7-105">DESCRIPTION</span></span>
<span data-ttu-id="1a1e7-106">Список всех клиентов, к которые `ReservationOrder` у пользователя есть доступ в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="1a1e7-107">Если параметр ReservationOrderId задан, получите определенный резервирование.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="1a1e7-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a1e7-108">EXAMPLES</span></span>

### <span data-ttu-id="1a1e7-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a1e7-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="1a1e7-110">`ReservationOrder`Укаймь все, к чем у пользователя есть доступ в текущем клиенте</span><span class="sxs-lookup"><span data-stu-id="1a1e7-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="1a1e7-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1a1e7-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="1a1e7-112">Получить `ReservationOrder` с указанным ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="1a1e7-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="1a1e7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a1e7-113">PARAMETERS</span></span>

### <span data-ttu-id="1a1e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1e7-114">-DefaultProfile</span></span>
<span data-ttu-id="1a1e7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a1e7-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="1a1e7-116">-ReservationOrderId</span></span>
<span data-ttu-id="1a1e7-117">Id of the specific ReservationOrder that user wants to see</span><span class="sxs-lookup"><span data-stu-id="1a1e7-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="1a1e7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1e7-118">CommonParameters</span></span>
<span data-ttu-id="1a1e7-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1e7-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a1e7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1e7-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a1e7-121">INPUTS</span></span>

### <span data-ttu-id="1a1e7-122">Нет</span><span class="sxs-lookup"><span data-stu-id="1a1e7-122">None</span></span>

## <span data-ttu-id="1a1e7-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a1e7-123">OUTPUTS</span></span>

### <span data-ttu-id="1a1e7-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="1a1e7-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="1a1e7-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="1a1e7-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="1a1e7-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a1e7-126">NOTES</span></span>

## <span data-ttu-id="1a1e7-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a1e7-127">RELATED LINKS</span></span>
