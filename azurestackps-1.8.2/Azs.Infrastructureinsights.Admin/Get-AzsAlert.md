---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076916"
---
# <span data-ttu-id="78cbc-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="78cbc-101">Get-AzsAlert</span></span>

## <span data-ttu-id="78cbc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="78cbc-103">Возвращает список всех оповещений в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="78cbc-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="78cbc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78cbc-104">SYNTAX</span></span>

### <span data-ttu-id="78cbc-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78cbc-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="78cbc-106">Получить</span><span class="sxs-lookup"><span data-stu-id="78cbc-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="78cbc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="78cbc-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="78cbc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78cbc-108">DESCRIPTION</span></span>
<span data-ttu-id="78cbc-109">Возвращает список всех оповещений в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="78cbc-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="78cbc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78cbc-110">EXAMPLES</span></span>

### <span data-ttu-id="78cbc-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="78cbc-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="78cbc-112">Получить оповещение по имени.</span><span class="sxs-lookup"><span data-stu-id="78cbc-112">Get an alert by Name.</span></span>

### <span data-ttu-id="78cbc-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="78cbc-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="78cbc-114">Получение всех активных оповещений и отображение их ошибок и названий.</span><span class="sxs-lookup"><span data-stu-id="78cbc-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="78cbc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78cbc-115">PARAMETERS</span></span>

### <span data-ttu-id="78cbc-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78cbc-116">-Name</span></span>
<span data-ttu-id="78cbc-117">Идентификатор оповещения.</span><span class="sxs-lookup"><span data-stu-id="78cbc-117">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78cbc-118">-Location</span><span class="sxs-lookup"><span data-stu-id="78cbc-118">-Location</span></span>
<span data-ttu-id="78cbc-119">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="78cbc-119">Name of the location.</span></span>

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

### <span data-ttu-id="78cbc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cbc-120">-ResourceGroupName</span></span>
<span data-ttu-id="78cbc-121">Имя группы ресурсов для оповещения.</span><span class="sxs-lookup"><span data-stu-id="78cbc-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="78cbc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78cbc-122">-ResourceId</span></span>
<span data-ttu-id="78cbc-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="78cbc-123">The resource id.</span></span>

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

### <span data-ttu-id="78cbc-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="78cbc-124">-Filter</span></span>
<span data-ttu-id="78cbc-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="78cbc-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78cbc-126">-Top</span><span class="sxs-lookup"><span data-stu-id="78cbc-126">-Top</span></span>
<span data-ttu-id="78cbc-127">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="78cbc-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="78cbc-128">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="78cbc-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="78cbc-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="78cbc-129">-Skip</span></span>
<span data-ttu-id="78cbc-130">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="78cbc-130">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="78cbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cbc-131">CommonParameters</span></span>
<span data-ttu-id="78cbc-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78cbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cbc-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78cbc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cbc-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78cbc-134">INPUTS</span></span>

## <span data-ttu-id="78cbc-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78cbc-135">OUTPUTS</span></span>

### <span data-ttu-id="78cbc-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="78cbc-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="78cbc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="78cbc-137">NOTES</span></span>

## <span data-ttu-id="78cbc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78cbc-138">RELATED LINKS</span></span>
