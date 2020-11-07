---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908954"
---
# <span data-ttu-id="2541a-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="2541a-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="2541a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2541a-102">SYNOPSIS</span></span>
<span data-ttu-id="2541a-103">Получение списка запусков обновлений.</span><span class="sxs-lookup"><span data-stu-id="2541a-103">Get the list of update runs.</span></span>

## <span data-ttu-id="2541a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2541a-104">SYNTAX</span></span>

### <span data-ttu-id="2541a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2541a-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2541a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="2541a-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2541a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2541a-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2541a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2541a-108">DESCRIPTION</span></span>
<span data-ttu-id="2541a-109">Получение списка запусков обновлений.</span><span class="sxs-lookup"><span data-stu-id="2541a-109">Get the list of update runs.</span></span> <span data-ttu-id="2541a-110">Экземпляры возвращенных объектов UpdateRun можно передавать на перезапуск (AzsUpdateRun), если это применимо.</span><span class="sxs-lookup"><span data-stu-id="2541a-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="2541a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2541a-111">EXAMPLES</span></span>

### <span data-ttu-id="2541a-112">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="2541a-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="2541a-113">Получение списка всех попыток применения определенного обновления.</span><span class="sxs-lookup"><span data-stu-id="2541a-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="2541a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2541a-114">PARAMETERS</span></span>

### <span data-ttu-id="2541a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2541a-115">-Name</span></span>
<span data-ttu-id="2541a-116">Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="2541a-116">Update run identifier.</span></span>

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

### <span data-ttu-id="2541a-117">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="2541a-117">-UpdateName</span></span>
<span data-ttu-id="2541a-118">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="2541a-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2541a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2541a-119">-Location</span></span>
<span data-ttu-id="2541a-120">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="2541a-120">The name of the update location.</span></span>

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

### <span data-ttu-id="2541a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2541a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2541a-122">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="2541a-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2541a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2541a-123">-ResourceId</span></span>
<span data-ttu-id="2541a-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2541a-124">The resource id.</span></span>

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

### <span data-ttu-id="2541a-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="2541a-125">-Skip</span></span>
<span data-ttu-id="2541a-126">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="2541a-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2541a-127">-Top</span><span class="sxs-lookup"><span data-stu-id="2541a-127">-Top</span></span>
<span data-ttu-id="2541a-128">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="2541a-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2541a-129">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="2541a-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2541a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2541a-130">CommonParameters</span></span>
<span data-ttu-id="2541a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2541a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2541a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2541a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2541a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2541a-133">INPUTS</span></span>

## <span data-ttu-id="2541a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2541a-134">OUTPUTS</span></span>

### <span data-ttu-id="2541a-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="2541a-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="2541a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2541a-136">NOTES</span></span>

## <span data-ttu-id="2541a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2541a-137">RELATED LINKS</span></span>
