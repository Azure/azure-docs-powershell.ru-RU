---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 646ee96dec361ac6318b4cfe48b80ec4c3686321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907598"
---
# <span data-ttu-id="98f9a-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="98f9a-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="98f9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="98f9a-103">Возвращает список определений метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="98f9a-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="98f9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98f9a-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="98f9a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f9a-105">DESCRIPTION</span></span>
<span data-ttu-id="98f9a-106">Возвращает список определений метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="98f9a-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="98f9a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98f9a-107">EXAMPLES</span></span>

### <span data-ttu-id="98f9a-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98f9a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="98f9a-109">Получение списка определений метрик для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="98f9a-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="98f9a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98f9a-110">PARAMETERS</span></span>

### <span data-ttu-id="98f9a-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="98f9a-111">-FarmName</span></span>
<span data-ttu-id="98f9a-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="98f9a-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f9a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98f9a-113">-Name</span></span>
<span data-ttu-id="98f9a-114">Имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="98f9a-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f9a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f9a-115">-ResourceGroupName</span></span>
<span data-ttu-id="98f9a-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98f9a-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f9a-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="98f9a-117">-Skip</span></span>
<span data-ttu-id="98f9a-118">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="98f9a-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f9a-119">-Top</span><span class="sxs-lookup"><span data-stu-id="98f9a-119">-Top</span></span>
<span data-ttu-id="98f9a-120">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="98f9a-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="98f9a-121">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="98f9a-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f9a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f9a-122">CommonParameters</span></span>
<span data-ttu-id="98f9a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98f9a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f9a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f9a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f9a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98f9a-125">INPUTS</span></span>

## <span data-ttu-id="98f9a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f9a-126">OUTPUTS</span></span>

### <span data-ttu-id="98f9a-127">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="98f9a-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="98f9a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="98f9a-128">NOTES</span></span>

## <span data-ttu-id="98f9a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98f9a-129">RELATED LINKS</span></span>

