---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b3fb659c1d11df734bdc95f554e4c100060e185
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555207"
---
# <span data-ttu-id="3bf86-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="3bf86-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="3bf86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bf86-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf86-103">Удаляет указанную вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="3bf86-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="3bf86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bf86-104">SYNTAX</span></span>

### <span data-ttu-id="3bf86-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3bf86-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bf86-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf86-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bf86-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bf86-107">DESCRIPTION</span></span>
<span data-ttu-id="3bf86-108">Удаление существующей квоты.</span><span class="sxs-lookup"><span data-stu-id="3bf86-108">Delete an existing quota.</span></span>

## <span data-ttu-id="3bf86-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bf86-109">EXAMPLES</span></span>

### <span data-ttu-id="3bf86-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3bf86-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="3bf86-111">Удаление вычислительной квоты с учетом всех параметров.</span><span class="sxs-lookup"><span data-stu-id="3bf86-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="3bf86-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bf86-112">PARAMETERS</span></span>

### <span data-ttu-id="3bf86-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3bf86-113">-Force</span></span>
<span data-ttu-id="3bf86-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3bf86-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3bf86-115">-Location</span><span class="sxs-lookup"><span data-stu-id="3bf86-115">-Location</span></span>
<span data-ttu-id="3bf86-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3bf86-116">Location of the resource.</span></span> <span data-ttu-id="3bf86-117">Если это значение не задано, по умолчанию используется расположение, связанное с подпиской на Tenat.</span><span class="sxs-lookup"><span data-stu-id="3bf86-117">If not given we default to the location bound to the tenat's subscription.</span></span>

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

### <span data-ttu-id="3bf86-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3bf86-118">-Name</span></span>
<span data-ttu-id="3bf86-119">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="3bf86-119">Name of the quota.</span></span>

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

### <span data-ttu-id="3bf86-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf86-120">-ResourceId</span></span>
<span data-ttu-id="3bf86-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3bf86-121">The resource id.</span></span>

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

### <span data-ttu-id="3bf86-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bf86-122">-Confirm</span></span>
<span data-ttu-id="3bf86-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3bf86-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bf86-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bf86-124">-WhatIf</span></span>
<span data-ttu-id="3bf86-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3bf86-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bf86-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3bf86-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bf86-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf86-127">CommonParameters</span></span>
<span data-ttu-id="3bf86-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bf86-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf86-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bf86-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf86-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bf86-130">INPUTS</span></span>

## <span data-ttu-id="3bf86-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bf86-131">OUTPUTS</span></span>

## <span data-ttu-id="3bf86-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bf86-132">NOTES</span></span>

## <span data-ttu-id="3bf86-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bf86-133">RELATED LINKS</span></span>

