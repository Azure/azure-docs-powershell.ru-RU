---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 155310764ea540d9062df8ae8f37171bc6f73066
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560735"
---
# <span data-ttu-id="29e87-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="29e87-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="29e87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29e87-102">SYNOPSIS</span></span>
<span data-ttu-id="29e87-103">Получение каталога доступных резервирований</span><span class="sxs-lookup"><span data-stu-id="29e87-103">Get the catalog of available reservations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29e87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29e87-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29e87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29e87-105">DESCRIPTION</span></span>
<span data-ttu-id="29e87-106">Получите регионы и SKU, доступные для зарезервированного экземпляра покупки для указанной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="29e87-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="29e87-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29e87-107">EXAMPLES</span></span>

### <span data-ttu-id="29e87-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29e87-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="29e87-109">Получение каталога VirtualMachines в westus для подписки по умолчанию</span><span class="sxs-lookup"><span data-stu-id="29e87-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="29e87-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="29e87-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="29e87-111">Получение каталога SuseLinux для указанной подписки</span><span class="sxs-lookup"><span data-stu-id="29e87-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="29e87-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29e87-112">PARAMETERS</span></span>

### <span data-ttu-id="29e87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e87-113">-DefaultProfile</span></span>
<span data-ttu-id="29e87-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29e87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29e87-115">-Location</span><span class="sxs-lookup"><span data-stu-id="29e87-115">-Location</span></span>
<span data-ttu-id="29e87-116">Указывает расположение зарезервированных ресурсов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="29e87-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="29e87-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="29e87-117">-ReservedResourceType</span></span>
<span data-ttu-id="29e87-118">Указывает тип зарезервированных ресурсов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="29e87-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="29e87-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29e87-119">-SubscriptionId</span></span>
<span data-ttu-id="29e87-120">Идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="29e87-120">Id of the subscription</span></span>

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

### <span data-ttu-id="29e87-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e87-121">CommonParameters</span></span>
<span data-ttu-id="29e87-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29e87-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e87-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e87-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e87-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29e87-124">INPUTS</span></span>

### <span data-ttu-id="29e87-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="29e87-125">None</span></span>

## <span data-ttu-id="29e87-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29e87-126">OUTPUTS</span></span>

### <span data-ttu-id="29e87-127">Microsoft. Azure. Commands. резервирования. Models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="29e87-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="29e87-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="29e87-128">NOTES</span></span>

## <span data-ttu-id="29e87-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29e87-129">RELATED LINKS</span></span>
