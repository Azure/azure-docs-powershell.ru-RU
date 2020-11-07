---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ec1f3e70752a5386cd5dad78d867da68091b96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906761"
---
# <span data-ttu-id="2d885-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="2d885-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="2d885-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d885-102">SYNOPSIS</span></span>
<span data-ttu-id="2d885-103">Добавление образа платформы виртуальной машины из заданной конфигурации образа.</span><span class="sxs-lookup"><span data-stu-id="2d885-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="2d885-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d885-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d885-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d885-105">DESCRIPTION</span></span>
<span data-ttu-id="2d885-106">Добавьте изображение платформы.</span><span class="sxs-lookup"><span data-stu-id="2d885-106">Add a platform image.</span></span>

## <span data-ttu-id="2d885-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d885-107">EXAMPLES</span></span>

### <span data-ttu-id="2d885-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d885-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="2d885-109">Добавьте новый образ платформы.</span><span class="sxs-lookup"><span data-stu-id="2d885-109">Add a new platform image.</span></span>

## <span data-ttu-id="2d885-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d885-110">PARAMETERS</span></span>

### <span data-ttu-id="2d885-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d885-111">-AsJob</span></span>
<span data-ttu-id="2d885-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="2d885-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2d885-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="2d885-113">-BillingPartNumber</span></span>
<span data-ttu-id="2d885-114">Номер детали используется для выставления счетов за программные расходы.</span><span class="sxs-lookup"><span data-stu-id="2d885-114">The part number is used to bill for software costs.</span></span>

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

### <span data-ttu-id="2d885-115">-Диски</span><span class="sxs-lookup"><span data-stu-id="2d885-115">-DataDisks</span></span>
<span data-ttu-id="2d885-116">Диски данных, используемые образом платформы.</span><span class="sxs-lookup"><span data-stu-id="2d885-116">Data disks used by the platform image.</span></span>

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

### <span data-ttu-id="2d885-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d885-117">-Force</span></span>
<span data-ttu-id="2d885-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2d885-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2d885-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2d885-119">-Location</span></span>
<span data-ttu-id="2d885-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d885-120">Location of the resource.</span></span>

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

### <span data-ttu-id="2d885-121">-Предложение</span><span class="sxs-lookup"><span data-stu-id="2d885-121">-Offer</span></span>
<span data-ttu-id="2d885-122">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="2d885-122">Name of the offer.</span></span>

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

### <span data-ttu-id="2d885-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="2d885-123">-OsType</span></span>
<span data-ttu-id="2d885-124">Тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2d885-124">Operating system type.</span></span>

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

### <span data-ttu-id="2d885-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="2d885-125">-OsUri</span></span>
<span data-ttu-id="2d885-126">Расположение диска.</span><span class="sxs-lookup"><span data-stu-id="2d885-126">Location of the disk.</span></span>

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

### <span data-ttu-id="2d885-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2d885-127">-Publisher</span></span>
<span data-ttu-id="2d885-128">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="2d885-128">Name of the publisher.</span></span>

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

### <span data-ttu-id="2d885-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="2d885-129">-Sku</span></span>
<span data-ttu-id="2d885-130">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="2d885-130">Name of the SKU.</span></span>

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

### <span data-ttu-id="2d885-131">-Version</span><span class="sxs-lookup"><span data-stu-id="2d885-131">-Version</span></span>
<span data-ttu-id="2d885-132">Версия образа платформы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d885-132">The version of the virtual machine platform image.</span></span>

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

### <span data-ttu-id="2d885-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d885-133">-Confirm</span></span>
<span data-ttu-id="2d885-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d885-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d885-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d885-135">-WhatIf</span></span>
<span data-ttu-id="2d885-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d885-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d885-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d885-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d885-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d885-138">CommonParameters</span></span>
<span data-ttu-id="2d885-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d885-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d885-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d885-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d885-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d885-141">INPUTS</span></span>

## <span data-ttu-id="2d885-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d885-142">OUTPUTS</span></span>

### <span data-ttu-id="2d885-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="2d885-143">PlatformImageObject</span></span>

## <span data-ttu-id="2d885-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d885-144">NOTES</span></span>

## <span data-ttu-id="2d885-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d885-145">RELATED LINKS</span></span>

