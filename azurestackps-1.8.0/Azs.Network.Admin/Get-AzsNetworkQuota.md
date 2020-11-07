---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908497"
---
# <span data-ttu-id="8e26f-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="8e26f-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="8e26f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e26f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e26f-103">Список всех квот.</span><span class="sxs-lookup"><span data-stu-id="8e26f-103">List all quotas.</span></span>

## <span data-ttu-id="8e26f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e26f-104">SYNTAX</span></span>

### <span data-ttu-id="8e26f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e26f-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="8e26f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8e26f-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="8e26f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e26f-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8e26f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e26f-108">DESCRIPTION</span></span>
<span data-ttu-id="8e26f-109">Список всех квот.</span><span class="sxs-lookup"><span data-stu-id="8e26f-109">List all quotas.</span></span>
<span data-ttu-id="8e26f-110">Ограничьте список, передав имя или фильтр.</span><span class="sxs-lookup"><span data-stu-id="8e26f-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="8e26f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e26f-111">EXAMPLES</span></span>

### <span data-ttu-id="8e26f-112">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="8e26f-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="8e26f-113">В этой статье перечислены все сетевые квоты.</span><span class="sxs-lookup"><span data-stu-id="8e26f-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="8e26f-114">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="8e26f-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="8e26f-115">Получает указанную квоту сети.</span><span class="sxs-lookup"><span data-stu-id="8e26f-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="8e26f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e26f-116">PARAMETERS</span></span>

### <span data-ttu-id="8e26f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e26f-117">-Name</span></span>
<span data-ttu-id="8e26f-118">Имя ресурса сетевой квоты.</span><span class="sxs-lookup"><span data-stu-id="8e26f-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="8e26f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8e26f-119">-Location</span></span>
<span data-ttu-id="8e26f-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e26f-120">Location of the resource.</span></span>

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

### <span data-ttu-id="8e26f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e26f-121">-ResourceId</span></span>
<span data-ttu-id="8e26f-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e26f-122">The resource id.</span></span>

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

### <span data-ttu-id="8e26f-123">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="8e26f-123">-Filter</span></span>
<span data-ttu-id="8e26f-124">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="8e26f-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="8e26f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e26f-125">CommonParameters</span></span>
<span data-ttu-id="8e26f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e26f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e26f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e26f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e26f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e26f-128">INPUTS</span></span>

## <span data-ttu-id="8e26f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e26f-129">OUTPUTS</span></span>

### <span data-ttu-id="8e26f-130">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="8e26f-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="8e26f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e26f-131">NOTES</span></span>

## <span data-ttu-id="8e26f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e26f-132">RELATED LINKS</span></span>
