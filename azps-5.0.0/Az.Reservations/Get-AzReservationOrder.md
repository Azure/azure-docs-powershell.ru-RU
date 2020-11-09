---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317708"
---
# <span data-ttu-id="a32b0-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="a32b0-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="a32b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a32b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a32b0-103">Получить `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="a32b0-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="a32b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a32b0-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a32b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a32b0-105">DESCRIPTION</span></span>
<span data-ttu-id="a32b0-106">Список всех `ReservationOrder` пользователей, к которым у пользователя есть доступ в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="a32b0-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="a32b0-107">Если задан параметр ReservationOrderId, получите этот конкретный ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="a32b0-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="a32b0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a32b0-108">EXAMPLES</span></span>

### <span data-ttu-id="a32b0-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a32b0-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="a32b0-110">Список всех `ReservationOrder` пользователей, имеющих доступ к текущему клиенту</span><span class="sxs-lookup"><span data-stu-id="a32b0-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="a32b0-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a32b0-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="a32b0-112">Получение `ReservationOrder` с помощью указанного ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a32b0-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="a32b0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a32b0-113">PARAMETERS</span></span>

### <span data-ttu-id="a32b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32b0-114">-DefaultProfile</span></span>
<span data-ttu-id="a32b0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a32b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a32b0-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a32b0-116">-ReservationOrderId</span></span>
<span data-ttu-id="a32b0-117">Идентификатор определенного ReservationOrder, который пользователь хочет просмотреть</span><span class="sxs-lookup"><span data-stu-id="a32b0-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="a32b0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32b0-118">CommonParameters</span></span>
<span data-ttu-id="a32b0-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a32b0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32b0-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a32b0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32b0-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a32b0-121">INPUTS</span></span>

### <span data-ttu-id="a32b0-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="a32b0-122">None</span></span>

## <span data-ttu-id="a32b0-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a32b0-123">OUTPUTS</span></span>

### <span data-ttu-id="a32b0-124">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="a32b0-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="a32b0-125">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="a32b0-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="a32b0-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a32b0-126">NOTES</span></span>

## <span data-ttu-id="a32b0-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a32b0-127">RELATED LINKS</span></span>
