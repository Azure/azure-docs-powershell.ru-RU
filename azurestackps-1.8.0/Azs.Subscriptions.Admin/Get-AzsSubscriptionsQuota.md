---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908445"
---
# <span data-ttu-id="74e3c-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="74e3c-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="74e3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="74e3c-103">Получите список квот поставщиков ресурсов подписки в местоположении.</span><span class="sxs-lookup"><span data-stu-id="74e3c-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="74e3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74e3c-104">SYNTAX</span></span>

### <span data-ttu-id="74e3c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74e3c-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="74e3c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="74e3c-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="74e3c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="74e3c-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="74e3c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74e3c-108">DESCRIPTION</span></span>
<span data-ttu-id="74e3c-109">Получите список квот в местоположении.</span><span class="sxs-lookup"><span data-stu-id="74e3c-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="74e3c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74e3c-110">EXAMPLES</span></span>

### <span data-ttu-id="74e3c-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="74e3c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="74e3c-112">Получите список квот поставщиков ресурсов подписки в местоположении.</span><span class="sxs-lookup"><span data-stu-id="74e3c-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="74e3c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74e3c-113">PARAMETERS</span></span>

### <span data-ttu-id="74e3c-114">-Location</span><span class="sxs-lookup"><span data-stu-id="74e3c-114">-Location</span></span>
<span data-ttu-id="74e3c-115">Расположение AzureStack.</span><span class="sxs-lookup"><span data-stu-id="74e3c-115">The AzureStack location.</span></span>

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

### <span data-ttu-id="74e3c-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74e3c-116">-Name</span></span>
<span data-ttu-id="74e3c-117">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="74e3c-117">Name of the quota.</span></span>

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

### <span data-ttu-id="74e3c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74e3c-118">-ResourceId</span></span>
<span data-ttu-id="74e3c-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="74e3c-119">The resource id.</span></span>

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

### <span data-ttu-id="74e3c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e3c-120">CommonParameters</span></span>
<span data-ttu-id="74e3c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74e3c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e3c-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e3c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e3c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74e3c-123">INPUTS</span></span>

## <span data-ttu-id="74e3c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74e3c-124">OUTPUTS</span></span>

### <span data-ttu-id="74e3c-125">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="74e3c-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="74e3c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="74e3c-126">NOTES</span></span>

## <span data-ttu-id="74e3c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74e3c-127">RELATED LINKS</span></span>

