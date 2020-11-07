---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906745"
---
# <span data-ttu-id="0c81d-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0c81d-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="0c81d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c81d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c81d-103">Возвращает доступ к расширениям изображений виртуальной машины в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="0c81d-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="0c81d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c81d-104">SYNTAX</span></span>

### <span data-ttu-id="0c81d-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c81d-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="0c81d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="0c81d-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c81d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c81d-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0c81d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c81d-108">DESCRIPTION</span></span>
<span data-ttu-id="0c81d-109">Возвращает расширения образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c81d-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="0c81d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c81d-110">EXAMPLES</span></span>

### <span data-ttu-id="0c81d-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c81d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="0c81d-112">Получение всех расширений ВМ на указанном месте.</span><span class="sxs-lookup"><span data-stu-id="0c81d-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="0c81d-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c81d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="0c81d-114">Получить определенное расширение ВМ.</span><span class="sxs-lookup"><span data-stu-id="0c81d-114">Get specific VM extension.</span></span>

## <span data-ttu-id="0c81d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c81d-115">PARAMETERS</span></span>

### <span data-ttu-id="0c81d-116">-Location</span><span class="sxs-lookup"><span data-stu-id="0c81d-116">-Location</span></span>
<span data-ttu-id="0c81d-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c81d-117">Location of the resource.</span></span>

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

### <span data-ttu-id="0c81d-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0c81d-118">-Publisher</span></span>
<span data-ttu-id="0c81d-119">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="0c81d-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="0c81d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c81d-120">-ResourceId</span></span>
<span data-ttu-id="0c81d-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c81d-121">The resource id.</span></span>

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

### <span data-ttu-id="0c81d-122">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="0c81d-122">-Type</span></span>
<span data-ttu-id="0c81d-123">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="0c81d-123">Type of extension.</span></span>

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

### <span data-ttu-id="0c81d-124">-Version</span><span class="sxs-lookup"><span data-stu-id="0c81d-124">-Version</span></span>
<span data-ttu-id="0c81d-125">Версия расширения образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c81d-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="0c81d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c81d-126">CommonParameters</span></span>
<span data-ttu-id="0c81d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c81d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c81d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c81d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c81d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c81d-129">INPUTS</span></span>

## <span data-ttu-id="0c81d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c81d-130">OUTPUTS</span></span>

### <span data-ttu-id="0c81d-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="0c81d-131">VmExtensionObject</span></span>

## <span data-ttu-id="0c81d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c81d-132">NOTES</span></span>

## <span data-ttu-id="0c81d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c81d-133">RELATED LINKS</span></span>

