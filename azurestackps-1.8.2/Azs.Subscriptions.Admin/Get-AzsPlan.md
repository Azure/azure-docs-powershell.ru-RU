---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076748"
---
# <span data-ttu-id="adc3c-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="adc3c-101">Get-AzsPlan</span></span>

## <span data-ttu-id="adc3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="adc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="adc3c-103">Список всех планов для всех подписок.</span><span class="sxs-lookup"><span data-stu-id="adc3c-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="adc3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="adc3c-104">SYNTAX</span></span>

### <span data-ttu-id="adc3c-105">ListAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adc3c-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="adc3c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="adc3c-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="adc3c-107">Список</span><span class="sxs-lookup"><span data-stu-id="adc3c-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="adc3c-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="adc3c-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="adc3c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adc3c-109">DESCRIPTION</span></span>
<span data-ttu-id="adc3c-110">Список всех планов для всех подписок.</span><span class="sxs-lookup"><span data-stu-id="adc3c-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="adc3c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="adc3c-111">EXAMPLES</span></span>

### <span data-ttu-id="adc3c-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="adc3c-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="adc3c-113">Получить план вложения в рамках этой подписки.</span><span class="sxs-lookup"><span data-stu-id="adc3c-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="adc3c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="adc3c-114">PARAMETERS</span></span>

### <span data-ttu-id="adc3c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="adc3c-115">-Name</span></span>
<span data-ttu-id="adc3c-116">Название плана.</span><span class="sxs-lookup"><span data-stu-id="adc3c-116">Name of the plan.</span></span>

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

### <span data-ttu-id="adc3c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc3c-117">-ResourceGroupName</span></span>
<span data-ttu-id="adc3c-118">Имя группы ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="adc3c-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc3c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adc3c-119">-ResourceId</span></span>
<span data-ttu-id="adc3c-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="adc3c-120">The resource id.</span></span>

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

### <span data-ttu-id="adc3c-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="adc3c-121">-Skip</span></span>
<span data-ttu-id="adc3c-122">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="adc3c-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc3c-123">-Top</span><span class="sxs-lookup"><span data-stu-id="adc3c-123">-Top</span></span>
<span data-ttu-id="adc3c-124">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="adc3c-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="adc3c-125">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="adc3c-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc3c-126">CommonParameters</span></span>
<span data-ttu-id="adc3c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="adc3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc3c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc3c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc3c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="adc3c-129">INPUTS</span></span>

## <span data-ttu-id="adc3c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="adc3c-130">OUTPUTS</span></span>

### <span data-ttu-id="adc3c-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="adc3c-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="adc3c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="adc3c-132">NOTES</span></span>

## <span data-ttu-id="adc3c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adc3c-133">RELATED LINKS</span></span>

