---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43691cfa3299fc0534ce2d44fd2a2f6ed1043d04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556128"
---
# <span data-ttu-id="70130-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70130-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="70130-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70130-102">SYNOPSIS</span></span>
<span data-ttu-id="70130-103">Получение списка всех виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="70130-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="70130-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70130-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="70130-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70130-105">DESCRIPTION</span></span>
<span data-ttu-id="70130-106">Получение списка всех виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="70130-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="70130-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70130-107">EXAMPLES</span></span>

### <span data-ttu-id="70130-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="70130-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="70130-109">Возврат списка виртуальных сетей для метки стека Azure.</span><span class="sxs-lookup"><span data-stu-id="70130-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="70130-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70130-110">PARAMETERS</span></span>

### <span data-ttu-id="70130-111">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="70130-111">-Filter</span></span>
<span data-ttu-id="70130-112">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="70130-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="70130-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="70130-113">-InlineCount</span></span>
<span data-ttu-id="70130-114">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="70130-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="70130-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="70130-115">-OrderBy</span></span>
<span data-ttu-id="70130-116">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="70130-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="70130-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="70130-117">-Skip</span></span>
<span data-ttu-id="70130-118">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="70130-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="70130-119">-Top</span><span class="sxs-lookup"><span data-stu-id="70130-119">-Top</span></span>
<span data-ttu-id="70130-120">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="70130-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="70130-121">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="70130-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="70130-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70130-122">CommonParameters</span></span>
<span data-ttu-id="70130-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70130-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70130-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70130-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70130-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70130-125">INPUTS</span></span>

## <span data-ttu-id="70130-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70130-126">OUTPUTS</span></span>

### <span data-ttu-id="70130-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70130-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="70130-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="70130-128">NOTES</span></span>

## <span data-ttu-id="70130-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70130-129">RELATED LINKS</span></span>

