---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076642"
---
# <span data-ttu-id="d35cc-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="d35cc-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="d35cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d35cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d35cc-103">Возвращает список всех ролей инфраструктуры в местоположении.</span><span class="sxs-lookup"><span data-stu-id="d35cc-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="d35cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d35cc-104">SYNTAX</span></span>

### <span data-ttu-id="d35cc-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d35cc-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d35cc-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d35cc-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d35cc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d35cc-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d35cc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d35cc-108">DESCRIPTION</span></span>
<span data-ttu-id="d35cc-109">Возвращает список всех ролей инфраструктуры в местоположении.</span><span class="sxs-lookup"><span data-stu-id="d35cc-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="d35cc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d35cc-110">EXAMPLES</span></span>

### <span data-ttu-id="d35cc-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="d35cc-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="d35cc-112">Получение списка всех ролей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d35cc-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="d35cc-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="d35cc-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="d35cc-114">Получить роль инфраструктуры на основе имени.</span><span class="sxs-lookup"><span data-stu-id="d35cc-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="d35cc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d35cc-115">PARAMETERS</span></span>

### <span data-ttu-id="d35cc-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d35cc-116">-Name</span></span>
<span data-ttu-id="d35cc-117">Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d35cc-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="d35cc-118">-Location</span><span class="sxs-lookup"><span data-stu-id="d35cc-118">-Location</span></span>
<span data-ttu-id="d35cc-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d35cc-119">Location of the resource.</span></span>

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

### <span data-ttu-id="d35cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d35cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="d35cc-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d35cc-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d35cc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d35cc-122">-ResourceId</span></span>
<span data-ttu-id="d35cc-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="d35cc-123">The resource id.</span></span>

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

### <span data-ttu-id="d35cc-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="d35cc-124">-Filter</span></span>
<span data-ttu-id="d35cc-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="d35cc-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35cc-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="d35cc-126">-Skip</span></span>
<span data-ttu-id="d35cc-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="d35cc-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d35cc-128">-Top</span><span class="sxs-lookup"><span data-stu-id="d35cc-128">-Top</span></span>
<span data-ttu-id="d35cc-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="d35cc-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d35cc-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="d35cc-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d35cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35cc-131">CommonParameters</span></span>
<span data-ttu-id="d35cc-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d35cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35cc-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d35cc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35cc-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d35cc-134">INPUTS</span></span>

## <span data-ttu-id="d35cc-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d35cc-135">OUTPUTS</span></span>

### <span data-ttu-id="d35cc-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="d35cc-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="d35cc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d35cc-137">NOTES</span></span>

## <span data-ttu-id="d35cc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d35cc-138">RELATED LINKS</span></span>
