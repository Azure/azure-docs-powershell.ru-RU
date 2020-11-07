---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908465"
---
# <span data-ttu-id="e0173-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="e0173-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="e0173-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0173-102">SYNOPSIS</span></span>
<span data-ttu-id="e0173-103">Список всех клиентов каталогов в текущей подписке и указанным именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0173-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="e0173-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0173-104">SYNTAX</span></span>

### <span data-ttu-id="e0173-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0173-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e0173-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e0173-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e0173-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0173-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e0173-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0173-108">DESCRIPTION</span></span>
<span data-ttu-id="e0173-109">Список всех клиентов каталогов в текущей подписке и указанным именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0173-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="e0173-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0173-110">EXAMPLES</span></span>

### <span data-ttu-id="e0173-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e0173-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="e0173-112">Список всех клиентов каталогов в текущей подписке и указанным именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0173-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="e0173-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0173-113">PARAMETERS</span></span>

### <span data-ttu-id="e0173-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0173-114">-Name</span></span>
<span data-ttu-id="e0173-115">Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e0173-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="e0173-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0173-116">-ResourceGroupName</span></span>
<span data-ttu-id="e0173-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="e0173-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="e0173-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0173-118">-ResourceId</span></span>
<span data-ttu-id="e0173-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e0173-119">The resource id.</span></span>

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

### <span data-ttu-id="e0173-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="e0173-120">-Skip</span></span>
<span data-ttu-id="e0173-121">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="e0173-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e0173-122">-Top</span><span class="sxs-lookup"><span data-stu-id="e0173-122">-Top</span></span>
<span data-ttu-id="e0173-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="e0173-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e0173-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="e0173-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e0173-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0173-125">CommonParameters</span></span>
<span data-ttu-id="e0173-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0173-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0173-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0173-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0173-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0173-128">INPUTS</span></span>

## <span data-ttu-id="e0173-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0173-129">OUTPUTS</span></span>

### <span data-ttu-id="e0173-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="e0173-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="e0173-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0173-131">NOTES</span></span>

## <span data-ttu-id="e0173-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0173-132">RELATED LINKS</span></span>

