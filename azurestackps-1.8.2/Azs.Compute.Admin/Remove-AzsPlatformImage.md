---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076783"
---
# <span data-ttu-id="eac18-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="eac18-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="eac18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eac18-102">SYNOPSIS</span></span>
<span data-ttu-id="eac18-103">Удаление образа виртуальной машины из репозитория образов платформы.</span><span class="sxs-lookup"><span data-stu-id="eac18-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="eac18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eac18-104">SYNTAX</span></span>

### <span data-ttu-id="eac18-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eac18-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac18-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eac18-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac18-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac18-107">DESCRIPTION</span></span>
<span data-ttu-id="eac18-108">Удаление образа платформы</span><span class="sxs-lookup"><span data-stu-id="eac18-108">Delete a platform image</span></span>

## <span data-ttu-id="eac18-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eac18-109">EXAMPLES</span></span>

### <span data-ttu-id="eac18-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eac18-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="eac18-111">Удаление существующего образа платформы.</span><span class="sxs-lookup"><span data-stu-id="eac18-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="eac18-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eac18-112">PARAMETERS</span></span>

### <span data-ttu-id="eac18-113">-Force</span><span class="sxs-lookup"><span data-stu-id="eac18-113">-Force</span></span>
<span data-ttu-id="eac18-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="eac18-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eac18-115">-Location</span><span class="sxs-lookup"><span data-stu-id="eac18-115">-Location</span></span>
<span data-ttu-id="eac18-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="eac18-116">Location of the resource.</span></span>

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

### <span data-ttu-id="eac18-117">-Предложение</span><span class="sxs-lookup"><span data-stu-id="eac18-117">-Offer</span></span>
<span data-ttu-id="eac18-118">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="eac18-118">Name of the offer.</span></span>

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

### <span data-ttu-id="eac18-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="eac18-119">-Publisher</span></span>
<span data-ttu-id="eac18-120">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="eac18-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="eac18-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eac18-121">-ResourceId</span></span>
<span data-ttu-id="eac18-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="eac18-122">The resource id.</span></span>

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

### <span data-ttu-id="eac18-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="eac18-123">-Sku</span></span>
<span data-ttu-id="eac18-124">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="eac18-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="eac18-125">-Version</span><span class="sxs-lookup"><span data-stu-id="eac18-125">-Version</span></span>
<span data-ttu-id="eac18-126">Версия образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="eac18-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="eac18-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eac18-127">-Confirm</span></span>
<span data-ttu-id="eac18-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eac18-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac18-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac18-129">-WhatIf</span></span>
<span data-ttu-id="eac18-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eac18-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac18-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eac18-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac18-132">CommonParameters</span></span>
<span data-ttu-id="eac18-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eac18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac18-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eac18-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac18-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eac18-135">INPUTS</span></span>

## <span data-ttu-id="eac18-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac18-136">OUTPUTS</span></span>

## <span data-ttu-id="eac18-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="eac18-137">NOTES</span></span>

## <span data-ttu-id="eac18-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eac18-138">RELATED LINKS</span></span>

