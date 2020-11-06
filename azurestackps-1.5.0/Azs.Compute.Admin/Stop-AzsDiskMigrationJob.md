---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555936"
---
# <span data-ttu-id="dfa91-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="dfa91-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="dfa91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfa91-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa91-103">Отмена задания миграции управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="dfa91-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="dfa91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfa91-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="dfa91-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfa91-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa91-106">Отмена задания миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="dfa91-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="dfa91-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfa91-107">EXAMPLES</span></span>

### <span data-ttu-id="dfa91-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dfa91-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="dfa91-109">Отмена задания миграции управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="dfa91-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="dfa91-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfa91-110">PARAMETERS</span></span>

### <span data-ttu-id="dfa91-111">-Location</span><span class="sxs-lookup"><span data-stu-id="dfa91-111">-Location</span></span>
<span data-ttu-id="dfa91-112">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="dfa91-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa91-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dfa91-113">-Name</span></span>
<span data-ttu-id="dfa91-114">Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="dfa91-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa91-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa91-115">CommonParameters</span></span>
<span data-ttu-id="dfa91-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfa91-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa91-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa91-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa91-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfa91-118">INPUTS</span></span>

## <span data-ttu-id="dfa91-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfa91-119">OUTPUTS</span></span>

### <span data-ttu-id="dfa91-120">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="dfa91-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="dfa91-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfa91-121">NOTES</span></span>

## <span data-ttu-id="dfa91-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfa91-122">RELATED LINKS</span></span>

