---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dbd8de47397e86f2aed9f774b555a587cf69976a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555728"
---
# <span data-ttu-id="f27e3-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="f27e3-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="f27e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f27e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f27e3-103">Возвращает состояние задания сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="f27e3-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="f27e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f27e3-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f27e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f27e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f27e3-106">Возвращает состояние задания сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="f27e3-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="f27e3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f27e3-107">EXAMPLES</span></span>

### <span data-ttu-id="f27e3-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f27e3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="f27e3-109">Возвращают сведения о состоянии сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="f27e3-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="f27e3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f27e3-110">PARAMETERS</span></span>

### <span data-ttu-id="f27e3-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="f27e3-111">-FarmName</span></span>
<span data-ttu-id="f27e3-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="f27e3-112">Farm Id.</span></span>

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

### <span data-ttu-id="f27e3-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="f27e3-113">-JobId</span></span>
<span data-ttu-id="f27e3-114">Код операции.</span><span class="sxs-lookup"><span data-stu-id="f27e3-114">Operation Id.</span></span>

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

### <span data-ttu-id="f27e3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f27e3-115">-ResourceGroupName</span></span>
<span data-ttu-id="f27e3-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f27e3-116">Resource group name.</span></span>

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

### <span data-ttu-id="f27e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27e3-117">CommonParameters</span></span>
<span data-ttu-id="f27e3-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f27e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27e3-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f27e3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27e3-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f27e3-120">INPUTS</span></span>

## <span data-ttu-id="f27e3-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f27e3-121">OUTPUTS</span></span>

## <span data-ttu-id="f27e3-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="f27e3-122">NOTES</span></span>

## <span data-ttu-id="f27e3-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f27e3-123">RELATED LINKS</span></span>

