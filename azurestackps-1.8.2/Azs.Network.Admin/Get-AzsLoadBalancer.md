---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076951"
---
# <span data-ttu-id="a994c-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a994c-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="a994c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a994c-102">SYNOPSIS</span></span>
<span data-ttu-id="a994c-103">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a994c-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="a994c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a994c-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a994c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a994c-105">DESCRIPTION</span></span>
<span data-ttu-id="a994c-106">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a994c-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="a994c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a994c-107">EXAMPLES</span></span>

### <span data-ttu-id="a994c-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="a994c-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="a994c-109">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a994c-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="a994c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a994c-110">PARAMETERS</span></span>

### <span data-ttu-id="a994c-111">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a994c-111">-Filter</span></span>
<span data-ttu-id="a994c-112">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="a994c-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="a994c-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="a994c-113">-OrderBy</span></span>
<span data-ttu-id="a994c-114">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="a994c-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="a994c-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="a994c-115">-Skip</span></span>
<span data-ttu-id="a994c-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="a994c-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a994c-117">-Top</span><span class="sxs-lookup"><span data-stu-id="a994c-117">-Top</span></span>
<span data-ttu-id="a994c-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="a994c-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a994c-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="a994c-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a994c-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="a994c-120">-InlineCount</span></span>
<span data-ttu-id="a994c-121">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="a994c-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="a994c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a994c-122">CommonParameters</span></span>
<span data-ttu-id="a994c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a994c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a994c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a994c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a994c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a994c-125">INPUTS</span></span>

## <span data-ttu-id="a994c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a994c-126">OUTPUTS</span></span>

### <span data-ttu-id="a994c-127">Microsoft. AzureStack. Management. Networking. admin. Models.</span><span class="sxs-lookup"><span data-stu-id="a994c-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="a994c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a994c-128">NOTES</span></span>

## <span data-ttu-id="a994c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a994c-129">RELATED LINKS</span></span>
