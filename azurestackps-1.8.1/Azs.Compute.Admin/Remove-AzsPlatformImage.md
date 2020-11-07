---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908901"
---
# <span data-ttu-id="ea7e2-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="ea7e2-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="ea7e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7e2-103">Удаление образа виртуальной машины из репозитория образов платформы.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="ea7e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea7e2-104">SYNTAX</span></span>

### <span data-ttu-id="ea7e2-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea7e2-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea7e2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea7e2-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7e2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea7e2-107">DESCRIPTION</span></span>
<span data-ttu-id="ea7e2-108">Удаление образа платформы</span><span class="sxs-lookup"><span data-stu-id="ea7e2-108">Delete a platform image</span></span>

## <span data-ttu-id="ea7e2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea7e2-109">EXAMPLES</span></span>

### <span data-ttu-id="ea7e2-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ea7e2-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="ea7e2-111">Удаление существующего образа платформы.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="ea7e2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea7e2-112">PARAMETERS</span></span>

### <span data-ttu-id="ea7e2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ea7e2-113">-Force</span></span>
<span data-ttu-id="ea7e2-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ea7e2-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ea7e2-115">-Location</span></span>
<span data-ttu-id="ea7e2-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7e2-117">-Предложение</span><span class="sxs-lookup"><span data-stu-id="ea7e2-117">-Offer</span></span>
<span data-ttu-id="ea7e2-118">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-118">Name of the offer.</span></span>

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

### <span data-ttu-id="ea7e2-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ea7e2-119">-Publisher</span></span>
<span data-ttu-id="ea7e2-120">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="ea7e2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea7e2-121">-ResourceId</span></span>
<span data-ttu-id="ea7e2-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-122">The resource id.</span></span>

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

### <span data-ttu-id="ea7e2-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="ea7e2-123">-Sku</span></span>
<span data-ttu-id="ea7e2-124">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="ea7e2-125">-Version</span><span class="sxs-lookup"><span data-stu-id="ea7e2-125">-Version</span></span>
<span data-ttu-id="ea7e2-126">Версия образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="ea7e2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea7e2-127">-Confirm</span></span>
<span data-ttu-id="ea7e2-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7e2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7e2-129">-WhatIf</span></span>
<span data-ttu-id="ea7e2-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7e2-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7e2-132">CommonParameters</span></span>
<span data-ttu-id="ea7e2-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7e2-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7e2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7e2-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea7e2-135">INPUTS</span></span>

## <span data-ttu-id="ea7e2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea7e2-136">OUTPUTS</span></span>

## <span data-ttu-id="ea7e2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea7e2-137">NOTES</span></span>

## <span data-ttu-id="ea7e2-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea7e2-138">RELATED LINKS</span></span>

