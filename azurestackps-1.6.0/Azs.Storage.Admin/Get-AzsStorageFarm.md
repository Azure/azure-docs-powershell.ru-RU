---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 419bddaaa121e052b486bf4bb5408fcae6160fd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555748"
---
# <span data-ttu-id="b01d5-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="b01d5-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="b01d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b01d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b01d5-103">Возвращает список всех ферм хранилища.</span><span class="sxs-lookup"><span data-stu-id="b01d5-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="b01d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b01d5-104">SYNTAX</span></span>

### <span data-ttu-id="b01d5-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b01d5-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b01d5-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b01d5-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b01d5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b01d5-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b01d5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b01d5-108">DESCRIPTION</span></span>
<span data-ttu-id="b01d5-109">Возвращает список всех ферм хранилища.</span><span class="sxs-lookup"><span data-stu-id="b01d5-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="b01d5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b01d5-110">EXAMPLES</span></span>

### <span data-ttu-id="b01d5-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b01d5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="b01d5-112">Получение списка всех ферм хранилищ.</span><span class="sxs-lookup"><span data-stu-id="b01d5-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="b01d5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b01d5-113">PARAMETERS</span></span>

### <span data-ttu-id="b01d5-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b01d5-114">-Name</span></span>
<span data-ttu-id="b01d5-115">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="b01d5-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01d5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b01d5-116">-ResourceGroupName</span></span>
<span data-ttu-id="b01d5-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b01d5-117">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01d5-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b01d5-118">-ResourceId</span></span>
<span data-ttu-id="b01d5-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b01d5-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b01d5-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="b01d5-120">-Skip</span></span>
<span data-ttu-id="b01d5-121">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="b01d5-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01d5-122">-Top</span><span class="sxs-lookup"><span data-stu-id="b01d5-122">-Top</span></span>
<span data-ttu-id="b01d5-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="b01d5-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b01d5-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="b01d5-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01d5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01d5-125">CommonParameters</span></span>
<span data-ttu-id="b01d5-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b01d5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01d5-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b01d5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01d5-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b01d5-128">INPUTS</span></span>

## <span data-ttu-id="b01d5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b01d5-129">OUTPUTS</span></span>

### <span data-ttu-id="b01d5-130">Microsoft. AzureStack. Management. Storage. admin. Models. ферма</span><span class="sxs-lookup"><span data-stu-id="b01d5-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="b01d5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b01d5-131">NOTES</span></span>

## <span data-ttu-id="b01d5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b01d5-132">RELATED LINKS</span></span>

