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
ms.locfileid: "93731714"
---
# <span data-ttu-id="457b4-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="457b4-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="457b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="457b4-102">SYNOPSIS</span></span>
<span data-ttu-id="457b4-103">Возвращает список всех экземпляров ролей инфраструктуры в расположении.</span><span class="sxs-lookup"><span data-stu-id="457b4-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="457b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="457b4-104">SYNTAX</span></span>

### <span data-ttu-id="457b4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="457b4-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="457b4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="457b4-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="457b4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="457b4-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="457b4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="457b4-108">DESCRIPTION</span></span>
<span data-ttu-id="457b4-109">Возвращает список всех экземпляров ролей инфраструктуры в расположении.</span><span class="sxs-lookup"><span data-stu-id="457b4-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="457b4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="457b4-110">EXAMPLES</span></span>

### <span data-ttu-id="457b4-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="457b4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="457b4-112">Возвращают список всех экземпляров ролей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="457b4-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="457b4-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="457b4-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="457b4-114">Возвращают единственный экземпляр роли инфраструктуры на основе имени.</span><span class="sxs-lookup"><span data-stu-id="457b4-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="457b4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="457b4-115">PARAMETERS</span></span>

### <span data-ttu-id="457b4-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="457b4-116">-Filter</span></span>
<span data-ttu-id="457b4-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="457b4-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="457b4-118">-Location</span><span class="sxs-lookup"><span data-stu-id="457b4-118">-Location</span></span>
<span data-ttu-id="457b4-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="457b4-119">Location of the resource.</span></span>

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

### <span data-ttu-id="457b4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="457b4-120">-Name</span></span>
<span data-ttu-id="457b4-121">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="457b4-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="457b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="457b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="457b4-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="457b4-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="457b4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="457b4-124">-ResourceId</span></span>
<span data-ttu-id="457b4-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="457b4-125">The resource id.</span></span>

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

### <span data-ttu-id="457b4-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="457b4-126">-Skip</span></span>
<span data-ttu-id="457b4-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="457b4-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="457b4-128">-Top</span><span class="sxs-lookup"><span data-stu-id="457b4-128">-Top</span></span>
<span data-ttu-id="457b4-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="457b4-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="457b4-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="457b4-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="457b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457b4-131">CommonParameters</span></span>
<span data-ttu-id="457b4-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="457b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457b4-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="457b4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457b4-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="457b4-134">INPUTS</span></span>

## <span data-ttu-id="457b4-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="457b4-135">OUTPUTS</span></span>

### <span data-ttu-id="457b4-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="457b4-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="457b4-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="457b4-137">NOTES</span></span>

## <span data-ttu-id="457b4-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="457b4-138">RELATED LINKS</span></span>

