---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570195"
---
# <span data-ttu-id="cd572-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="cd572-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="cd572-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd572-102">SYNOPSIS</span></span>
<span data-ttu-id="cd572-103">Получение `Reservation` журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="cd572-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd572-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd572-104">SYNTAX</span></span>

### <span data-ttu-id="cd572-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd572-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd572-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="cd572-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd572-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd572-107">DESCRIPTION</span></span>
<span data-ttu-id="cd572-108">Список всех исправлений для `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="cd572-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="cd572-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd572-109">EXAMPLES</span></span>

### <span data-ttu-id="cd572-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd572-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="cd572-111">Получение истории исправлений для определенного резервирования</span><span class="sxs-lookup"><span data-stu-id="cd572-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="cd572-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd572-112">PARAMETERS</span></span>

### <span data-ttu-id="cd572-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd572-113">-DefaultProfile</span></span>
<span data-ttu-id="cd572-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd572-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd572-115">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="cd572-115">-Reservation</span></span>
<span data-ttu-id="cd572-116">Параметр объекта pipe для `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="cd572-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="cd572-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="cd572-117">-ReservationId</span></span>
<span data-ttu-id="cd572-118">ReservationId, в `Reservation` котором будет отображаться история</span><span class="sxs-lookup"><span data-stu-id="cd572-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="cd572-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="cd572-119">-ReservationOrderId</span></span>
<span data-ttu-id="cd572-120">ReservationOrderId `ReservationOrder` , где находится `Reservation`</span><span class="sxs-lookup"><span data-stu-id="cd572-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="cd572-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd572-121">CommonParameters</span></span>
<span data-ttu-id="cd572-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd572-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd572-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd572-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd572-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd572-124">INPUTS</span></span>

### <span data-ttu-id="cd572-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cd572-125">System.Guid</span></span>

### <span data-ttu-id="cd572-126">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="cd572-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="cd572-127">Параметры: резервирование (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd572-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="cd572-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd572-128">OUTPUTS</span></span>

### <span data-ttu-id="cd572-129">Microsoft. Azure. Commands. резервирования. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="cd572-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="cd572-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd572-130">NOTES</span></span>

## <span data-ttu-id="cd572-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd572-131">RELATED LINKS</span></span>
