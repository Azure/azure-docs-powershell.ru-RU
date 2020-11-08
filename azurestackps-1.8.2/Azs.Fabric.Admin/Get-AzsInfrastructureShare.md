---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076961"
---
# <span data-ttu-id="908c3-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="908c3-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="908c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="908c3-102">SYNOPSIS</span></span>
<span data-ttu-id="908c3-103">Возвращает список всех файловых ресурсов структуры в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="908c3-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="908c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="908c3-104">SYNTAX</span></span>

### <span data-ttu-id="908c3-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="908c3-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="908c3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="908c3-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="908c3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="908c3-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="908c3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="908c3-108">DESCRIPTION</span></span>
<span data-ttu-id="908c3-109">Возвращает список всех файловых ресурсов структуры в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="908c3-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="908c3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="908c3-110">EXAMPLES</span></span>

### <span data-ttu-id="908c3-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="908c3-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="908c3-112">Возвращает список всех общих файловых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="908c3-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="908c3-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="908c3-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="908c3-114">Возвращает общую файловую систему на основе имени.</span><span class="sxs-lookup"><span data-stu-id="908c3-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="908c3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="908c3-115">PARAMETERS</span></span>

### <span data-ttu-id="908c3-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="908c3-116">-Name</span></span>
<span data-ttu-id="908c3-117">Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="908c3-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="908c3-118">-Location</span><span class="sxs-lookup"><span data-stu-id="908c3-118">-Location</span></span>
<span data-ttu-id="908c3-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="908c3-119">Location of the resource.</span></span>

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

### <span data-ttu-id="908c3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908c3-120">-ResourceGroupName</span></span>
<span data-ttu-id="908c3-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="908c3-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="908c3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="908c3-122">-ResourceId</span></span>
<span data-ttu-id="908c3-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="908c3-123">The resource id.</span></span>

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

### <span data-ttu-id="908c3-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="908c3-124">-Filter</span></span>
<span data-ttu-id="908c3-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="908c3-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="908c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908c3-126">CommonParameters</span></span>
<span data-ttu-id="908c3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="908c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908c3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908c3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908c3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="908c3-129">INPUTS</span></span>

## <span data-ttu-id="908c3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="908c3-130">OUTPUTS</span></span>

### <span data-ttu-id="908c3-131">Microsoft. AzureStack. Management. Fabric. admin. Models. \ мои</span><span class="sxs-lookup"><span data-stu-id="908c3-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="908c3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="908c3-132">NOTES</span></span>

## <span data-ttu-id="908c3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="908c3-133">RELATED LINKS</span></span>
