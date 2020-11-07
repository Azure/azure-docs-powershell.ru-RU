---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908514"
---
# <span data-ttu-id="79801-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79801-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="79801-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79801-102">SYNOPSIS</span></span>
<span data-ttu-id="79801-103">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79801-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="79801-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79801-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="79801-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79801-105">DESCRIPTION</span></span>
<span data-ttu-id="79801-106">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79801-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="79801-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79801-107">EXAMPLES</span></span>

### <span data-ttu-id="79801-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="79801-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="79801-109">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79801-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="79801-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79801-110">PARAMETERS</span></span>

### <span data-ttu-id="79801-111">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="79801-111">-Filter</span></span>
<span data-ttu-id="79801-112">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="79801-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="79801-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="79801-113">-OrderBy</span></span>
<span data-ttu-id="79801-114">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="79801-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79801-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="79801-115">-Skip</span></span>
<span data-ttu-id="79801-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="79801-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79801-117">-Top</span><span class="sxs-lookup"><span data-stu-id="79801-117">-Top</span></span>
<span data-ttu-id="79801-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="79801-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="79801-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="79801-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79801-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="79801-120">-InlineCount</span></span>
<span data-ttu-id="79801-121">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="79801-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79801-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79801-122">CommonParameters</span></span>
<span data-ttu-id="79801-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79801-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79801-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79801-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79801-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79801-125">INPUTS</span></span>

## <span data-ttu-id="79801-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79801-126">OUTPUTS</span></span>

### <span data-ttu-id="79801-127">Microsoft. AzureStack. Management. Networking. admin. Models.</span><span class="sxs-lookup"><span data-stu-id="79801-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="79801-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="79801-128">NOTES</span></span>

## <span data-ttu-id="79801-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79801-129">RELATED LINKS</span></span>
