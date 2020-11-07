---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731770"
---
# <span data-ttu-id="bb998-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="bb998-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="bb998-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb998-102">SYNOPSIS</span></span>
<span data-ttu-id="bb998-103">Масштабирование единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="bb998-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="bb998-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb998-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="bb998-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb998-105">DESCRIPTION</span></span>
<span data-ttu-id="bb998-106">Добавьте новый узел шкалы масштабирования в кластер единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="bb998-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="bb998-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb998-107">EXAMPLES</span></span>

### <span data-ttu-id="bb998-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bb998-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="bb998-109">Добавляет список узлов в единицу измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="bb998-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="bb998-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb998-110">PARAMETERS</span></span>

### <span data-ttu-id="bb998-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb998-111">-AsJob</span></span>
<span data-ttu-id="bb998-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="bb998-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bb998-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="bb998-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="bb998-114">Дождитесь завершения репликации хранилища, прежде чем возвращать сообщение об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="bb998-114">Wait for storage replication to complete before returning success.</span></span>

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

### <span data-ttu-id="bb998-115">-Location</span><span class="sxs-lookup"><span data-stu-id="bb998-115">-Location</span></span>
<span data-ttu-id="bb998-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb998-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb998-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="bb998-117">-NodeList</span></span>
<span data-ttu-id="bb998-118">Список входных данных, с помощью которых можно добавить набор узлов единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="bb998-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb998-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb998-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb998-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb998-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb998-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="bb998-121">-ScaleUnit</span></span>
<span data-ttu-id="bb998-122">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="bb998-122">Name of the scale units.</span></span>

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

### <span data-ttu-id="bb998-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb998-123">CommonParameters</span></span>
<span data-ttu-id="bb998-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb998-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb998-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb998-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb998-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb998-126">INPUTS</span></span>

## <span data-ttu-id="bb998-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb998-127">OUTPUTS</span></span>

## <span data-ttu-id="bb998-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb998-128">NOTES</span></span>

## <span data-ttu-id="bb998-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb998-129">RELATED LINKS</span></span>

