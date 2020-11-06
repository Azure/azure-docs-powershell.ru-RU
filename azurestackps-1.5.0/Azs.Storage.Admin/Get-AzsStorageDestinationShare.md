---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47ac85406955592cba566df505900e6c42befb7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555408"
---
# <span data-ttu-id="14907-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="14907-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="14907-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14907-102">SYNOPSIS</span></span>
<span data-ttu-id="14907-103">Возвращает список целевых долей назначения, которые система рассматривает как наиболее подходящее число потенциальных миграций.</span><span class="sxs-lookup"><span data-stu-id="14907-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="14907-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14907-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="14907-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14907-105">DESCRIPTION</span></span>
<span data-ttu-id="14907-106">Возвращает список целевых долей назначения, которые система рассматривает как наиболее подходящее число потенциальных миграций.</span><span class="sxs-lookup"><span data-stu-id="14907-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="14907-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14907-107">EXAMPLES</span></span>

### <span data-ttu-id="14907-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14907-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="14907-109">Получите список конечных долей, которые система рассчитает наиболее подходящими кандидатами для миграции.</span><span class="sxs-lookup"><span data-stu-id="14907-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="14907-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14907-110">PARAMETERS</span></span>

### <span data-ttu-id="14907-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="14907-111">-FarmName</span></span>
<span data-ttu-id="14907-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="14907-112">Farm Id.</span></span>

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

### <span data-ttu-id="14907-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14907-113">-ResourceGroupName</span></span>
<span data-ttu-id="14907-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14907-114">Resource group name.</span></span>

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

### <span data-ttu-id="14907-115">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="14907-115">-SourceShareName</span></span>
<span data-ttu-id="14907-116">Имя общего доступа, содержащего контейнеры, которые нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="14907-116">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="14907-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14907-117">CommonParameters</span></span>
<span data-ttu-id="14907-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14907-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14907-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14907-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14907-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14907-120">INPUTS</span></span>

## <span data-ttu-id="14907-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14907-121">OUTPUTS</span></span>

## <span data-ttu-id="14907-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="14907-122">NOTES</span></span>

## <span data-ttu-id="14907-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14907-123">RELATED LINKS</span></span>

