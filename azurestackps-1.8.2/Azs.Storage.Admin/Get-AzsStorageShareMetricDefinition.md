---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e127b0cb9198471d237df62bfedf8d2d57ecdca2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077091"
---
# <span data-ttu-id="3582d-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="3582d-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="3582d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3582d-102">SYNOPSIS</span></span>
<span data-ttu-id="3582d-103">Возвращает список определений метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3582d-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="3582d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3582d-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3582d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3582d-105">DESCRIPTION</span></span>
<span data-ttu-id="3582d-106">Возвращает список определений метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3582d-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="3582d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3582d-107">EXAMPLES</span></span>

### <span data-ttu-id="3582d-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="3582d-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="3582d-109">Получение списка определений метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3582d-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="3582d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3582d-110">PARAMETERS</span></span>

### <span data-ttu-id="3582d-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="3582d-111">-FarmName</span></span>
<span data-ttu-id="3582d-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="3582d-112">Farm Id.</span></span>

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

### <span data-ttu-id="3582d-113">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="3582d-113">-ShareName</span></span>
<span data-ttu-id="3582d-114">Имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="3582d-114">Share name.</span></span>

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

### <span data-ttu-id="3582d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3582d-115">-ResourceGroupName</span></span>
<span data-ttu-id="3582d-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3582d-116">Resource group name.</span></span>

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

### <span data-ttu-id="3582d-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="3582d-117">-Skip</span></span>
<span data-ttu-id="3582d-118">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="3582d-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3582d-119">-Top</span><span class="sxs-lookup"><span data-stu-id="3582d-119">-Top</span></span>
<span data-ttu-id="3582d-120">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="3582d-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3582d-121">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="3582d-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3582d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3582d-122">CommonParameters</span></span>
<span data-ttu-id="3582d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3582d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3582d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3582d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3582d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3582d-125">INPUTS</span></span>

## <span data-ttu-id="3582d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3582d-126">OUTPUTS</span></span>

### <span data-ttu-id="3582d-127">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="3582d-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="3582d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3582d-128">NOTES</span></span>

## <span data-ttu-id="3582d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3582d-129">RELATED LINKS</span></span>
