---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 2b470a9837fafbb20d2e83f6fa9e7b4308b12d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729482"
---
# <span data-ttu-id="22eb1-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="22eb1-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="22eb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="22eb1-103">Получение каталога доступных резервирований</span><span class="sxs-lookup"><span data-stu-id="22eb1-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="22eb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22eb1-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22eb1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="22eb1-106">Получите регионы и SKU, доступные для зарезервированного экземпляра покупки для указанной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="22eb1-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="22eb1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="22eb1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22eb1-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="22eb1-109">Получение каталога VirtualMachines в westus для подписки по умолчанию</span><span class="sxs-lookup"><span data-stu-id="22eb1-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="22eb1-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="22eb1-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="22eb1-111">Получение каталога SuseLinux для указанной подписки</span><span class="sxs-lookup"><span data-stu-id="22eb1-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="22eb1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22eb1-112">PARAMETERS</span></span>

### <span data-ttu-id="22eb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22eb1-113">-DefaultProfile</span></span>
<span data-ttu-id="22eb1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22eb1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22eb1-115">-Location</span><span class="sxs-lookup"><span data-stu-id="22eb1-115">-Location</span></span>
<span data-ttu-id="22eb1-116">Указывает расположение зарезервированных ресурсов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="22eb1-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="22eb1-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="22eb1-117">-ReservedResourceType</span></span>
<span data-ttu-id="22eb1-118">Указывает тип зарезервированных ресурсов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="22eb1-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="22eb1-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22eb1-119">-SubscriptionId</span></span>
<span data-ttu-id="22eb1-120">Идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="22eb1-120">Id of the subscription</span></span>

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

### <span data-ttu-id="22eb1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22eb1-121">CommonParameters</span></span>
<span data-ttu-id="22eb1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22eb1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22eb1-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22eb1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22eb1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22eb1-124">INPUTS</span></span>

### <span data-ttu-id="22eb1-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="22eb1-125">None</span></span>

## <span data-ttu-id="22eb1-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22eb1-126">OUTPUTS</span></span>

### <span data-ttu-id="22eb1-127">Microsoft. Azure. Commands. резервирования. Models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="22eb1-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="22eb1-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="22eb1-128">NOTES</span></span>

## <span data-ttu-id="22eb1-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22eb1-129">RELATED LINKS</span></span>
