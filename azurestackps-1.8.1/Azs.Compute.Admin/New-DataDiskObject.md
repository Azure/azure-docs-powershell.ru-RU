---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908905"
---
# <span data-ttu-id="09c32-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="09c32-101">New-DataDiskObject</span></span>

## <span data-ttu-id="09c32-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09c32-102">SYNOPSIS</span></span>
<span data-ttu-id="09c32-103">Создание диска данных, который используется для создания нового образа платформы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09c32-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="09c32-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09c32-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="09c32-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09c32-105">DESCRIPTION</span></span>
<span data-ttu-id="09c32-106">Создает объект, хранящий информацию о диске с данными.</span><span class="sxs-lookup"><span data-stu-id="09c32-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="09c32-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09c32-107">EXAMPLES</span></span>

### <span data-ttu-id="09c32-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="09c32-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="09c32-109">Создайте новый объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="09c32-109">Create a new data disk object.</span></span>

## <span data-ttu-id="09c32-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09c32-110">PARAMETERS</span></span>

### <span data-ttu-id="09c32-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="09c32-111">-Lun</span></span>
<span data-ttu-id="09c32-112">Логический номер устройства.</span><span class="sxs-lookup"><span data-stu-id="09c32-112">Logical unit number.</span></span>

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

### <span data-ttu-id="09c32-113">-URI</span><span class="sxs-lookup"><span data-stu-id="09c32-113">-Uri</span></span>
<span data-ttu-id="09c32-114">Расположение шаблона диска.</span><span class="sxs-lookup"><span data-stu-id="09c32-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="09c32-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c32-115">CommonParameters</span></span>
<span data-ttu-id="09c32-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09c32-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c32-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c32-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c32-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09c32-118">INPUTS</span></span>

## <span data-ttu-id="09c32-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09c32-119">OUTPUTS</span></span>

## <span data-ttu-id="09c32-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="09c32-120">NOTES</span></span>

## <span data-ttu-id="09c32-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09c32-121">RELATED LINKS</span></span>

