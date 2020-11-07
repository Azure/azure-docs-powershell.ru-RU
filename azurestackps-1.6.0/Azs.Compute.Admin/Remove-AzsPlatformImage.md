---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 947bb6b453d92897f7901a00ed5a43efa4ac640e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731687"
---
# <span data-ttu-id="9d703-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="9d703-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="9d703-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d703-102">SYNOPSIS</span></span>
<span data-ttu-id="9d703-103">Удаление образа виртуальной машины из репозитория образов платформы.</span><span class="sxs-lookup"><span data-stu-id="9d703-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="9d703-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d703-104">SYNTAX</span></span>

### <span data-ttu-id="9d703-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d703-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d703-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d703-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d703-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d703-107">DESCRIPTION</span></span>
<span data-ttu-id="9d703-108">Удаление образа платформы</span><span class="sxs-lookup"><span data-stu-id="9d703-108">Delete a platform image</span></span>

## <span data-ttu-id="9d703-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d703-109">EXAMPLES</span></span>

### <span data-ttu-id="9d703-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d703-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="9d703-111">Удаление существующего образа платформы.</span><span class="sxs-lookup"><span data-stu-id="9d703-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="9d703-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d703-112">PARAMETERS</span></span>

### <span data-ttu-id="9d703-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9d703-113">-Force</span></span>
<span data-ttu-id="9d703-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9d703-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9d703-115">-Location</span><span class="sxs-lookup"><span data-stu-id="9d703-115">-Location</span></span>
<span data-ttu-id="9d703-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9d703-116">Location of the resource.</span></span>

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

### <span data-ttu-id="9d703-117">-Предложение</span><span class="sxs-lookup"><span data-stu-id="9d703-117">-Offer</span></span>
<span data-ttu-id="9d703-118">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="9d703-118">Name of the offer.</span></span>

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

### <span data-ttu-id="9d703-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9d703-119">-Publisher</span></span>
<span data-ttu-id="9d703-120">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="9d703-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="9d703-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d703-121">-ResourceId</span></span>
<span data-ttu-id="9d703-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9d703-122">The resource id.</span></span>

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

### <span data-ttu-id="9d703-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="9d703-123">-Sku</span></span>
<span data-ttu-id="9d703-124">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="9d703-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="9d703-125">-Version</span><span class="sxs-lookup"><span data-stu-id="9d703-125">-Version</span></span>
<span data-ttu-id="9d703-126">Версия образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d703-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="9d703-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d703-127">-Confirm</span></span>
<span data-ttu-id="9d703-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d703-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d703-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d703-129">-WhatIf</span></span>
<span data-ttu-id="9d703-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9d703-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d703-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9d703-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d703-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d703-132">CommonParameters</span></span>
<span data-ttu-id="9d703-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d703-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d703-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d703-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d703-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d703-135">INPUTS</span></span>

## <span data-ttu-id="9d703-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d703-136">OUTPUTS</span></span>

## <span data-ttu-id="9d703-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d703-137">NOTES</span></span>

## <span data-ttu-id="9d703-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d703-138">RELATED LINKS</span></span>

