---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b7cc2211df4fd8b9d65c3e93483a485a10ae32
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2020
ms.locfileid: "94077325"
---
# <span data-ttu-id="21047-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="21047-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="21047-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21047-102">SYNOPSIS</span></span>
<span data-ttu-id="21047-103">Возвращает список продуктов, скачанных из Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="21047-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="21047-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21047-104">SYNTAX</span></span>

### <span data-ttu-id="21047-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21047-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="21047-106">Получить</span><span class="sxs-lookup"><span data-stu-id="21047-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="21047-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="21047-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="21047-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21047-108">DESCRIPTION</span></span>
<span data-ttu-id="21047-109">Возвращает список продуктов, скачанных из Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="21047-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="21047-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21047-110">EXAMPLES</span></span>

### <span data-ttu-id="21047-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="21047-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="21047-112">Получение списка загруженных продуктов для моста Azure</span><span class="sxs-lookup"><span data-stu-id="21047-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="21047-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="21047-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="21047-114">Получение продукта Azure Bridge загружено по имени</span><span class="sxs-lookup"><span data-stu-id="21047-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="21047-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21047-115">PARAMETERS</span></span>

### <span data-ttu-id="21047-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="21047-116">-ActivationName</span></span>
<span data-ttu-id="21047-117">Имя активации.</span><span class="sxs-lookup"><span data-stu-id="21047-117">Name of the activation.</span></span>

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

### <span data-ttu-id="21047-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21047-118">-Name</span></span>
<span data-ttu-id="21047-119">Название продукта.</span><span class="sxs-lookup"><span data-stu-id="21047-119">Name of the product.</span></span>

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

### <span data-ttu-id="21047-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21047-120">-ResourceGroupName</span></span>
<span data-ttu-id="21047-121">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="21047-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="21047-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21047-122">-ResourceId</span></span>
<span data-ttu-id="21047-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="21047-123">The resource id.</span></span>

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

### <span data-ttu-id="21047-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="21047-124">-Skip</span></span>
<span data-ttu-id="21047-125">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="21047-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="21047-126">-Top</span><span class="sxs-lookup"><span data-stu-id="21047-126">-Top</span></span>
<span data-ttu-id="21047-127">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="21047-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="21047-128">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="21047-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="21047-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21047-129">CommonParameters</span></span>
<span data-ttu-id="21047-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21047-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21047-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21047-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21047-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21047-132">INPUTS</span></span>

## <span data-ttu-id="21047-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21047-133">OUTPUTS</span></span>

### <span data-ttu-id="21047-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="21047-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="21047-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="21047-135">NOTES</span></span>

## <span data-ttu-id="21047-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21047-136">RELATED LINKS</span></span>

