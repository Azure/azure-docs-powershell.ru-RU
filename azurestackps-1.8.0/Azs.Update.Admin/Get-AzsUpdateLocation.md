---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908358"
---
# <span data-ttu-id="4c1fd-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="4c1fd-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="4c1fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="4c1fd-103">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="4c1fd-103">Get the list of update locations.</span></span>

## <span data-ttu-id="4c1fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c1fd-104">SYNTAX</span></span>

### <span data-ttu-id="4c1fd-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c1fd-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4c1fd-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4c1fd-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4c1fd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c1fd-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4c1fd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c1fd-108">DESCRIPTION</span></span>
<span data-ttu-id="4c1fd-109">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="4c1fd-109">Get the list of update locations.</span></span> <span data-ttu-id="4c1fd-110">Возвращенные расположения можно использовать для получения доступных обновлений в определенном расположении с помощью Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="4c1fd-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="4c1fd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c1fd-111">EXAMPLES</span></span>

### <span data-ttu-id="4c1fd-112">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="4c1fd-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="4c1fd-113">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="4c1fd-113">Get the list of update locations.</span></span>

## <span data-ttu-id="4c1fd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c1fd-114">PARAMETERS</span></span>

### <span data-ttu-id="4c1fd-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4c1fd-115">-Location</span></span>
<span data-ttu-id="4c1fd-116">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="4c1fd-116">Name of the Location.</span></span>

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

### <span data-ttu-id="4c1fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c1fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="4c1fd-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="4c1fd-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4c1fd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c1fd-119">-ResourceId</span></span>
<span data-ttu-id="4c1fd-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c1fd-120">The resource id.</span></span>

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

### <span data-ttu-id="4c1fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c1fd-121">CommonParameters</span></span>
<span data-ttu-id="4c1fd-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c1fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c1fd-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c1fd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c1fd-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c1fd-124">INPUTS</span></span>

## <span data-ttu-id="4c1fd-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c1fd-125">OUTPUTS</span></span>

### <span data-ttu-id="4c1fd-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="4c1fd-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="4c1fd-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c1fd-127">NOTES</span></span>

## <span data-ttu-id="4c1fd-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c1fd-128">RELATED LINKS</span></span>
