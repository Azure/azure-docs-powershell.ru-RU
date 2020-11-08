---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a75fafa646839375bf9dc7f1a64b3084fd31ee4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076888"
---
# <span data-ttu-id="96e5e-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="96e5e-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="96e5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="96e5e-103">Возвращает список целевых долей назначения, которые система рассматривает как наиболее подходящее число потенциальных миграций.</span><span class="sxs-lookup"><span data-stu-id="96e5e-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="96e5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96e5e-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="96e5e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="96e5e-106">Возвращает список целевых долей назначения, которые система рассматривает как наиболее подходящее число потенциальных миграций.</span><span class="sxs-lookup"><span data-stu-id="96e5e-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="96e5e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="96e5e-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="96e5e-108">EXAMPLE 1</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="96e5e-109">Получите список конечных долей, которые система рассчитает наиболее подходящими кандидатами для миграции.</span><span class="sxs-lookup"><span data-stu-id="96e5e-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="96e5e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96e5e-110">PARAMETERS</span></span>

### <span data-ttu-id="96e5e-111">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="96e5e-111">-SourceShareName</span></span>
<span data-ttu-id="96e5e-112">Имя общего доступа, содержащего контейнеры, которые нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="96e5e-112">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="96e5e-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="96e5e-113">-FarmName</span></span>
<span data-ttu-id="96e5e-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="96e5e-114">Farm Id.</span></span>

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

### <span data-ttu-id="96e5e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e5e-115">-ResourceGroupName</span></span>
<span data-ttu-id="96e5e-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96e5e-116">Resource group name.</span></span>

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

### <span data-ttu-id="96e5e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e5e-117">CommonParameters</span></span>
<span data-ttu-id="96e5e-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96e5e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e5e-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e5e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e5e-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96e5e-120">INPUTS</span></span>

## <span data-ttu-id="96e5e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96e5e-121">OUTPUTS</span></span>

## <span data-ttu-id="96e5e-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="96e5e-122">NOTES</span></span>

## <span data-ttu-id="96e5e-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96e5e-123">RELATED LINKS</span></span>
