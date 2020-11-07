---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb5d980efc5f4e4ad7aff13a8f91832589175039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907938"
---
# <span data-ttu-id="8c879-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="8c879-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="8c879-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c879-102">SYNOPSIS</span></span>
<span data-ttu-id="8c879-103">Список всех квот.</span><span class="sxs-lookup"><span data-stu-id="8c879-103">List all quotas.</span></span>

## <span data-ttu-id="8c879-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c879-104">SYNTAX</span></span>

### <span data-ttu-id="8c879-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c879-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c879-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8c879-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c879-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c879-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8c879-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c879-108">DESCRIPTION</span></span>
<span data-ttu-id="8c879-109">Список всех квот.</span><span class="sxs-lookup"><span data-stu-id="8c879-109">List all quotas.</span></span>
<span data-ttu-id="8c879-110">Ограничьте список, передав имя или фильтр.</span><span class="sxs-lookup"><span data-stu-id="8c879-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="8c879-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c879-111">EXAMPLES</span></span>

### <span data-ttu-id="8c879-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8c879-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="8c879-113">В этой статье перечислены все сетевые квоты.</span><span class="sxs-lookup"><span data-stu-id="8c879-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="8c879-114">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8c879-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="8c879-115">Получает указанную квоту сети.</span><span class="sxs-lookup"><span data-stu-id="8c879-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="8c879-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c879-116">PARAMETERS</span></span>

### <span data-ttu-id="8c879-117">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="8c879-117">-Filter</span></span>
<span data-ttu-id="8c879-118">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="8c879-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="8c879-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8c879-119">-Location</span></span>
<span data-ttu-id="8c879-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c879-120">Location of the resource.</span></span>

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

### <span data-ttu-id="8c879-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c879-121">-Name</span></span>
<span data-ttu-id="8c879-122">Имя ресурса сетевой квоты.</span><span class="sxs-lookup"><span data-stu-id="8c879-122">Network quota resource name.</span></span>

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

### <span data-ttu-id="8c879-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c879-123">-ResourceId</span></span>
<span data-ttu-id="8c879-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c879-124">The resource id.</span></span>

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

### <span data-ttu-id="8c879-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c879-125">CommonParameters</span></span>
<span data-ttu-id="8c879-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c879-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c879-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c879-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c879-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c879-128">INPUTS</span></span>

## <span data-ttu-id="8c879-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c879-129">OUTPUTS</span></span>

### <span data-ttu-id="8c879-130">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="8c879-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="8c879-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c879-131">NOTES</span></span>

## <span data-ttu-id="8c879-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c879-132">RELATED LINKS</span></span>

