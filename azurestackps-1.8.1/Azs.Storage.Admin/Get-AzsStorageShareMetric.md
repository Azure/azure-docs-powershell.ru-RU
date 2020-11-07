---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 80c80cb38013701d3e58d6d6bf77f774e2d61548
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909218"
---
# <span data-ttu-id="14461-101">Get-AzsStorageShareMetric</span><span class="sxs-lookup"><span data-stu-id="14461-101">Get-AzsStorageShareMetric</span></span>

## <span data-ttu-id="14461-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14461-102">SYNOPSIS</span></span>
<span data-ttu-id="14461-103">Возвращает список метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="14461-103">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="14461-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14461-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetric [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="14461-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14461-105">DESCRIPTION</span></span>
<span data-ttu-id="14461-106">Возвращает список метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="14461-106">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="14461-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14461-107">EXAMPLES</span></span>

### <span data-ttu-id="14461-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="14461-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="14461-109">Получение списка метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="14461-109">Get the list of metrics for a storage share.</span></span>

## <span data-ttu-id="14461-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14461-110">PARAMETERS</span></span>

### <span data-ttu-id="14461-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="14461-111">-FarmName</span></span>
<span data-ttu-id="14461-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="14461-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14461-113">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="14461-113">-ShareName</span></span>
<span data-ttu-id="14461-114">Имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="14461-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14461-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14461-115">-ResourceGroupName</span></span>
<span data-ttu-id="14461-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14461-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14461-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="14461-117">-Skip</span></span>
<span data-ttu-id="14461-118">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="14461-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="14461-119">-Top</span><span class="sxs-lookup"><span data-stu-id="14461-119">-Top</span></span>
<span data-ttu-id="14461-120">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="14461-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="14461-121">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="14461-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14461-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14461-122">CommonParameters</span></span>
<span data-ttu-id="14461-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14461-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14461-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14461-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14461-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14461-125">INPUTS</span></span>

## <span data-ttu-id="14461-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14461-126">OUTPUTS</span></span>

### <span data-ttu-id="14461-127">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="14461-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="14461-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="14461-128">NOTES</span></span>

## <span data-ttu-id="14461-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14461-129">RELATED LINKS</span></span>
