---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909178"
---
# <span data-ttu-id="ae549-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ae549-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="ae549-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae549-102">SYNOPSIS</span></span>
<span data-ttu-id="ae549-103">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="ae549-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="ae549-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae549-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="ae549-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae549-105">DESCRIPTION</span></span>
<span data-ttu-id="ae549-106">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="ae549-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="ae549-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae549-107">EXAMPLES</span></span>

### <span data-ttu-id="ae549-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ae549-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="ae549-109">Возвращает avaialbility указанного типа ресурса подписок и его имя.</span><span class="sxs-lookup"><span data-stu-id="ae549-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="ae549-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae549-110">PARAMETERS</span></span>

### <span data-ttu-id="ae549-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae549-111">-Name</span></span>
<span data-ttu-id="ae549-112">Имя проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae549-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="ae549-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ae549-113">-ResourceType</span></span>
<span data-ttu-id="ae549-114">Тип проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae549-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="ae549-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae549-115">CommonParameters</span></span>
<span data-ttu-id="ae549-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae549-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae549-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae549-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae549-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae549-118">INPUTS</span></span>

## <span data-ttu-id="ae549-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae549-119">OUTPUTS</span></span>

### <span data-ttu-id="ae549-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ae549-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="ae549-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae549-121">NOTES</span></span>

## <span data-ttu-id="ae549-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae549-122">RELATED LINKS</span></span>

