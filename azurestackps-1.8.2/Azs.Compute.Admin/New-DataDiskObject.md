---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076787"
---
# <span data-ttu-id="01cfc-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="01cfc-101">New-DataDiskObject</span></span>

## <span data-ttu-id="01cfc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="01cfc-103">Создание диска данных, который используется для создания нового образа платформы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="01cfc-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="01cfc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01cfc-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="01cfc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01cfc-105">DESCRIPTION</span></span>
<span data-ttu-id="01cfc-106">Создает объект, хранящий информацию о диске с данными.</span><span class="sxs-lookup"><span data-stu-id="01cfc-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="01cfc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01cfc-107">EXAMPLES</span></span>

### <span data-ttu-id="01cfc-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="01cfc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="01cfc-109">Создайте новый объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="01cfc-109">Create a new data disk object.</span></span>

## <span data-ttu-id="01cfc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01cfc-110">PARAMETERS</span></span>

### <span data-ttu-id="01cfc-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="01cfc-111">-Lun</span></span>
<span data-ttu-id="01cfc-112">Логический номер устройства.</span><span class="sxs-lookup"><span data-stu-id="01cfc-112">Logical unit number.</span></span>

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

### <span data-ttu-id="01cfc-113">-URI</span><span class="sxs-lookup"><span data-stu-id="01cfc-113">-Uri</span></span>
<span data-ttu-id="01cfc-114">Расположение шаблона диска.</span><span class="sxs-lookup"><span data-stu-id="01cfc-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="01cfc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01cfc-115">CommonParameters</span></span>
<span data-ttu-id="01cfc-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01cfc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01cfc-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01cfc-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01cfc-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01cfc-118">INPUTS</span></span>

## <span data-ttu-id="01cfc-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01cfc-119">OUTPUTS</span></span>

## <span data-ttu-id="01cfc-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="01cfc-120">NOTES</span></span>

## <span data-ttu-id="01cfc-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01cfc-121">RELATED LINKS</span></span>

