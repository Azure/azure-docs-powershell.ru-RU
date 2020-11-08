---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d39721f1a9ed243242bd08053f9a22f0ed53df30
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076601"
---
# <span data-ttu-id="d7aca-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d7aca-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="d7aca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7aca-102">SYNOPSIS</span></span>
<span data-ttu-id="d7aca-103">Добавление образа платформы виртуальной машины из заданной конфигурации образа.</span><span class="sxs-lookup"><span data-stu-id="d7aca-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="d7aca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7aca-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7aca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7aca-105">DESCRIPTION</span></span>
<span data-ttu-id="d7aca-106">Добавьте изображение платформы.</span><span class="sxs-lookup"><span data-stu-id="d7aca-106">Add a platform image.</span></span>

## <span data-ttu-id="d7aca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7aca-107">EXAMPLES</span></span>

### <span data-ttu-id="d7aca-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d7aca-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="d7aca-109">Добавьте новый образ платформы.</span><span class="sxs-lookup"><span data-stu-id="d7aca-109">Add a new platform image.</span></span>

## <span data-ttu-id="d7aca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7aca-110">PARAMETERS</span></span>

### <span data-ttu-id="d7aca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7aca-111">-AsJob</span></span>
<span data-ttu-id="d7aca-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="d7aca-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d7aca-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="d7aca-113">-BillingPartNumber</span></span>
<span data-ttu-id="d7aca-114">Номер детали используется для выставления счетов за программные расходы.</span><span class="sxs-lookup"><span data-stu-id="d7aca-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-115">-Диски</span><span class="sxs-lookup"><span data-stu-id="d7aca-115">-DataDisks</span></span>
<span data-ttu-id="d7aca-116">Диски данных, используемые образом платформы.</span><span class="sxs-lookup"><span data-stu-id="d7aca-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d7aca-117">-Force</span></span>
<span data-ttu-id="d7aca-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d7aca-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d7aca-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d7aca-119">-Location</span></span>
<span data-ttu-id="d7aca-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d7aca-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-121">-Предложение</span><span class="sxs-lookup"><span data-stu-id="d7aca-121">-Offer</span></span>
<span data-ttu-id="d7aca-122">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="d7aca-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="d7aca-123">-OsType</span></span>
<span data-ttu-id="d7aca-124">Тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d7aca-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="d7aca-125">-OsUri</span></span>
<span data-ttu-id="d7aca-126">Расположение диска.</span><span class="sxs-lookup"><span data-stu-id="d7aca-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d7aca-127">-Publisher</span></span>
<span data-ttu-id="d7aca-128">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="d7aca-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="d7aca-129">-Sku</span></span>
<span data-ttu-id="d7aca-130">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="d7aca-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-131">-Version</span><span class="sxs-lookup"><span data-stu-id="d7aca-131">-Version</span></span>
<span data-ttu-id="d7aca-132">Версия образа платформы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d7aca-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7aca-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7aca-133">-Confirm</span></span>
<span data-ttu-id="d7aca-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7aca-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7aca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7aca-135">-WhatIf</span></span>
<span data-ttu-id="d7aca-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7aca-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7aca-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7aca-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7aca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7aca-138">CommonParameters</span></span>
<span data-ttu-id="d7aca-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7aca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7aca-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7aca-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7aca-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7aca-141">INPUTS</span></span>

## <span data-ttu-id="d7aca-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7aca-142">OUTPUTS</span></span>

### <span data-ttu-id="d7aca-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="d7aca-143">PlatformImageObject</span></span>

## <span data-ttu-id="d7aca-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7aca-144">NOTES</span></span>

## <span data-ttu-id="d7aca-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7aca-145">RELATED LINKS</span></span>

