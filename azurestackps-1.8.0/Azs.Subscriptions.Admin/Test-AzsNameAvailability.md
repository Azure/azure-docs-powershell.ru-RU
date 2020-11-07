---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908034"
---
# <span data-ttu-id="82929-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="82929-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="82929-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82929-102">SYNOPSIS</span></span>
<span data-ttu-id="82929-103">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="82929-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="82929-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82929-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="82929-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82929-105">DESCRIPTION</span></span>
<span data-ttu-id="82929-106">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="82929-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="82929-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82929-107">EXAMPLES</span></span>

### <span data-ttu-id="82929-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="82929-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="82929-109">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="82929-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="82929-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82929-110">PARAMETERS</span></span>

### <span data-ttu-id="82929-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82929-111">-Name</span></span>
<span data-ttu-id="82929-112">Имя проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="82929-112">The resource name to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82929-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="82929-113">-ResourceType</span></span>
<span data-ttu-id="82929-114">Тип проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="82929-114">The resource type to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82929-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82929-115">CommonParameters</span></span>
<span data-ttu-id="82929-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82929-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82929-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82929-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82929-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82929-118">INPUTS</span></span>

## <span data-ttu-id="82929-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82929-119">OUTPUTS</span></span>

### <span data-ttu-id="82929-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="82929-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="82929-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="82929-121">NOTES</span></span>

## <span data-ttu-id="82929-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82929-122">RELATED LINKS</span></span>

