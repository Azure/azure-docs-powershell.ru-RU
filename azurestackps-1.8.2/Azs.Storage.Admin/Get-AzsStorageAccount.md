---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4ec0639e31df3766550d6f7acc655cd3b5608bf
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076893"
---
# <span data-ttu-id="0ed9c-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0ed9c-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="0ed9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ed9c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed9c-103">Возвращает запрашиваемую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="0ed9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ed9c-104">SYNTAX</span></span>

### <span data-ttu-id="0ed9c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ed9c-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0ed9c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="0ed9c-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0ed9c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ed9c-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="0ed9c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ed9c-108">DESCRIPTION</span></span>
<span data-ttu-id="0ed9c-109">Возвращает запрашиваемую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="0ed9c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ed9c-110">EXAMPLES</span></span>

### <span data-ttu-id="0ed9c-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="0ed9c-111">EXAMPLE 1</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="0ed9c-112">Получение списка учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="0ed9c-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="0ed9c-113">EXAMPLE 2</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="0ed9c-114">Получение сведений об указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="0ed9c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ed9c-115">PARAMETERS</span></span>

### <span data-ttu-id="0ed9c-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="0ed9c-116">-FarmName</span></span>
<span data-ttu-id="0ed9c-117">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-117">Farm Id.</span></span>

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

### <span data-ttu-id="0ed9c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ed9c-118">-Name</span></span>
<span data-ttu-id="0ed9c-119">Внутренний идентификатор учетной записи хранилища, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-119">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed9c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed9c-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ed9c-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-121">Resource group name.</span></span>

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

### <span data-ttu-id="0ed9c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ed9c-122">-ResourceId</span></span>
<span data-ttu-id="0ed9c-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed9c-124">-Сводка</span><span class="sxs-lookup"><span data-stu-id="0ed9c-124">-Summary</span></span>
<span data-ttu-id="0ed9c-125">Возвращается параметр для wheter сводки или подробной информации.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-125">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed9c-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="0ed9c-126">-Skip</span></span>
<span data-ttu-id="0ed9c-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0ed9c-128">-Top</span><span class="sxs-lookup"><span data-stu-id="0ed9c-128">-Top</span></span>
<span data-ttu-id="0ed9c-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0ed9c-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0ed9c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed9c-131">CommonParameters</span></span>
<span data-ttu-id="0ed9c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ed9c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed9c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed9c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed9c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ed9c-134">INPUTS</span></span>

## <span data-ttu-id="0ed9c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ed9c-135">OUTPUTS</span></span>

### <span data-ttu-id="0ed9c-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0ed9c-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="0ed9c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ed9c-137">NOTES</span></span>

## <span data-ttu-id="0ed9c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ed9c-138">RELATED LINKS</span></span>