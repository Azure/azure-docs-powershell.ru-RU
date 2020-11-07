---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720294"
---
# <span data-ttu-id="d6a1f-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="d6a1f-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="d6a1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a1f-103">Получение списка delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="d6a1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6a1f-104">SYNTAX</span></span>

### <span data-ttu-id="d6a1f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6a1f-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="d6a1f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d6a1f-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="d6a1f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6a1f-107">DESCRIPTION</span></span>
<span data-ttu-id="d6a1f-108">Получение списка delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="d6a1f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6a1f-109">EXAMPLES</span></span>

### <span data-ttu-id="d6a1f-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d6a1f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="d6a1f-111">Получение списка делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="d6a1f-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d6a1f-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="d6a1f-113">Получить определенного делегируемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="d6a1f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6a1f-114">PARAMETERS</span></span>

### <span data-ttu-id="d6a1f-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="d6a1f-115">-DelegatedProviderId</span></span>
<span data-ttu-id="d6a1f-116">Идентификатор DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-116">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="d6a1f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a1f-117">CommonParameters</span></span>
<span data-ttu-id="d6a1f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a1f-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a1f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a1f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6a1f-120">INPUTS</span></span>

## <span data-ttu-id="d6a1f-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6a1f-121">OUTPUTS</span></span>

### <span data-ttu-id="d6a1f-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="d6a1f-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="d6a1f-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6a1f-123">NOTES</span></span>

## <span data-ttu-id="d6a1f-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6a1f-124">RELATED LINKS</span></span>

