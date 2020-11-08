---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f8c9192100536a04b664f981a9df9e1508a1f87
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076913"
---
# <span data-ttu-id="9a8a6-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="9a8a6-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="9a8a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8a6-103">Возвращает список общих ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a8a6-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="9a8a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a8a6-104">SYNTAX</span></span>

### <span data-ttu-id="9a8a6-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a8a6-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9a8a6-106">Получить</span><span class="sxs-lookup"><span data-stu-id="9a8a6-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -ShareName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9a8a6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a8a6-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9a8a6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a8a6-108">DESCRIPTION</span></span>
<span data-ttu-id="9a8a6-109">Возвращает список общих ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a8a6-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="9a8a6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a8a6-110">EXAMPLES</span></span>

### <span data-ttu-id="9a8a6-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="9a8a6-111">EXAMPLE 1</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="9a8a6-112">Получите список общих ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a8a6-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="9a8a6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a8a6-113">PARAMETERS</span></span>

### <span data-ttu-id="9a8a6-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9a8a6-114">-FarmName</span></span>
<span data-ttu-id="9a8a6-115">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="9a8a6-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8a6-116">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="9a8a6-116">-ShareName</span></span>
<span data-ttu-id="9a8a6-117">Имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9a8a6-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8a6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a8a6-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a8a6-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a8a6-119">Resource group name.</span></span>

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

### <span data-ttu-id="9a8a6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a8a6-120">-ResourceId</span></span>
<span data-ttu-id="9a8a6-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9a8a6-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8a6-122">CommonParameters</span></span>
<span data-ttu-id="9a8a6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a8a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8a6-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a8a6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8a6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a8a6-125">INPUTS</span></span>

## <span data-ttu-id="9a8a6-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a8a6-126">OUTPUTS</span></span>

### <span data-ttu-id="9a8a6-127">Microsoft. AzureStack. Management. Storage. admin. Model. Share</span><span class="sxs-lookup"><span data-stu-id="9a8a6-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="9a8a6-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a8a6-128">NOTES</span></span>

## <span data-ttu-id="9a8a6-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a8a6-129">RELATED LINKS</span></span>
