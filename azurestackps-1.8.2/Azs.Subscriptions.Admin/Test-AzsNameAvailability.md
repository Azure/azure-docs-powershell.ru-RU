---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076712"
---
# <span data-ttu-id="24c5f-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="24c5f-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="24c5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="24c5f-103">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="24c5f-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="24c5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24c5f-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="24c5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="24c5f-106">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="24c5f-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="24c5f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24c5f-107">EXAMPLES</span></span>

### <span data-ttu-id="24c5f-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24c5f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="24c5f-109">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="24c5f-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="24c5f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24c5f-110">PARAMETERS</span></span>

### <span data-ttu-id="24c5f-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24c5f-111">-Name</span></span>
<span data-ttu-id="24c5f-112">Имя проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="24c5f-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="24c5f-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="24c5f-113">-ResourceType</span></span>
<span data-ttu-id="24c5f-114">Тип проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="24c5f-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="24c5f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c5f-115">CommonParameters</span></span>
<span data-ttu-id="24c5f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24c5f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c5f-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c5f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c5f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24c5f-118">INPUTS</span></span>

## <span data-ttu-id="24c5f-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24c5f-119">OUTPUTS</span></span>

### <span data-ttu-id="24c5f-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="24c5f-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="24c5f-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="24c5f-121">NOTES</span></span>

## <span data-ttu-id="24c5f-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24c5f-122">RELATED LINKS</span></span>

