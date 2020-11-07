---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909221"
---
# <span data-ttu-id="14587-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="14587-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="14587-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14587-102">SYNOPSIS</span></span>
<span data-ttu-id="14587-103">Получение списка delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="14587-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="14587-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14587-104">SYNTAX</span></span>

### <span data-ttu-id="14587-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14587-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="14587-106">Получить</span><span class="sxs-lookup"><span data-stu-id="14587-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="14587-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14587-107">DESCRIPTION</span></span>
<span data-ttu-id="14587-108">Получение списка delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="14587-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="14587-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14587-109">EXAMPLES</span></span>

### <span data-ttu-id="14587-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14587-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="14587-111">Получение списка делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="14587-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="14587-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="14587-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="14587-113">Получить определенного делегируемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="14587-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="14587-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14587-114">PARAMETERS</span></span>

### <span data-ttu-id="14587-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="14587-115">-DelegatedProviderId</span></span>
<span data-ttu-id="14587-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="14587-116">{{Fill DelegatedProviderId Description}}</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14587-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14587-117">CommonParameters</span></span>
<span data-ttu-id="14587-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14587-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14587-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14587-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14587-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14587-120">INPUTS</span></span>

## <span data-ttu-id="14587-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14587-121">OUTPUTS</span></span>

### <span data-ttu-id="14587-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="14587-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="14587-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="14587-123">NOTES</span></span>

## <span data-ttu-id="14587-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14587-124">RELATED LINKS</span></span>

