---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ebe9c71560f18ba9e4d7fb52514a4f5b7007bfb
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2020
ms.locfileid: "93570536"
---
# <span data-ttu-id="711bc-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="711bc-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="711bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="711bc-102">SYNOPSIS</span></span>
<span data-ttu-id="711bc-103">Загружает продукт из Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="711bc-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="711bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="711bc-104">SYNTAX</span></span>

### <span data-ttu-id="711bc-105">Products_Download (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="711bc-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="711bc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="711bc-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="711bc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="711bc-107">DESCRIPTION</span></span>
<span data-ttu-id="711bc-108">Загружает продукт из Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="711bc-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="711bc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="711bc-109">EXAMPLES</span></span>

### <span data-ttu-id="711bc-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="711bc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="711bc-111">Скачайте продукт из Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="711bc-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="711bc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="711bc-112">PARAMETERS</span></span>

### <span data-ttu-id="711bc-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="711bc-113">-ActivationName</span></span>
<span data-ttu-id="711bc-114">Имя активации.</span><span class="sxs-lookup"><span data-stu-id="711bc-114">Name of the activation.</span></span>

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

### <span data-ttu-id="711bc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="711bc-115">-AsJob</span></span>
<span data-ttu-id="711bc-116">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="711bc-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="711bc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="711bc-117">-Force</span></span>
<span data-ttu-id="711bc-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="711bc-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="711bc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="711bc-119">-Name</span></span>
<span data-ttu-id="711bc-120">Название продукта.</span><span class="sxs-lookup"><span data-stu-id="711bc-120">Name of the product.</span></span>

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

### <span data-ttu-id="711bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="711bc-122">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="711bc-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="711bc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="711bc-123">-ResourceId</span></span>
<span data-ttu-id="711bc-124">Идентификатор ресурса для продукта моста Azure.</span><span class="sxs-lookup"><span data-stu-id="711bc-124">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="711bc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="711bc-125">-Confirm</span></span>
<span data-ttu-id="711bc-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="711bc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="711bc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="711bc-127">-WhatIf</span></span>
<span data-ttu-id="711bc-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="711bc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="711bc-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="711bc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="711bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711bc-130">CommonParameters</span></span>
<span data-ttu-id="711bc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="711bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711bc-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="711bc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711bc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="711bc-133">INPUTS</span></span>

## <span data-ttu-id="711bc-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="711bc-134">OUTPUTS</span></span>

## <span data-ttu-id="711bc-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="711bc-135">NOTES</span></span>

## <span data-ttu-id="711bc-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="711bc-136">RELATED LINKS</span></span>

