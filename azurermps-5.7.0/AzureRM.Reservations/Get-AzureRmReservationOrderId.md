---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563343"
---
# <span data-ttu-id="58353-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="58353-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="58353-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58353-102">SYNOPSIS</span></span>
<span data-ttu-id="58353-103">Получить список приемлемых `ReservationOrder` идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="58353-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58353-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58353-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="58353-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58353-105">DESCRIPTION</span></span>
<span data-ttu-id="58353-106">Получите идентификаторы `ReservationOrder` , которые можно применить к этой подписке.</span><span class="sxs-lookup"><span data-stu-id="58353-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="58353-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58353-107">EXAMPLES</span></span>

### <span data-ttu-id="58353-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58353-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="58353-109">Применить к `ReservationOrder` подписке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="58353-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="58353-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="58353-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="58353-111">Применить к `ReservationOrder` указанной подписке</span><span class="sxs-lookup"><span data-stu-id="58353-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="58353-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58353-112">PARAMETERS</span></span>

### <span data-ttu-id="58353-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58353-113">-SubscriptionId</span></span>
<span data-ttu-id="58353-114">Идентификатор подписки для получения примененного `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="58353-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58353-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58353-115">CommonParameters</span></span>
<span data-ttu-id="58353-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58353-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58353-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58353-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58353-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58353-118">INPUTS</span></span>

### <span data-ttu-id="58353-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="58353-119">None</span></span>

## <span data-ttu-id="58353-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58353-120">OUTPUTS</span></span>

### <span data-ttu-id="58353-121">Microsoft. Azure. Commands. резервирования. Models. PSAppliedReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="58353-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="58353-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="58353-122">NOTES</span></span>

## <span data-ttu-id="58353-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58353-123">RELATED LINKS</span></span>

