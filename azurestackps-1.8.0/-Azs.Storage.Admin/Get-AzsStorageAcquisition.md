---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908581"
---
# <span data-ttu-id="aca45-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="aca45-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="aca45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aca45-102">SYNOPSIS</span></span>
<span data-ttu-id="aca45-103">Возвращает список acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="aca45-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="aca45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aca45-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="aca45-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aca45-105">DESCRIPTION</span></span>
<span data-ttu-id="aca45-106">Возвращает список acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="aca45-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="aca45-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aca45-107">EXAMPLES</span></span>

### <span data-ttu-id="aca45-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aca45-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="aca45-109">Получение списка acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="aca45-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="aca45-110">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="aca45-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="aca45-111">Получение списка acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="aca45-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="aca45-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aca45-112">PARAMETERS</span></span>

### <span data-ttu-id="aca45-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="aca45-113">-FarmName</span></span>
<span data-ttu-id="aca45-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="aca45-114">Farm Id.</span></span>

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

### <span data-ttu-id="aca45-115">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="aca45-115">-Filter</span></span>
<span data-ttu-id="aca45-116">Строка фильтра</span><span class="sxs-lookup"><span data-stu-id="aca45-116">Filter string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca45-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca45-117">-ResourceGroupName</span></span>
<span data-ttu-id="aca45-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aca45-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca45-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca45-119">CommonParameters</span></span>
<span data-ttu-id="aca45-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aca45-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca45-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca45-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca45-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aca45-122">INPUTS</span></span>

## <span data-ttu-id="aca45-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aca45-123">OUTPUTS</span></span>

## <span data-ttu-id="aca45-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="aca45-124">NOTES</span></span>

## <span data-ttu-id="aca45-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aca45-125">RELATED LINKS</span></span>

