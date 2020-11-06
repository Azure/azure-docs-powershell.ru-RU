---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563352"
---
# <span data-ttu-id="ff32e-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="ff32e-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="ff32e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff32e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff32e-103">Получение каталога для доступного резервирования</span><span class="sxs-lookup"><span data-stu-id="ff32e-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff32e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff32e-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff32e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff32e-105">DESCRIPTION</span></span>
<span data-ttu-id="ff32e-106">Получите регионы и SKU, доступные для зарезервированного экземпляра покупки для указанной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="ff32e-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="ff32e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff32e-107">EXAMPLES</span></span>

### <span data-ttu-id="ff32e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff32e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="ff32e-109">Получение каталога для подписки по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff32e-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="ff32e-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ff32e-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="ff32e-111">Получение каталога для указанной подписки</span><span class="sxs-lookup"><span data-stu-id="ff32e-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="ff32e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff32e-112">PARAMETERS</span></span>

### <span data-ttu-id="ff32e-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff32e-113">-SubscriptionId</span></span>
<span data-ttu-id="ff32e-114">Идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="ff32e-114">Id of the subscription</span></span>

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

### <span data-ttu-id="ff32e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff32e-115">CommonParameters</span></span>
<span data-ttu-id="ff32e-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff32e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff32e-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff32e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff32e-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff32e-118">INPUTS</span></span>

### <span data-ttu-id="ff32e-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="ff32e-119">None</span></span>

## <span data-ttu-id="ff32e-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff32e-120">OUTPUTS</span></span>

### <span data-ttu-id="ff32e-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. резервирования. Models. PSCatalog, Microsoft. Azure. Commands. резервирования, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ff32e-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ff32e-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff32e-122">NOTES</span></span>

## <span data-ttu-id="ff32e-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff32e-123">RELATED LINKS</span></span>

