---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edcc9bea35e1675b42a04c2b4e804c48ba052742
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2020
ms.locfileid: "94077321"
---
# <span data-ttu-id="6cdd5-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="6cdd5-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="6cdd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cdd5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdd5-103">Возвращает список продуктов, доступных для скачивания из Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="6cdd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cdd5-104">SYNTAX</span></span>

### <span data-ttu-id="6cdd5-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6cdd5-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cdd5-106">Получить</span><span class="sxs-lookup"><span data-stu-id="6cdd5-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="6cdd5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cdd5-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6cdd5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cdd5-108">DESCRIPTION</span></span>
<span data-ttu-id="6cdd5-109">Возвращает список продуктов, доступных для скачивания из Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="6cdd5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cdd5-110">EXAMPLES</span></span>

### <span data-ttu-id="6cdd5-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6cdd5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="6cdd5-112">Получите список продуктов, доступных для скачивания из Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="6cdd5-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6cdd5-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="6cdd5-114">Получите сведения о продукте, доступные для скачивания из Azure Marketplace по имени.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="6cdd5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cdd5-115">PARAMETERS</span></span>

### <span data-ttu-id="6cdd5-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="6cdd5-116">-ActivationName</span></span>
<span data-ttu-id="6cdd5-117">Имя активации.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cdd5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6cdd5-118">-Name</span></span>
<span data-ttu-id="6cdd5-119">Название продукта.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-119">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cdd5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cdd5-120">-ResourceGroupName</span></span>
<span data-ttu-id="6cdd5-121">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-121">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cdd5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cdd5-122">-ResourceId</span></span>
<span data-ttu-id="6cdd5-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-123">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cdd5-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="6cdd5-124">-Skip</span></span>
<span data-ttu-id="6cdd5-125">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-125">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cdd5-126">-Top</span><span class="sxs-lookup"><span data-stu-id="6cdd5-126">-Top</span></span>
<span data-ttu-id="6cdd5-127">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6cdd5-128">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cdd5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdd5-129">CommonParameters</span></span>
<span data-ttu-id="6cdd5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cdd5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdd5-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cdd5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdd5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cdd5-132">INPUTS</span></span>

## <span data-ttu-id="6cdd5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cdd5-133">OUTPUTS</span></span>

### <span data-ttu-id="6cdd5-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="6cdd5-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="6cdd5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cdd5-135">NOTES</span></span>

## <span data-ttu-id="6cdd5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cdd5-136">RELATED LINKS</span></span>
