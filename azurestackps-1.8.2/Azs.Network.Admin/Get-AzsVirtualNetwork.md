---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076963"
---
# <span data-ttu-id="c8e5d-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8e5d-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="c8e5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e5d-103">Получение списка всех виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="c8e5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8e5d-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8e5d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8e5d-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e5d-106">Получение списка всех виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="c8e5d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8e5d-107">EXAMPLES</span></span>

### <span data-ttu-id="c8e5d-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="c8e5d-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="c8e5d-109">Возврат списка виртуальных сетей для метки стека Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="c8e5d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8e5d-110">PARAMETERS</span></span>

### <span data-ttu-id="c8e5d-111">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="c8e5d-111">-Filter</span></span>
<span data-ttu-id="c8e5d-112">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="c8e5d-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c8e5d-113">-OrderBy</span></span>
<span data-ttu-id="c8e5d-114">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="c8e5d-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="c8e5d-115">-Skip</span></span>
<span data-ttu-id="c8e5d-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c8e5d-117">-Top</span><span class="sxs-lookup"><span data-stu-id="c8e5d-117">-Top</span></span>
<span data-ttu-id="c8e5d-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c8e5d-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c8e5d-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="c8e5d-120">-InlineCount</span></span>
<span data-ttu-id="c8e5d-121">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="c8e5d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e5d-122">CommonParameters</span></span>
<span data-ttu-id="c8e5d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8e5d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e5d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e5d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e5d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8e5d-125">INPUTS</span></span>

## <span data-ttu-id="c8e5d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8e5d-126">OUTPUTS</span></span>

### <span data-ttu-id="c8e5d-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8e5d-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="c8e5d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8e5d-128">NOTES</span></span>

## <span data-ttu-id="c8e5d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8e5d-129">RELATED LINKS</span></span>