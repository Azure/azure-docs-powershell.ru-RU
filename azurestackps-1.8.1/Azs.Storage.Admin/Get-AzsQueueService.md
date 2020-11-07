---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d6bd071f4e1d61fdf2d682459dbe8baa57b5276
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909037"
---
# <span data-ttu-id="86f60-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="86f60-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="86f60-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86f60-102">SYNOPSIS</span></span>
<span data-ttu-id="86f60-103">Возвращает службу очереди.</span><span class="sxs-lookup"><span data-stu-id="86f60-103">Returns the queue service.</span></span>

## <span data-ttu-id="86f60-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86f60-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="86f60-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86f60-105">DESCRIPTION</span></span>
<span data-ttu-id="86f60-106">Возвращает службу очереди.</span><span class="sxs-lookup"><span data-stu-id="86f60-106">Returns the queue service.</span></span>

## <span data-ttu-id="86f60-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86f60-107">EXAMPLES</span></span>

### <span data-ttu-id="86f60-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="86f60-108">EXAMPLE 1</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="86f60-109">Получение службы очереди.</span><span class="sxs-lookup"><span data-stu-id="86f60-109">Get the queue service.</span></span>

## <span data-ttu-id="86f60-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86f60-110">PARAMETERS</span></span>

### <span data-ttu-id="86f60-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="86f60-111">-FarmName</span></span>
<span data-ttu-id="86f60-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="86f60-112">Farm Id.</span></span>

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

### <span data-ttu-id="86f60-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f60-113">-ResourceGroupName</span></span>
<span data-ttu-id="86f60-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86f60-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f60-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f60-115">CommonParameters</span></span>
<span data-ttu-id="86f60-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86f60-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f60-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f60-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f60-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86f60-118">INPUTS</span></span>

## <span data-ttu-id="86f60-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86f60-119">OUTPUTS</span></span>

### <span data-ttu-id="86f60-120">Microsoft. AzureStack. Management. Storage. admin. Models. QueueService</span><span class="sxs-lookup"><span data-stu-id="86f60-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="86f60-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="86f60-121">NOTES</span></span>

## <span data-ttu-id="86f60-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86f60-122">RELATED LINKS</span></span>
