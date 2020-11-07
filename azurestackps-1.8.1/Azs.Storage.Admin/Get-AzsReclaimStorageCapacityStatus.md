---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd62756b3a41af82a245a39d4f80478d47d90e1c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909033"
---
# <span data-ttu-id="a7291-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="a7291-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="a7291-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7291-102">SYNOPSIS</span></span>
<span data-ttu-id="a7291-103">Возвращает состояние задания сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="a7291-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="a7291-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7291-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7291-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7291-105">DESCRIPTION</span></span>
<span data-ttu-id="a7291-106">Возвращает состояние задания сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="a7291-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="a7291-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7291-107">EXAMPLES</span></span>

### <span data-ttu-id="a7291-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="a7291-108">EXAMPLE 1</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="a7291-109">Возвращают сведения о состоянии сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="a7291-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="a7291-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7291-110">PARAMETERS</span></span>

### <span data-ttu-id="a7291-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="a7291-111">-FarmName</span></span>
<span data-ttu-id="a7291-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="a7291-112">Farm Id.</span></span>

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

### <span data-ttu-id="a7291-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="a7291-113">-JobId</span></span>
<span data-ttu-id="a7291-114">Код операции.</span><span class="sxs-lookup"><span data-stu-id="a7291-114">Operation Id.</span></span>

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

### <span data-ttu-id="a7291-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7291-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7291-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7291-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7291-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7291-117">CommonParameters</span></span>
<span data-ttu-id="a7291-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7291-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7291-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7291-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7291-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7291-120">INPUTS</span></span>

## <span data-ttu-id="a7291-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7291-121">OUTPUTS</span></span>

## <span data-ttu-id="a7291-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7291-122">NOTES</span></span>

## <span data-ttu-id="a7291-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7291-123">RELATED LINKS</span></span>
