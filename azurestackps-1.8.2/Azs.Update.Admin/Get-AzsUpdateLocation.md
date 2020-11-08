---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076935"
---
# <span data-ttu-id="88d6f-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="88d6f-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="88d6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="88d6f-103">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="88d6f-103">Get the list of update locations.</span></span>

## <span data-ttu-id="88d6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88d6f-104">SYNTAX</span></span>

### <span data-ttu-id="88d6f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88d6f-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="88d6f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="88d6f-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="88d6f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="88d6f-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="88d6f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="88d6f-109">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="88d6f-109">Get the list of update locations.</span></span> <span data-ttu-id="88d6f-110">Возвращенные расположения можно использовать для получения доступных обновлений в определенном расположении с помощью Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="88d6f-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="88d6f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88d6f-111">EXAMPLES</span></span>

### <span data-ttu-id="88d6f-112">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="88d6f-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="88d6f-113">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="88d6f-113">Get the list of update locations.</span></span>

## <span data-ttu-id="88d6f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88d6f-114">PARAMETERS</span></span>

### <span data-ttu-id="88d6f-115">-Location</span><span class="sxs-lookup"><span data-stu-id="88d6f-115">-Location</span></span>
<span data-ttu-id="88d6f-116">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="88d6f-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d6f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88d6f-117">-ResourceGroupName</span></span>
<span data-ttu-id="88d6f-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="88d6f-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="88d6f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88d6f-119">-ResourceId</span></span>
<span data-ttu-id="88d6f-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="88d6f-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88d6f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d6f-121">CommonParameters</span></span>
<span data-ttu-id="88d6f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88d6f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d6f-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d6f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d6f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88d6f-124">INPUTS</span></span>

## <span data-ttu-id="88d6f-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88d6f-125">OUTPUTS</span></span>

### <span data-ttu-id="88d6f-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="88d6f-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="88d6f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="88d6f-127">NOTES</span></span>

## <span data-ttu-id="88d6f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88d6f-128">RELATED LINKS</span></span>
