---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907754"
---
# <span data-ttu-id="98244-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="98244-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="98244-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98244-102">SYNOPSIS</span></span>
<span data-ttu-id="98244-103">Список всех клиентов каталогов в текущей подписке и указанным именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98244-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="98244-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98244-104">SYNTAX</span></span>

### <span data-ttu-id="98244-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98244-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="98244-106">Получить</span><span class="sxs-lookup"><span data-stu-id="98244-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="98244-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="98244-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="98244-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98244-108">DESCRIPTION</span></span>
<span data-ttu-id="98244-109">Список всех клиентов каталогов в текущей подписке и указанным именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98244-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="98244-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98244-110">EXAMPLES</span></span>

### <span data-ttu-id="98244-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98244-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="98244-112">Список всех клиентов каталогов в текущей подписке и указанным именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98244-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="98244-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98244-113">PARAMETERS</span></span>

### <span data-ttu-id="98244-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98244-114">-Name</span></span>
<span data-ttu-id="98244-115">Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="98244-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="98244-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98244-116">-ResourceGroupName</span></span>
<span data-ttu-id="98244-117">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="98244-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="98244-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98244-118">-ResourceId</span></span>
<span data-ttu-id="98244-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="98244-119">The resource id.</span></span>

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

### <span data-ttu-id="98244-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="98244-120">-Skip</span></span>
<span data-ttu-id="98244-121">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="98244-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="98244-122">-Top</span><span class="sxs-lookup"><span data-stu-id="98244-122">-Top</span></span>
<span data-ttu-id="98244-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="98244-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="98244-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="98244-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="98244-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98244-125">CommonParameters</span></span>
<span data-ttu-id="98244-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98244-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98244-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98244-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98244-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98244-128">INPUTS</span></span>

## <span data-ttu-id="98244-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98244-129">OUTPUTS</span></span>

### <span data-ttu-id="98244-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="98244-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="98244-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="98244-131">NOTES</span></span>

## <span data-ttu-id="98244-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98244-132">RELATED LINKS</span></span>

