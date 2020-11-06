---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556016"
---
# <span data-ttu-id="af28c-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="af28c-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="af28c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af28c-102">SYNOPSIS</span></span>
<span data-ttu-id="af28c-103">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="af28c-103">Get the list of update locations.</span></span>

## <span data-ttu-id="af28c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af28c-104">SYNTAX</span></span>

### <span data-ttu-id="af28c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af28c-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="af28c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="af28c-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="af28c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="af28c-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="af28c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af28c-108">DESCRIPTION</span></span>
<span data-ttu-id="af28c-109">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="af28c-109">Get the list of update locations.</span></span> <span data-ttu-id="af28c-110">Возвращенные расположения можно использовать для получения доступных обновлений в определенном расположении с помощью Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="af28c-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="af28c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af28c-111">EXAMPLES</span></span>

### <span data-ttu-id="af28c-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="af28c-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="af28c-113">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="af28c-113">Get the list of update locations.</span></span>

## <span data-ttu-id="af28c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af28c-114">PARAMETERS</span></span>

### <span data-ttu-id="af28c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af28c-115">-Name</span></span>
<span data-ttu-id="af28c-116">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="af28c-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af28c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af28c-117">-ResourceGroupName</span></span>
<span data-ttu-id="af28c-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="af28c-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="af28c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af28c-119">-ResourceId</span></span>
<span data-ttu-id="af28c-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="af28c-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af28c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af28c-121">CommonParameters</span></span>
<span data-ttu-id="af28c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af28c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af28c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af28c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af28c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af28c-124">INPUTS</span></span>

## <span data-ttu-id="af28c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af28c-125">OUTPUTS</span></span>

### <span data-ttu-id="af28c-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="af28c-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="af28c-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="af28c-127">NOTES</span></span>

## <span data-ttu-id="af28c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af28c-128">RELATED LINKS</span></span>

