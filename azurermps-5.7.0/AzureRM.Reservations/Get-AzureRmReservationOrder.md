---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563348"
---
# <span data-ttu-id="a9d9f-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="a9d9f-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="a9d9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d9f-103">Получить `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="a9d9f-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9d9f-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## <span data-ttu-id="a9d9f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9d9f-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d9f-106">Список всех `ReservationOrder` пользователей, к которым у пользователя есть доступ в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="a9d9f-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="a9d9f-107">Если задан параметр ReservationOrderId, получите этот конкретный ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="a9d9f-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="a9d9f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9d9f-108">EXAMPLES</span></span>

### <span data-ttu-id="a9d9f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a9d9f-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="a9d9f-110">Список всех `ReservationOrder` пользователей, имеющих доступ к текущему клиенту</span><span class="sxs-lookup"><span data-stu-id="a9d9f-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="a9d9f-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a9d9f-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="a9d9f-112">Получение `ReservationOrder` с помощью указанного ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a9d9f-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="a9d9f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9d9f-113">PARAMETERS</span></span>

### <span data-ttu-id="a9d9f-114">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a9d9f-114">-ReservationOrderId</span></span>
<span data-ttu-id="a9d9f-115">Идентификатор определенного ReservationOrder, который пользователь хочет просмотреть</span><span class="sxs-lookup"><span data-stu-id="a9d9f-115">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="a9d9f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d9f-116">CommonParameters</span></span>
<span data-ttu-id="a9d9f-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9d9f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d9f-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d9f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d9f-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9d9f-119">INPUTS</span></span>

### <span data-ttu-id="a9d9f-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="a9d9f-120">None</span></span>

## <span data-ttu-id="a9d9f-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9d9f-121">OUTPUTS</span></span>

### <span data-ttu-id="a9d9f-122">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="a9d9f-122">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="a9d9f-123">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="a9d9f-123">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="a9d9f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9d9f-124">NOTES</span></span>

## <span data-ttu-id="a9d9f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9d9f-125">RELATED LINKS</span></span>

