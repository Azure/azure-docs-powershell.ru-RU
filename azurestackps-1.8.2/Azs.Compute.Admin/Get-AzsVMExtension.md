---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7eac7b9d23914aa909a111958d64cc9d4247d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076631"
---
# <span data-ttu-id="b8f51-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="b8f51-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="b8f51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8f51-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f51-103">Возвращает доступ к расширениям изображений виртуальной машины в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="b8f51-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="b8f51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8f51-104">SYNTAX</span></span>

### <span data-ttu-id="b8f51-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8f51-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8f51-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b8f51-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8f51-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8f51-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b8f51-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8f51-108">DESCRIPTION</span></span>
<span data-ttu-id="b8f51-109">Возвращает расширения образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b8f51-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="b8f51-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8f51-110">EXAMPLES</span></span>

### <span data-ttu-id="b8f51-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8f51-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="b8f51-112">Получение всех расширений ВМ на указанном месте.</span><span class="sxs-lookup"><span data-stu-id="b8f51-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="b8f51-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8f51-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="b8f51-114">Получить определенное расширение ВМ.</span><span class="sxs-lookup"><span data-stu-id="b8f51-114">Get specific VM extension.</span></span>

## <span data-ttu-id="b8f51-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8f51-115">PARAMETERS</span></span>

### <span data-ttu-id="b8f51-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b8f51-116">-Location</span></span>
<span data-ttu-id="b8f51-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8f51-117">Location of the resource.</span></span>

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

### <span data-ttu-id="b8f51-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b8f51-118">-Publisher</span></span>
<span data-ttu-id="b8f51-119">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="b8f51-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="b8f51-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8f51-120">-ResourceId</span></span>
<span data-ttu-id="b8f51-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8f51-121">The resource id.</span></span>

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

### <span data-ttu-id="b8f51-122">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="b8f51-122">-Type</span></span>
<span data-ttu-id="b8f51-123">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="b8f51-123">Type of extension.</span></span>

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

### <span data-ttu-id="b8f51-124">-Version</span><span class="sxs-lookup"><span data-stu-id="b8f51-124">-Version</span></span>
<span data-ttu-id="b8f51-125">Версия расширения образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b8f51-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="b8f51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f51-126">CommonParameters</span></span>
<span data-ttu-id="b8f51-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8f51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f51-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f51-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f51-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8f51-129">INPUTS</span></span>

## <span data-ttu-id="b8f51-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8f51-130">OUTPUTS</span></span>

### <span data-ttu-id="b8f51-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="b8f51-131">VmExtensionObject</span></span>

## <span data-ttu-id="b8f51-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8f51-132">NOTES</span></span>

## <span data-ttu-id="b8f51-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8f51-133">RELATED LINKS</span></span>

