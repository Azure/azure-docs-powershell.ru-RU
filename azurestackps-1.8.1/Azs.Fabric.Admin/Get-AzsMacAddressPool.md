---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e22024b1b246a60104db0832860ed0aff699ff5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908834"
---
# <span data-ttu-id="02058-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="02058-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="02058-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02058-102">SYNOPSIS</span></span>
<span data-ttu-id="02058-103">Возвращает список всех пулов MAC-адресов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="02058-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="02058-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02058-104">SYNTAX</span></span>

### <span data-ttu-id="02058-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02058-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="02058-106">Получить</span><span class="sxs-lookup"><span data-stu-id="02058-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="02058-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="02058-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="02058-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02058-108">DESCRIPTION</span></span>
<span data-ttu-id="02058-109">Возвращает список всех пулов MAC-адресов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="02058-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="02058-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02058-110">EXAMPLES</span></span>

### <span data-ttu-id="02058-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="02058-111">EXAMPLE 1</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="02058-112">Получение всех пулов MAC-адресов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="02058-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="02058-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="02058-113">EXAMPLE 2</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="02058-114">Получение определенного пула MAC-адресов в местоположении на основе имени.</span><span class="sxs-lookup"><span data-stu-id="02058-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="02058-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02058-115">PARAMETERS</span></span>

### <span data-ttu-id="02058-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02058-116">-Name</span></span>
<span data-ttu-id="02058-117">Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="02058-117">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="02058-118">-Location</span><span class="sxs-lookup"><span data-stu-id="02058-118">-Location</span></span>
<span data-ttu-id="02058-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="02058-119">Location of the resource.</span></span>

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

### <span data-ttu-id="02058-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02058-120">-ResourceGroupName</span></span>
<span data-ttu-id="02058-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02058-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="02058-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02058-122">-ResourceId</span></span>
<span data-ttu-id="02058-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="02058-123">The resource id.</span></span>

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

### <span data-ttu-id="02058-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="02058-124">-Filter</span></span>
<span data-ttu-id="02058-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="02058-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="02058-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="02058-126">-Skip</span></span>
<span data-ttu-id="02058-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="02058-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="02058-128">-Top</span><span class="sxs-lookup"><span data-stu-id="02058-128">-Top</span></span>
<span data-ttu-id="02058-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="02058-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="02058-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="02058-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="02058-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02058-131">CommonParameters</span></span>
<span data-ttu-id="02058-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02058-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02058-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02058-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02058-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02058-134">INPUTS</span></span>

## <span data-ttu-id="02058-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02058-135">OUTPUTS</span></span>

### <span data-ttu-id="02058-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="02058-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="02058-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="02058-137">NOTES</span></span>

## <span data-ttu-id="02058-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02058-138">RELATED LINKS</span></span>
