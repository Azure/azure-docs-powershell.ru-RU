---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7eac7b9d23914aa909a111958d64cc9d4247d3
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908913"
---
# <span data-ttu-id="c173a-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="c173a-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="c173a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c173a-102">SYNOPSIS</span></span>
<span data-ttu-id="c173a-103">Возвращает доступ к расширениям изображений виртуальной машины в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="c173a-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="c173a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c173a-104">SYNTAX</span></span>

### <span data-ttu-id="c173a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c173a-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="c173a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c173a-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c173a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c173a-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c173a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c173a-108">DESCRIPTION</span></span>
<span data-ttu-id="c173a-109">Возвращает расширения образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c173a-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="c173a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c173a-110">EXAMPLES</span></span>

### <span data-ttu-id="c173a-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c173a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="c173a-112">Получение всех расширений ВМ на указанном месте.</span><span class="sxs-lookup"><span data-stu-id="c173a-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="c173a-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c173a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="c173a-114">Получить определенное расширение ВМ.</span><span class="sxs-lookup"><span data-stu-id="c173a-114">Get specific VM extension.</span></span>

## <span data-ttu-id="c173a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c173a-115">PARAMETERS</span></span>

### <span data-ttu-id="c173a-116">-Location</span><span class="sxs-lookup"><span data-stu-id="c173a-116">-Location</span></span>
<span data-ttu-id="c173a-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c173a-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c173a-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c173a-118">-Publisher</span></span>
<span data-ttu-id="c173a-119">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="c173a-119">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c173a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c173a-120">-ResourceId</span></span>
<span data-ttu-id="c173a-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c173a-121">The resource id.</span></span>

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

### <span data-ttu-id="c173a-122">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="c173a-122">-Type</span></span>
<span data-ttu-id="c173a-123">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="c173a-123">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c173a-124">-Version</span><span class="sxs-lookup"><span data-stu-id="c173a-124">-Version</span></span>
<span data-ttu-id="c173a-125">Версия расширения образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c173a-125">The version of the virtual machine image extension.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c173a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c173a-126">CommonParameters</span></span>
<span data-ttu-id="c173a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c173a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c173a-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c173a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c173a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c173a-129">INPUTS</span></span>

## <span data-ttu-id="c173a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c173a-130">OUTPUTS</span></span>

### <span data-ttu-id="c173a-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="c173a-131">VmExtensionObject</span></span>

## <span data-ttu-id="c173a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c173a-132">NOTES</span></span>

## <span data-ttu-id="c173a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c173a-133">RELATED LINKS</span></span>

