---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 107709fa7431e8c37f156f1304f560e42c08ed60
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2020
ms.locfileid: "94245133"
---
# <span data-ttu-id="c754e-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="c754e-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="c754e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c754e-102">SYNOPSIS</span></span>
<span data-ttu-id="c754e-103">Загружает продукт из Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c754e-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="c754e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c754e-104">SYNTAX</span></span>

### <span data-ttu-id="c754e-105">Products_Download (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c754e-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c754e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c754e-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c754e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c754e-107">DESCRIPTION</span></span>
<span data-ttu-id="c754e-108">Загружает продукт из Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c754e-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="c754e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c754e-109">EXAMPLES</span></span>

### <span data-ttu-id="c754e-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="c754e-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="c754e-111">Скачайте продукт из Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="c754e-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="c754e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c754e-112">PARAMETERS</span></span>

### <span data-ttu-id="c754e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c754e-113">-Name</span></span>
<span data-ttu-id="c754e-114">Название продукта</span><span class="sxs-lookup"><span data-stu-id="c754e-114">Name of the product</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c754e-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="c754e-115">-ActivationName</span></span>
<span data-ttu-id="c754e-116">Имя активации.</span><span class="sxs-lookup"><span data-stu-id="c754e-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c754e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c754e-117">-ResourceGroupName</span></span>
<span data-ttu-id="c754e-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="c754e-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c754e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c754e-119">-ResourceId</span></span>
<span data-ttu-id="c754e-120">Идентификатор ресурса для продукта моста Azure.</span><span class="sxs-lookup"><span data-stu-id="c754e-120">Resource identifier for azure bridge product.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c754e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c754e-121">-AsJob</span></span>
<span data-ttu-id="c754e-122">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="c754e-122">Run asynchronous as a job and return the job object.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c754e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c754e-123">-Force</span></span>
<span data-ttu-id="c754e-124">Параметр переключить не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="c754e-124">Switch parameter not to ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c754e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c754e-125">-WhatIf</span></span>
<span data-ttu-id="c754e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c754e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c754e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c754e-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c754e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c754e-128">-Confirm</span></span>
<span data-ttu-id="c754e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c754e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c754e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c754e-130">CommonParameters</span></span>
<span data-ttu-id="c754e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c754e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c754e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c754e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c754e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c754e-133">INPUTS</span></span>

## <span data-ttu-id="c754e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c754e-134">OUTPUTS</span></span>

## <span data-ttu-id="c754e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c754e-135">NOTES</span></span>

## <span data-ttu-id="c754e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c754e-136">RELATED LINKS</span></span>