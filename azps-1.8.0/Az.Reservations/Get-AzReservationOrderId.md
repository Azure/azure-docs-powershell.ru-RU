---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: c969d24a894165e23628b91cda640f676ec3f3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729472"
---
# <span data-ttu-id="ee6ba-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="ee6ba-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="ee6ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ee6ba-103">Получить список приемлемых `ReservationOrder` идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="ee6ba-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="ee6ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee6ba-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee6ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee6ba-105">DESCRIPTION</span></span>
<span data-ttu-id="ee6ba-106">Получите идентификаторы `ReservationOrder` , которые можно применить к этой подписке.</span><span class="sxs-lookup"><span data-stu-id="ee6ba-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="ee6ba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee6ba-107">EXAMPLES</span></span>

### <span data-ttu-id="ee6ba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee6ba-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="ee6ba-109">Применить к `ReservationOrder` подписке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ee6ba-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="ee6ba-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee6ba-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="ee6ba-111">Применить к `ReservationOrder` указанной подписке</span><span class="sxs-lookup"><span data-stu-id="ee6ba-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="ee6ba-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee6ba-112">PARAMETERS</span></span>

### <span data-ttu-id="ee6ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee6ba-113">-DefaultProfile</span></span>
<span data-ttu-id="ee6ba-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee6ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee6ba-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee6ba-115">-SubscriptionId</span></span>
<span data-ttu-id="ee6ba-116">Идентификатор подписки для получения примененного `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="ee6ba-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="ee6ba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee6ba-117">CommonParameters</span></span>
<span data-ttu-id="ee6ba-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee6ba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee6ba-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee6ba-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee6ba-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee6ba-120">INPUTS</span></span>

### <span data-ttu-id="ee6ba-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="ee6ba-121">None</span></span>

## <span data-ttu-id="ee6ba-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee6ba-122">OUTPUTS</span></span>

### <span data-ttu-id="ee6ba-123">Microsoft. Azure. Management. резервирования. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="ee6ba-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="ee6ba-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee6ba-124">NOTES</span></span>

## <span data-ttu-id="ee6ba-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee6ba-125">RELATED LINKS</span></span>
