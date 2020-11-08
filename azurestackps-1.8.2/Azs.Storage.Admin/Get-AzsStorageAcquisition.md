---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076892"
---
# <span data-ttu-id="bf289-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="bf289-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="bf289-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf289-102">SYNOPSIS</span></span>
<span data-ttu-id="bf289-103">Возвращает список acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="bf289-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="bf289-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf289-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf289-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf289-105">DESCRIPTION</span></span>
<span data-ttu-id="bf289-106">Возвращает список acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="bf289-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="bf289-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf289-107">EXAMPLES</span></span>

### <span data-ttu-id="bf289-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="bf289-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="bf289-109">Получение списка acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="bf289-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="bf289-110">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="bf289-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="bf289-111">Получение списка acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="bf289-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="bf289-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf289-112">PARAMETERS</span></span>

### <span data-ttu-id="bf289-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="bf289-113">-FarmName</span></span>
<span data-ttu-id="bf289-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="bf289-114">Farm Id.</span></span>

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

### <span data-ttu-id="bf289-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf289-115">-ResourceGroupName</span></span>
<span data-ttu-id="bf289-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bf289-116">Resource group name.</span></span>

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

### <span data-ttu-id="bf289-117">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="bf289-117">-Filter</span></span>
<span data-ttu-id="bf289-118">Строка фильтра</span><span class="sxs-lookup"><span data-stu-id="bf289-118">Filter string</span></span>

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

### <span data-ttu-id="bf289-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf289-119">CommonParameters</span></span>
<span data-ttu-id="bf289-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf289-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf289-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf289-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf289-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf289-122">INPUTS</span></span>

## <span data-ttu-id="bf289-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf289-123">OUTPUTS</span></span>

## <span data-ttu-id="bf289-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf289-124">NOTES</span></span>

## <span data-ttu-id="bf289-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf289-125">RELATED LINKS</span></span>
