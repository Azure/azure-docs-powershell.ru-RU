---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908749"
---
# <span data-ttu-id="7523b-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="7523b-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="7523b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7523b-102">SYNOPSIS</span></span>
<span data-ttu-id="7523b-103">Получите список квот поставщиков ресурсов подписки в местоположении.</span><span class="sxs-lookup"><span data-stu-id="7523b-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="7523b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7523b-104">SYNTAX</span></span>

### <span data-ttu-id="7523b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7523b-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="7523b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="7523b-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="7523b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7523b-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7523b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7523b-108">DESCRIPTION</span></span>
<span data-ttu-id="7523b-109">Получите список квот в местоположении.</span><span class="sxs-lookup"><span data-stu-id="7523b-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="7523b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7523b-110">EXAMPLES</span></span>

### <span data-ttu-id="7523b-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7523b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="7523b-112">Получите список квот поставщиков ресурсов подписки в местоположении.</span><span class="sxs-lookup"><span data-stu-id="7523b-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="7523b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7523b-113">PARAMETERS</span></span>

### <span data-ttu-id="7523b-114">-Location</span><span class="sxs-lookup"><span data-stu-id="7523b-114">-Location</span></span>
<span data-ttu-id="7523b-115">Расположение AzureStack.</span><span class="sxs-lookup"><span data-stu-id="7523b-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7523b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7523b-116">-Name</span></span>
<span data-ttu-id="7523b-117">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="7523b-117">Name of the quota.</span></span>

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

### <span data-ttu-id="7523b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7523b-118">-ResourceId</span></span>
<span data-ttu-id="7523b-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="7523b-119">The resource id.</span></span>

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

### <span data-ttu-id="7523b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7523b-120">CommonParameters</span></span>
<span data-ttu-id="7523b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7523b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7523b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7523b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7523b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7523b-123">INPUTS</span></span>

## <span data-ttu-id="7523b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7523b-124">OUTPUTS</span></span>

### <span data-ttu-id="7523b-125">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="7523b-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="7523b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="7523b-126">NOTES</span></span>

## <span data-ttu-id="7523b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7523b-127">RELATED LINKS</span></span>

