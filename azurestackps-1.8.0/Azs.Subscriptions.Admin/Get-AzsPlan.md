---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908097"
---
# <span data-ttu-id="888c9-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="888c9-101">Get-AzsPlan</span></span>

## <span data-ttu-id="888c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="888c9-102">SYNOPSIS</span></span>
<span data-ttu-id="888c9-103">Список всех планов для всех подписок.</span><span class="sxs-lookup"><span data-stu-id="888c9-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="888c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="888c9-104">SYNTAX</span></span>

### <span data-ttu-id="888c9-105">ListAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="888c9-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="888c9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="888c9-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="888c9-107">Список</span><span class="sxs-lookup"><span data-stu-id="888c9-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="888c9-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="888c9-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="888c9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="888c9-109">DESCRIPTION</span></span>
<span data-ttu-id="888c9-110">Список всех планов для всех подписок.</span><span class="sxs-lookup"><span data-stu-id="888c9-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="888c9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="888c9-111">EXAMPLES</span></span>

### <span data-ttu-id="888c9-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="888c9-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="888c9-113">Получить план вложения в рамках этой подписки.</span><span class="sxs-lookup"><span data-stu-id="888c9-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="888c9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="888c9-114">PARAMETERS</span></span>

### <span data-ttu-id="888c9-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="888c9-115">-Name</span></span>
<span data-ttu-id="888c9-116">Название плана.</span><span class="sxs-lookup"><span data-stu-id="888c9-116">Name of the plan.</span></span>

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

### <span data-ttu-id="888c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="888c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="888c9-118">Имя группы ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="888c9-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="888c9-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="888c9-119">-ResourceId</span></span>
<span data-ttu-id="888c9-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="888c9-120">The resource id.</span></span>

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

### <span data-ttu-id="888c9-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="888c9-121">-Skip</span></span>
<span data-ttu-id="888c9-122">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="888c9-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="888c9-123">-Top</span><span class="sxs-lookup"><span data-stu-id="888c9-123">-Top</span></span>
<span data-ttu-id="888c9-124">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="888c9-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="888c9-125">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="888c9-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="888c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888c9-126">CommonParameters</span></span>
<span data-ttu-id="888c9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="888c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888c9-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="888c9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888c9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="888c9-129">INPUTS</span></span>

## <span data-ttu-id="888c9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="888c9-130">OUTPUTS</span></span>

### <span data-ttu-id="888c9-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="888c9-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="888c9-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="888c9-132">NOTES</span></span>

## <span data-ttu-id="888c9-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="888c9-133">RELATED LINKS</span></span>

