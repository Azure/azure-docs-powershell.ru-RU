---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd280133b3a0bc536c57f839fcc0faab81669c03
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909005"
---
# <span data-ttu-id="4d044-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="4d044-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="4d044-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d044-102">SYNOPSIS</span></span>
<span data-ttu-id="4d044-103">Возвращает список всех ферм хранилища.</span><span class="sxs-lookup"><span data-stu-id="4d044-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="4d044-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d044-104">SYNTAX</span></span>

### <span data-ttu-id="4d044-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d044-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4d044-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4d044-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4d044-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d044-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4d044-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d044-108">DESCRIPTION</span></span>
<span data-ttu-id="4d044-109">Возвращает список всех ферм хранилища.</span><span class="sxs-lookup"><span data-stu-id="4d044-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="4d044-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d044-110">EXAMPLES</span></span>

### <span data-ttu-id="4d044-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="4d044-111">EXAMPLE 1</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="4d044-112">Получение списка всех ферм хранилищ.</span><span class="sxs-lookup"><span data-stu-id="4d044-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="4d044-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d044-113">PARAMETERS</span></span>

### <span data-ttu-id="4d044-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4d044-114">-Name</span></span>
<span data-ttu-id="4d044-115">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="4d044-115">Farm Id.</span></span>

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

### <span data-ttu-id="4d044-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d044-116">-ResourceGroupName</span></span>
<span data-ttu-id="4d044-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d044-117">Resource group name.</span></span>

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

### <span data-ttu-id="4d044-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d044-118">-ResourceId</span></span>
<span data-ttu-id="4d044-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4d044-119">The resource id.</span></span>

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

### <span data-ttu-id="4d044-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="4d044-120">-Skip</span></span>
<span data-ttu-id="4d044-121">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="4d044-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4d044-122">-Top</span><span class="sxs-lookup"><span data-stu-id="4d044-122">-Top</span></span>
<span data-ttu-id="4d044-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="4d044-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4d044-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="4d044-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4d044-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d044-125">CommonParameters</span></span>
<span data-ttu-id="4d044-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d044-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d044-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d044-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d044-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d044-128">INPUTS</span></span>

## <span data-ttu-id="4d044-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d044-129">OUTPUTS</span></span>

### <span data-ttu-id="4d044-130">Microsoft. AzureStack. Management. Storage. admin. Models. ферма</span><span class="sxs-lookup"><span data-stu-id="4d044-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="4d044-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d044-131">NOTES</span></span>

## <span data-ttu-id="4d044-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d044-132">RELATED LINKS</span></span>
