---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dac95eced72f70d3471019136d302fcdfe95f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555348"
---
# <span data-ttu-id="8ece1-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="8ece1-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="8ece1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ece1-102">SYNOPSIS</span></span>
<span data-ttu-id="8ece1-103">Возвращает список всех ролей инфраструктуры в местоположении.</span><span class="sxs-lookup"><span data-stu-id="8ece1-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="8ece1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ece1-104">SYNTAX</span></span>

### <span data-ttu-id="8ece1-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ece1-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8ece1-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8ece1-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ece1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ece1-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8ece1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ece1-108">DESCRIPTION</span></span>
<span data-ttu-id="8ece1-109">Возвращает список всех ролей инфраструктуры в местоположении.</span><span class="sxs-lookup"><span data-stu-id="8ece1-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="8ece1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ece1-110">EXAMPLES</span></span>

### <span data-ttu-id="8ece1-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ece1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="8ece1-112">Получение списка всех ролей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="8ece1-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="8ece1-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ece1-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="8ece1-114">Получить роль инфраструктуры на основе имени.</span><span class="sxs-lookup"><span data-stu-id="8ece1-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="8ece1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ece1-115">PARAMETERS</span></span>

### <span data-ttu-id="8ece1-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="8ece1-116">-Filter</span></span>
<span data-ttu-id="8ece1-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="8ece1-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="8ece1-118">-Location</span><span class="sxs-lookup"><span data-stu-id="8ece1-118">-Location</span></span>
<span data-ttu-id="8ece1-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ece1-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8ece1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ece1-120">-Name</span></span>
<span data-ttu-id="8ece1-121">Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="8ece1-121">Infrastructure role name.</span></span>

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

### <span data-ttu-id="8ece1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ece1-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ece1-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ece1-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8ece1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ece1-124">-ResourceId</span></span>
<span data-ttu-id="8ece1-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ece1-125">The resource id.</span></span>

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

### <span data-ttu-id="8ece1-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="8ece1-126">-Skip</span></span>
<span data-ttu-id="8ece1-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="8ece1-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8ece1-128">-Top</span><span class="sxs-lookup"><span data-stu-id="8ece1-128">-Top</span></span>
<span data-ttu-id="8ece1-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="8ece1-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8ece1-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="8ece1-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8ece1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ece1-131">CommonParameters</span></span>
<span data-ttu-id="8ece1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ece1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ece1-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ece1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ece1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ece1-134">INPUTS</span></span>

## <span data-ttu-id="8ece1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ece1-135">OUTPUTS</span></span>

### <span data-ttu-id="8ece1-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="8ece1-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="8ece1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ece1-137">NOTES</span></span>

## <span data-ttu-id="8ece1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ece1-138">RELATED LINKS</span></span>

