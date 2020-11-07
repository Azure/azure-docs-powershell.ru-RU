---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908853"
---
# <span data-ttu-id="712d7-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="712d7-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="712d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="712d7-102">SYNOPSIS</span></span>
<span data-ttu-id="712d7-103">Возвращает список всех экземпляров ролей инфраструктуры в расположении.</span><span class="sxs-lookup"><span data-stu-id="712d7-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="712d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="712d7-104">SYNTAX</span></span>

### <span data-ttu-id="712d7-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="712d7-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="712d7-106">Получить</span><span class="sxs-lookup"><span data-stu-id="712d7-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="712d7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="712d7-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="712d7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="712d7-108">DESCRIPTION</span></span>
<span data-ttu-id="712d7-109">Возвращает список всех экземпляров ролей инфраструктуры в расположении.</span><span class="sxs-lookup"><span data-stu-id="712d7-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="712d7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="712d7-110">EXAMPLES</span></span>

### <span data-ttu-id="712d7-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="712d7-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="712d7-112">Возвращают список всех экземпляров ролей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="712d7-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="712d7-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="712d7-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="712d7-114">Возвращают единственный экземпляр роли инфраструктуры на основе имени.</span><span class="sxs-lookup"><span data-stu-id="712d7-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="712d7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="712d7-115">PARAMETERS</span></span>

### <span data-ttu-id="712d7-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="712d7-116">-Name</span></span>
<span data-ttu-id="712d7-117">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="712d7-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="712d7-118">-Location</span><span class="sxs-lookup"><span data-stu-id="712d7-118">-Location</span></span>
<span data-ttu-id="712d7-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="712d7-119">Location of the resource.</span></span>

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

### <span data-ttu-id="712d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="712d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="712d7-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="712d7-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="712d7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="712d7-122">-ResourceId</span></span>
<span data-ttu-id="712d7-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="712d7-123">The resource id.</span></span>

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

### <span data-ttu-id="712d7-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="712d7-124">-Filter</span></span>
<span data-ttu-id="712d7-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="712d7-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="712d7-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="712d7-126">-Skip</span></span>
<span data-ttu-id="712d7-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="712d7-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="712d7-128">-Top</span><span class="sxs-lookup"><span data-stu-id="712d7-128">-Top</span></span>
<span data-ttu-id="712d7-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="712d7-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="712d7-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="712d7-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="712d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712d7-131">CommonParameters</span></span>
<span data-ttu-id="712d7-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="712d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712d7-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="712d7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712d7-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="712d7-134">INPUTS</span></span>

## <span data-ttu-id="712d7-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="712d7-135">OUTPUTS</span></span>

### <span data-ttu-id="712d7-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="712d7-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="712d7-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="712d7-137">NOTES</span></span>

## <span data-ttu-id="712d7-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="712d7-138">RELATED LINKS</span></span>
