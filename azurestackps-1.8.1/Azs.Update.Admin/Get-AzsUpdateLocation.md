---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908953"
---
# <span data-ttu-id="bee4b-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="bee4b-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="bee4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bee4b-102">SYNOPSIS</span></span>
<span data-ttu-id="bee4b-103">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="bee4b-103">Get the list of update locations.</span></span>

## <span data-ttu-id="bee4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bee4b-104">SYNTAX</span></span>

### <span data-ttu-id="bee4b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bee4b-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bee4b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="bee4b-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bee4b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bee4b-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bee4b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bee4b-108">DESCRIPTION</span></span>
<span data-ttu-id="bee4b-109">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="bee4b-109">Get the list of update locations.</span></span> <span data-ttu-id="bee4b-110">Возвращенные расположения можно использовать для получения доступных обновлений в определенном расположении с помощью Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="bee4b-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="bee4b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bee4b-111">EXAMPLES</span></span>

### <span data-ttu-id="bee4b-112">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="bee4b-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="bee4b-113">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="bee4b-113">Get the list of update locations.</span></span>

## <span data-ttu-id="bee4b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bee4b-114">PARAMETERS</span></span>

### <span data-ttu-id="bee4b-115">-Location</span><span class="sxs-lookup"><span data-stu-id="bee4b-115">-Location</span></span>
<span data-ttu-id="bee4b-116">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="bee4b-116">Name of the Location.</span></span>

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

### <span data-ttu-id="bee4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="bee4b-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="bee4b-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="bee4b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bee4b-119">-ResourceId</span></span>
<span data-ttu-id="bee4b-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="bee4b-120">The resource id.</span></span>

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

### <span data-ttu-id="bee4b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee4b-121">CommonParameters</span></span>
<span data-ttu-id="bee4b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bee4b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee4b-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee4b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee4b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bee4b-124">INPUTS</span></span>

## <span data-ttu-id="bee4b-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bee4b-125">OUTPUTS</span></span>

### <span data-ttu-id="bee4b-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="bee4b-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="bee4b-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="bee4b-127">NOTES</span></span>

## <span data-ttu-id="bee4b-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bee4b-128">RELATED LINKS</span></span>
