---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39955a2b99ffd7e3c604b4fc288f117face8205f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907862"
---
# <span data-ttu-id="b4660-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b4660-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="b4660-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4660-102">SYNOPSIS</span></span>
<span data-ttu-id="b4660-103">Возвращает список всех экземпляров ролей инфраструктуры в расположении.</span><span class="sxs-lookup"><span data-stu-id="b4660-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="b4660-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4660-104">SYNTAX</span></span>

### <span data-ttu-id="b4660-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4660-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b4660-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b4660-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4660-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4660-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b4660-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4660-108">DESCRIPTION</span></span>
<span data-ttu-id="b4660-109">Возвращает список всех экземпляров ролей инфраструктуры в расположении.</span><span class="sxs-lookup"><span data-stu-id="b4660-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="b4660-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4660-110">EXAMPLES</span></span>

### <span data-ttu-id="b4660-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b4660-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="b4660-112">Возвращают список всех экземпляров ролей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="b4660-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="b4660-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b4660-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="b4660-114">Возвращают единственный экземпляр роли инфраструктуры на основе имени.</span><span class="sxs-lookup"><span data-stu-id="b4660-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="b4660-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4660-115">PARAMETERS</span></span>

### <span data-ttu-id="b4660-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="b4660-116">-Filter</span></span>
<span data-ttu-id="b4660-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="b4660-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="b4660-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b4660-118">-Location</span></span>
<span data-ttu-id="b4660-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4660-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b4660-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4660-120">-Name</span></span>
<span data-ttu-id="b4660-121">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="b4660-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="b4660-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4660-122">-ResourceGroupName</span></span>
<span data-ttu-id="b4660-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4660-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b4660-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4660-124">-ResourceId</span></span>
<span data-ttu-id="b4660-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4660-125">The resource id.</span></span>

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

### <span data-ttu-id="b4660-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="b4660-126">-Skip</span></span>
<span data-ttu-id="b4660-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="b4660-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b4660-128">-Top</span><span class="sxs-lookup"><span data-stu-id="b4660-128">-Top</span></span>
<span data-ttu-id="b4660-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="b4660-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b4660-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="b4660-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b4660-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4660-131">CommonParameters</span></span>
<span data-ttu-id="b4660-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4660-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4660-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4660-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4660-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4660-134">INPUTS</span></span>

## <span data-ttu-id="b4660-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4660-135">OUTPUTS</span></span>

### <span data-ttu-id="b4660-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b4660-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="b4660-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4660-137">NOTES</span></span>

## <span data-ttu-id="b4660-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4660-138">RELATED LINKS</span></span>

