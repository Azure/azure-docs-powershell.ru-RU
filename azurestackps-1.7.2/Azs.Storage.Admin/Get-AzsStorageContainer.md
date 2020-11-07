---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907585"
---
# <span data-ttu-id="0daca-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0daca-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="0daca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0daca-102">SYNOPSIS</span></span>
<span data-ttu-id="0daca-103">Возвращает список контейнеров, которые можно перенести в указанном общем доступе.</span><span class="sxs-lookup"><span data-stu-id="0daca-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="0daca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0daca-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0daca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0daca-105">DESCRIPTION</span></span>
<span data-ttu-id="0daca-106">Возвращает список контейнеров, которые можно перенести в указанном общем доступе.</span><span class="sxs-lookup"><span data-stu-id="0daca-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="0daca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0daca-107">EXAMPLES</span></span>

### <span data-ttu-id="0daca-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0daca-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="0daca-109">Получение списка контейнеров, которые можно перенести в указанном общем доступе.</span><span class="sxs-lookup"><span data-stu-id="0daca-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="0daca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0daca-110">PARAMETERS</span></span>

### <span data-ttu-id="0daca-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="0daca-111">-FarmName</span></span>
<span data-ttu-id="0daca-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="0daca-112">Farm Id.</span></span>

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

### <span data-ttu-id="0daca-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0daca-113">-MaxCount</span></span>
<span data-ttu-id="0daca-114">Максимальное количество контейнеров.</span><span class="sxs-lookup"><span data-stu-id="0daca-114">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0daca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0daca-115">-ResourceGroupName</span></span>
<span data-ttu-id="0daca-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0daca-116">Resource group name.</span></span>

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

### <span data-ttu-id="0daca-117">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="0daca-117">-ShareName</span></span>
<span data-ttu-id="0daca-118">Имя общего доступа, содержащее контейнеры хранилища.</span><span class="sxs-lookup"><span data-stu-id="0daca-118">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="0daca-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="0daca-119">-StartIndex</span></span>
<span data-ttu-id="0daca-120">Начальный индекс для Get Containers.</span><span class="sxs-lookup"><span data-stu-id="0daca-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0daca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daca-121">CommonParameters</span></span>
<span data-ttu-id="0daca-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0daca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daca-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0daca-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daca-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0daca-124">INPUTS</span></span>

## <span data-ttu-id="0daca-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0daca-125">OUTPUTS</span></span>

## <span data-ttu-id="0daca-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="0daca-126">NOTES</span></span>

## <span data-ttu-id="0daca-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0daca-127">RELATED LINKS</span></span>

