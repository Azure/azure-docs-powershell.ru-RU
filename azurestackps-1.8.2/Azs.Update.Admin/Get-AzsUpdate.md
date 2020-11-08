---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076940"
---
# <span data-ttu-id="c5be2-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="c5be2-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="c5be2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5be2-102">SYNOPSIS</span></span>
<span data-ttu-id="c5be2-103">Получение списка доступных обновлений.</span><span class="sxs-lookup"><span data-stu-id="c5be2-103">Get the list of available updates.</span></span>

## <span data-ttu-id="c5be2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5be2-104">SYNTAX</span></span>

### <span data-ttu-id="c5be2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5be2-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5be2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c5be2-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c5be2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5be2-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c5be2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5be2-108">DESCRIPTION</span></span>
<span data-ttu-id="c5be2-109">Получение списка доступных обновлений.</span><span class="sxs-lookup"><span data-stu-id="c5be2-109">Get the list of available updates.</span></span> <span data-ttu-id="c5be2-110">Обновления, возвращенные из этого модуля, могут быть переданы в "Install-AzsUpdate", если это применимо.</span><span class="sxs-lookup"><span data-stu-id="c5be2-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="c5be2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5be2-111">EXAMPLES</span></span>

### <span data-ttu-id="c5be2-112">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="c5be2-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="c5be2-113">Получение списка доступных обновлений.</span><span class="sxs-lookup"><span data-stu-id="c5be2-113">Get the list of available updates.</span></span>

### <span data-ttu-id="c5be2-114">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="c5be2-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="c5be2-115">Загрузите конкретное обновление.</span><span class="sxs-lookup"><span data-stu-id="c5be2-115">Get the specific update.</span></span>

## <span data-ttu-id="c5be2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5be2-116">PARAMETERS</span></span>

### <span data-ttu-id="c5be2-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5be2-117">-Name</span></span>
<span data-ttu-id="c5be2-118">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="c5be2-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c5be2-119">-Location</span></span>
<span data-ttu-id="c5be2-120">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="c5be2-120">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5be2-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5be2-122">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="c5be2-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5be2-123">-ResourceId</span></span>
<span data-ttu-id="c5be2-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c5be2-124">The resource id.</span></span>

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

### <span data-ttu-id="c5be2-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="c5be2-125">-Skip</span></span>
<span data-ttu-id="c5be2-126">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="c5be2-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be2-127">-Top</span><span class="sxs-lookup"><span data-stu-id="c5be2-127">-Top</span></span>
<span data-ttu-id="c5be2-128">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="c5be2-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c5be2-129">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="c5be2-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5be2-130">CommonParameters</span></span>
<span data-ttu-id="c5be2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5be2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5be2-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5be2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5be2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5be2-133">INPUTS</span></span>

## <span data-ttu-id="c5be2-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5be2-134">OUTPUTS</span></span>

### <span data-ttu-id="c5be2-135">Microsoft. AzureStack. Management. Update. admin. Model. Update</span><span class="sxs-lookup"><span data-stu-id="c5be2-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="c5be2-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5be2-136">NOTES</span></span>

## <span data-ttu-id="c5be2-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5be2-137">RELATED LINKS</span></span>
