---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907737"
---
# <span data-ttu-id="1303e-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="1303e-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="1303e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1303e-102">SYNOPSIS</span></span>
<span data-ttu-id="1303e-103">Возвращает список acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="1303e-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="1303e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1303e-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1303e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1303e-105">DESCRIPTION</span></span>
<span data-ttu-id="1303e-106">Возвращает список acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="1303e-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="1303e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1303e-107">EXAMPLES</span></span>

### <span data-ttu-id="1303e-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1303e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="1303e-109">Получение списка acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="1303e-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="1303e-110">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1303e-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="1303e-111">Получение списка acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="1303e-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="1303e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1303e-112">PARAMETERS</span></span>

### <span data-ttu-id="1303e-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="1303e-113">-FarmName</span></span>
<span data-ttu-id="1303e-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="1303e-114">Farm Id.</span></span>

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

### <span data-ttu-id="1303e-115">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="1303e-115">-Filter</span></span>
<span data-ttu-id="1303e-116">Строка фильтра</span><span class="sxs-lookup"><span data-stu-id="1303e-116">Filter string</span></span>

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

### <span data-ttu-id="1303e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1303e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1303e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1303e-118">Resource group name.</span></span>

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

### <span data-ttu-id="1303e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1303e-119">CommonParameters</span></span>
<span data-ttu-id="1303e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1303e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1303e-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1303e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1303e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1303e-122">INPUTS</span></span>

## <span data-ttu-id="1303e-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1303e-123">OUTPUTS</span></span>

## <span data-ttu-id="1303e-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1303e-124">NOTES</span></span>

## <span data-ttu-id="1303e-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1303e-125">RELATED LINKS</span></span>

