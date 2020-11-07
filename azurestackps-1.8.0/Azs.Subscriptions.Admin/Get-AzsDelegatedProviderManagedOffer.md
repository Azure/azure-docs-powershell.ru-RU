---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908477"
---
# <span data-ttu-id="cbd75-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="cbd75-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="cbd75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbd75-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd75-103">Получение списка предлагаемых провайдеров делегирования.</span><span class="sxs-lookup"><span data-stu-id="cbd75-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="cbd75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbd75-104">SYNTAX</span></span>

### <span data-ttu-id="cbd75-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbd75-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbd75-106">Получить</span><span class="sxs-lookup"><span data-stu-id="cbd75-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="cbd75-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd75-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cbd75-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbd75-108">DESCRIPTION</span></span>
<span data-ttu-id="cbd75-109">Получение списка предлагаемых провайдеров делегирования.</span><span class="sxs-lookup"><span data-stu-id="cbd75-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="cbd75-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbd75-110">EXAMPLES</span></span>

### <span data-ttu-id="cbd75-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cbd75-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="cbd75-112">Получение списка предлагаемых провайдеров делегирования.</span><span class="sxs-lookup"><span data-stu-id="cbd75-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="cbd75-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbd75-113">PARAMETERS</span></span>

### <span data-ttu-id="cbd75-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="cbd75-114">-DelegatedProviderId</span></span>
<span data-ttu-id="cbd75-115">Идентификатор DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="cbd75-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd75-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbd75-116">-Name</span></span>
<span data-ttu-id="cbd75-117">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="cbd75-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd75-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd75-118">-ResourceId</span></span>
<span data-ttu-id="cbd75-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="cbd75-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd75-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="cbd75-120">-Skip</span></span>
<span data-ttu-id="cbd75-121">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="cbd75-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd75-122">-Top</span><span class="sxs-lookup"><span data-stu-id="cbd75-122">-Top</span></span>
<span data-ttu-id="cbd75-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="cbd75-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cbd75-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="cbd75-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd75-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd75-125">CommonParameters</span></span>
<span data-ttu-id="cbd75-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbd75-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd75-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd75-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd75-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbd75-128">INPUTS</span></span>

## <span data-ttu-id="cbd75-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbd75-129">OUTPUTS</span></span>

### <span data-ttu-id="cbd75-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="cbd75-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="cbd75-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbd75-131">NOTES</span></span>

## <span data-ttu-id="cbd75-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbd75-132">RELATED LINKS</span></span>

