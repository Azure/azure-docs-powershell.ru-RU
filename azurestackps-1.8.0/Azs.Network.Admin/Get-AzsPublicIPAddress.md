---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908494"
---
# <span data-ttu-id="3cf08-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="3cf08-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="3cf08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3cf08-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf08-103">Список общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3cf08-103">List of public IP addresses.</span></span>

## <span data-ttu-id="3cf08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3cf08-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="3cf08-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cf08-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf08-106">Список общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3cf08-106">List of public IP addresses.</span></span>

## <span data-ttu-id="3cf08-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3cf08-107">EXAMPLES</span></span>

### <span data-ttu-id="3cf08-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="3cf08-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="3cf08-109">Получение списка общедоступных IP-адресов, выделенных или не выделенных.</span><span class="sxs-lookup"><span data-stu-id="3cf08-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="3cf08-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3cf08-110">PARAMETERS</span></span>

### <span data-ttu-id="3cf08-111">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="3cf08-111">-Filter</span></span>
<span data-ttu-id="3cf08-112">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="3cf08-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="3cf08-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="3cf08-113">-OrderBy</span></span>
<span data-ttu-id="3cf08-114">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="3cf08-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="3cf08-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="3cf08-115">-Skip</span></span>
<span data-ttu-id="3cf08-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="3cf08-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3cf08-117">-Top</span><span class="sxs-lookup"><span data-stu-id="3cf08-117">-Top</span></span>
<span data-ttu-id="3cf08-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="3cf08-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3cf08-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="3cf08-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3cf08-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="3cf08-120">-InlineCount</span></span>
<span data-ttu-id="3cf08-121">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="3cf08-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="3cf08-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf08-122">CommonParameters</span></span>
<span data-ttu-id="3cf08-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3cf08-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf08-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf08-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf08-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3cf08-125">INPUTS</span></span>

## <span data-ttu-id="3cf08-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cf08-126">OUTPUTS</span></span>

### <span data-ttu-id="3cf08-127">Microsoft. AzureStack. Management. Network. admin. Models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3cf08-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="3cf08-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3cf08-128">NOTES</span></span>

## <span data-ttu-id="3cf08-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cf08-129">RELATED LINKS</span></span>
