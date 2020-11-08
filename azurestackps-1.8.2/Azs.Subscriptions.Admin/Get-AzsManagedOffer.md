---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076826"
---
# <span data-ttu-id="39883-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="39883-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="39883-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39883-102">SYNOPSIS</span></span>
<span data-ttu-id="39883-103">Получите список предложенных для администратора.</span><span class="sxs-lookup"><span data-stu-id="39883-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="39883-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39883-104">SYNTAX</span></span>

### <span data-ttu-id="39883-105">ListAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39883-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="39883-106">Получить</span><span class="sxs-lookup"><span data-stu-id="39883-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="39883-107">Список</span><span class="sxs-lookup"><span data-stu-id="39883-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="39883-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="39883-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="39883-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39883-109">DESCRIPTION</span></span>
<span data-ttu-id="39883-110">Получите список предложенных.</span><span class="sxs-lookup"><span data-stu-id="39883-110">Get the list of offers.</span></span>

## <span data-ttu-id="39883-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39883-111">EXAMPLES</span></span>

### <span data-ttu-id="39883-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="39883-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="39883-113">Получите список предложенных для администратора.</span><span class="sxs-lookup"><span data-stu-id="39883-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="39883-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39883-114">PARAMETERS</span></span>

### <span data-ttu-id="39883-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39883-115">-Name</span></span>
<span data-ttu-id="39883-116">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="39883-116">Name of an offer.</span></span>

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

### <span data-ttu-id="39883-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39883-117">-ResourceGroupName</span></span>
<span data-ttu-id="39883-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="39883-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="39883-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39883-119">-ResourceId</span></span>
<span data-ttu-id="39883-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="39883-120">The resource id.</span></span>

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

### <span data-ttu-id="39883-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="39883-121">-Skip</span></span>
<span data-ttu-id="39883-122">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="39883-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="39883-123">-Top</span><span class="sxs-lookup"><span data-stu-id="39883-123">-Top</span></span>
<span data-ttu-id="39883-124">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="39883-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="39883-125">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="39883-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="39883-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39883-126">CommonParameters</span></span>
<span data-ttu-id="39883-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39883-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39883-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39883-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39883-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39883-129">INPUTS</span></span>

## <span data-ttu-id="39883-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39883-130">OUTPUTS</span></span>

### <span data-ttu-id="39883-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Offer</span><span class="sxs-lookup"><span data-stu-id="39883-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="39883-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="39883-132">NOTES</span></span>

## <span data-ttu-id="39883-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39883-133">RELATED LINKS</span></span>

