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
ms.locfileid: "93720101"
---
# <span data-ttu-id="839ac-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="839ac-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="839ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="839ac-102">SYNOPSIS</span></span>
<span data-ttu-id="839ac-103">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="839ac-103">Get the list of update locations.</span></span>

## <span data-ttu-id="839ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="839ac-104">SYNTAX</span></span>

### <span data-ttu-id="839ac-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="839ac-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="839ac-106">Получить</span><span class="sxs-lookup"><span data-stu-id="839ac-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="839ac-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="839ac-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="839ac-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="839ac-108">DESCRIPTION</span></span>
<span data-ttu-id="839ac-109">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="839ac-109">Get the list of update locations.</span></span> <span data-ttu-id="839ac-110">Возвращенные расположения можно использовать для получения доступных обновлений в определенном расположении с помощью Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="839ac-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="839ac-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="839ac-111">EXAMPLES</span></span>

### <span data-ttu-id="839ac-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="839ac-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="839ac-113">Получите список местоположений обновлений.</span><span class="sxs-lookup"><span data-stu-id="839ac-113">Get the list of update locations.</span></span>

## <span data-ttu-id="839ac-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="839ac-114">PARAMETERS</span></span>

### <span data-ttu-id="839ac-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="839ac-115">-Name</span></span>
<span data-ttu-id="839ac-116">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="839ac-116">The name of the update location.</span></span>

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

### <span data-ttu-id="839ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="839ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="839ac-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="839ac-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="839ac-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="839ac-119">-ResourceId</span></span>
<span data-ttu-id="839ac-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="839ac-120">The resource id.</span></span>

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

### <span data-ttu-id="839ac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839ac-121">CommonParameters</span></span>
<span data-ttu-id="839ac-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="839ac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839ac-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839ac-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839ac-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="839ac-124">INPUTS</span></span>

## <span data-ttu-id="839ac-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="839ac-125">OUTPUTS</span></span>

### <span data-ttu-id="839ac-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="839ac-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="839ac-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="839ac-127">NOTES</span></span>

## <span data-ttu-id="839ac-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="839ac-128">RELATED LINKS</span></span>

