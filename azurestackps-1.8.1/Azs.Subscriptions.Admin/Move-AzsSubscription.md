---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908746"
---
# <span data-ttu-id="a2834-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="a2834-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="a2834-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2834-102">SYNOPSIS</span></span>
<span data-ttu-id="a2834-103">Перемещение подписок между предлагаемыми поставщиками делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a2834-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="a2834-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2834-104">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="a2834-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2834-105">DESCRIPTION</span></span>
<span data-ttu-id="a2834-106">Перемещение подписок между предлагаемыми поставщиками делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a2834-106">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="a2834-107">Этот процесс будет выполнять только изменение фирменной символики, но базовые предложения, планы, квоты для подписок не изменяются.</span><span class="sxs-lookup"><span data-stu-id="a2834-107">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="a2834-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2834-108">EXAMPLES</span></span>

### <span data-ttu-id="a2834-109">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2834-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="a2834-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/Offers/Ro1"-ResourceId "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="a2834-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="a2834-111">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2834-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="a2834-112">$resourceIds = Get-AzsUserSubscription-Filter "offerName EQ" O1 "" | where {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | SELECT-ExpandProperty ID Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="a2834-112">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="a2834-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2834-113">PARAMETERS</span></span>

### <span data-ttu-id="a2834-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2834-114">-AsJob</span></span>
<span data-ttu-id="a2834-115">Указывает, должна ли операция перемещения выполняться как задание.</span><span class="sxs-lookup"><span data-stu-id="a2834-115">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2834-116">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="a2834-116">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="a2834-117">Указывает полный предоставленный поставщик делегирования, на который этот командлет перемещает подписки.</span><span class="sxs-lookup"><span data-stu-id="a2834-117">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="a2834-118">NULL, если нужно вернуть подписки обратно поставщику по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2834-118">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2834-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2834-119">-ResourceId</span></span>
<span data-ttu-id="a2834-120">Задает массив полных идентификаторов ресурсов подписки, перемещается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a2834-120">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2834-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2834-121">CommonParameters</span></span>
<span data-ttu-id="a2834-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2834-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2834-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2834-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2834-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2834-124">INPUTS</span></span>

## <span data-ttu-id="a2834-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2834-125">OUTPUTS</span></span>

## <span data-ttu-id="a2834-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2834-126">NOTES</span></span>

## <span data-ttu-id="a2834-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2834-127">RELATED LINKS</span></span>

