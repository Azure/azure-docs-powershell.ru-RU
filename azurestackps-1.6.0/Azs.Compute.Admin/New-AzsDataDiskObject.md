---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555212"
---
# <span data-ttu-id="a07eb-101">New-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="a07eb-101">New-AzsDataDiskObject</span></span>

## <span data-ttu-id="a07eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a07eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a07eb-103">Создание диска данных, который используется для создания нового образа платформы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a07eb-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="a07eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a07eb-104">SYNTAX</span></span>

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a07eb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a07eb-105">DESCRIPTION</span></span>
<span data-ttu-id="a07eb-106">Создает объект, хранящий информацию о диске с данными.</span><span class="sxs-lookup"><span data-stu-id="a07eb-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="a07eb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a07eb-107">EXAMPLES</span></span>

### <span data-ttu-id="a07eb-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a07eb-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="a07eb-109">Создайте новый объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="a07eb-109">Create a new data disk object.</span></span>

## <span data-ttu-id="a07eb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a07eb-110">PARAMETERS</span></span>

### <span data-ttu-id="a07eb-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="a07eb-111">-Lun</span></span>
<span data-ttu-id="a07eb-112">Логический номер устройства.</span><span class="sxs-lookup"><span data-stu-id="a07eb-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07eb-113">-URI</span><span class="sxs-lookup"><span data-stu-id="a07eb-113">-Uri</span></span>
<span data-ttu-id="a07eb-114">Расположение шаблона диска.</span><span class="sxs-lookup"><span data-stu-id="a07eb-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="a07eb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07eb-115">CommonParameters</span></span>
<span data-ttu-id="a07eb-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a07eb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07eb-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a07eb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07eb-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a07eb-118">INPUTS</span></span>

## <span data-ttu-id="a07eb-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a07eb-119">OUTPUTS</span></span>

## <span data-ttu-id="a07eb-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="a07eb-120">NOTES</span></span>

## <span data-ttu-id="a07eb-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a07eb-121">RELATED LINKS</span></span>

