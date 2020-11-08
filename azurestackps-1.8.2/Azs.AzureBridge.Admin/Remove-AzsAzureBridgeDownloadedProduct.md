---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc5311b1c26d4ae0cb9c1a7ce6ad58a818b53c6
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2020
ms.locfileid: "94245131"
---
# <span data-ttu-id="7125e-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="7125e-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="7125e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7125e-102">SYNOPSIS</span></span>
<span data-ttu-id="7125e-103">Удаление продукта, скачанного из Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="7125e-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="7125e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7125e-104">SYNTAX</span></span>

### <span data-ttu-id="7125e-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7125e-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7125e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7125e-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7125e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7125e-107">DESCRIPTION</span></span>
<span data-ttu-id="7125e-108">Удаление продукта, скачанного из Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="7125e-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="7125e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7125e-109">EXAMPLES</span></span>

### <span data-ttu-id="7125e-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="7125e-110">EXAMPLE 1</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="7125e-111">Удаление продукта, скачанного из Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="7125e-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="7125e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7125e-112">PARAMETERS</span></span>

### <span data-ttu-id="7125e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7125e-113">-Name</span></span>
<span data-ttu-id="7125e-114">Название продукта.</span><span class="sxs-lookup"><span data-stu-id="7125e-114">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125e-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="7125e-115">-ActivationName</span></span>
<span data-ttu-id="7125e-116">Имя активации.</span><span class="sxs-lookup"><span data-stu-id="7125e-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7125e-117">-ResourceGroupName</span></span>
<span data-ttu-id="7125e-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="7125e-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7125e-119">-Force</span></span>
<span data-ttu-id="7125e-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7125e-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7125e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7125e-121">-ResourceId</span></span>
<span data-ttu-id="7125e-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="7125e-122">The resource id.</span></span>

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

### <span data-ttu-id="7125e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7125e-123">-AsJob</span></span>
<span data-ttu-id="7125e-124">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="7125e-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7125e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7125e-125">-WhatIf</span></span>
<span data-ttu-id="7125e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7125e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7125e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7125e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7125e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7125e-128">-Confirm</span></span>
<span data-ttu-id="7125e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7125e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7125e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7125e-130">CommonParameters</span></span>
<span data-ttu-id="7125e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7125e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7125e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7125e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7125e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7125e-133">INPUTS</span></span>

## <span data-ttu-id="7125e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7125e-134">OUTPUTS</span></span>

### <span data-ttu-id="7125e-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="7125e-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="7125e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7125e-136">NOTES</span></span>

## <span data-ttu-id="7125e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7125e-137">RELATED LINKS</span></span>
