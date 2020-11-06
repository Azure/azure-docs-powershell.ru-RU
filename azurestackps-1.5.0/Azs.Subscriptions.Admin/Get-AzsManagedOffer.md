---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66d8deb8551dfee98c15fcc5524c993c741bca0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555284"
---
# <span data-ttu-id="97da8-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="97da8-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="97da8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97da8-102">SYNOPSIS</span></span>
<span data-ttu-id="97da8-103">Получите список предложенных операторов.</span><span class="sxs-lookup"><span data-stu-id="97da8-103">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="97da8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97da8-104">SYNTAX</span></span>

### <span data-ttu-id="97da8-105">ListAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97da8-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="97da8-106">Получить</span><span class="sxs-lookup"><span data-stu-id="97da8-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="97da8-107">Список</span><span class="sxs-lookup"><span data-stu-id="97da8-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="97da8-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="97da8-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="97da8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97da8-109">DESCRIPTION</span></span>
<span data-ttu-id="97da8-110">Получите список предложенных.</span><span class="sxs-lookup"><span data-stu-id="97da8-110">Get the list of offers.</span></span>

## <span data-ttu-id="97da8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97da8-111">EXAMPLES</span></span>

### <span data-ttu-id="97da8-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="97da8-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="97da8-113">Получите список предложенных операторов.</span><span class="sxs-lookup"><span data-stu-id="97da8-113">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="97da8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97da8-114">PARAMETERS</span></span>

### <span data-ttu-id="97da8-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97da8-115">-Name</span></span>
<span data-ttu-id="97da8-116">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="97da8-116">Name of an offer.</span></span>

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

### <span data-ttu-id="97da8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97da8-117">-ResourceGroupName</span></span>
<span data-ttu-id="97da8-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="97da8-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="97da8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97da8-119">-ResourceId</span></span>
<span data-ttu-id="97da8-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="97da8-120">The resource id.</span></span>

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

### <span data-ttu-id="97da8-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="97da8-121">-Skip</span></span>
<span data-ttu-id="97da8-122">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="97da8-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="97da8-123">-Top</span><span class="sxs-lookup"><span data-stu-id="97da8-123">-Top</span></span>
<span data-ttu-id="97da8-124">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="97da8-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="97da8-125">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="97da8-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="97da8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97da8-126">CommonParameters</span></span>
<span data-ttu-id="97da8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97da8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97da8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97da8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97da8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97da8-129">INPUTS</span></span>

## <span data-ttu-id="97da8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97da8-130">OUTPUTS</span></span>

### <span data-ttu-id="97da8-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Offer</span><span class="sxs-lookup"><span data-stu-id="97da8-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="97da8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="97da8-132">NOTES</span></span>

## <span data-ttu-id="97da8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97da8-133">RELATED LINKS</span></span>

