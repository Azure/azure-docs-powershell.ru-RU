---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244690"
---
# <span data-ttu-id="695b9-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="695b9-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="695b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="695b9-102">SYNOPSIS</span></span>
<span data-ttu-id="695b9-103">Получение каталога доступных резервирований</span><span class="sxs-lookup"><span data-stu-id="695b9-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="695b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="695b9-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="695b9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="695b9-105">DESCRIPTION</span></span>
<span data-ttu-id="695b9-106">Получите регионы и SKU, доступные для зарезервированного экземпляра покупки для указанной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="695b9-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="695b9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="695b9-107">EXAMPLES</span></span>

### <span data-ttu-id="695b9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="695b9-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="695b9-109">Получение каталога VirtualMachines в westus для подписки по умолчанию</span><span class="sxs-lookup"><span data-stu-id="695b9-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="695b9-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="695b9-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="695b9-111">Получение каталога SuseLinux для указанной подписки</span><span class="sxs-lookup"><span data-stu-id="695b9-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="695b9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="695b9-112">PARAMETERS</span></span>

### <span data-ttu-id="695b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695b9-113">-DefaultProfile</span></span>
<span data-ttu-id="695b9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="695b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="695b9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="695b9-115">-Location</span></span>
<span data-ttu-id="695b9-116">Указывает расположение зарезервированных ресурсов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="695b9-116">Specifies the location of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695b9-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="695b9-117">-ReservedResourceType</span></span>
<span data-ttu-id="695b9-118">Указывает тип зарезервированных ресурсов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="695b9-118">Specifies the type of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695b9-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="695b9-119">-SubscriptionId</span></span>
<span data-ttu-id="695b9-120">Идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="695b9-120">Id of the subscription</span></span>

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

### <span data-ttu-id="695b9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695b9-121">CommonParameters</span></span>
<span data-ttu-id="695b9-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="695b9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695b9-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="695b9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695b9-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="695b9-124">INPUTS</span></span>

### <span data-ttu-id="695b9-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="695b9-125">None</span></span>

## <span data-ttu-id="695b9-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="695b9-126">OUTPUTS</span></span>

### <span data-ttu-id="695b9-127">Microsoft. Azure. Commands. резервирования. Models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="695b9-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="695b9-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="695b9-128">NOTES</span></span>

## <span data-ttu-id="695b9-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="695b9-129">RELATED LINKS</span></span>
