---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1f3a965d287aa266683636b4b17a8d8954cace8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907573"
---
# <span data-ttu-id="799c9-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="799c9-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="799c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="799c9-102">SYNOPSIS</span></span>
<span data-ttu-id="799c9-103">Возвращает список конфигураций резервных копий.</span><span class="sxs-lookup"><span data-stu-id="799c9-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="799c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="799c9-104">SYNTAX</span></span>

### <span data-ttu-id="799c9-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="799c9-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="799c9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="799c9-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="799c9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="799c9-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="799c9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="799c9-108">DESCRIPTION</span></span>
<span data-ttu-id="799c9-109">Возвращает список конфигураций резервных копий.</span><span class="sxs-lookup"><span data-stu-id="799c9-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="799c9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="799c9-110">EXAMPLES</span></span>

### <span data-ttu-id="799c9-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="799c9-111">EXAMPLE 1</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="799c9-112">Скачайте конфигурацию стека для резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="799c9-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="799c9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="799c9-113">PARAMETERS</span></span>

### <span data-ttu-id="799c9-114">-Location</span><span class="sxs-lookup"><span data-stu-id="799c9-114">-Location</span></span>
<span data-ttu-id="799c9-115">Расположение для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="799c9-115">Backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799c9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="799c9-116">-ResourceGroupName</span></span>
<span data-ttu-id="799c9-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="799c9-117">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799c9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="799c9-118">-ResourceId</span></span>
<span data-ttu-id="799c9-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="799c9-119">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="799c9-120">-Top</span><span class="sxs-lookup"><span data-stu-id="799c9-120">-Top</span></span>
<span data-ttu-id="799c9-121">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="799c9-121">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="799c9-122">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="799c9-122">Applies after the -Skip parameter.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799c9-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="799c9-123">-Skip</span></span>
<span data-ttu-id="799c9-124">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="799c9-124">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799c9-125">CommonParameters</span></span>
<span data-ttu-id="799c9-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="799c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799c9-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="799c9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799c9-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="799c9-128">INPUTS</span></span>

## <span data-ttu-id="799c9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="799c9-129">OUTPUTS</span></span>

### <span data-ttu-id="799c9-130">Microsoft. AzureStack. Management. Backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="799c9-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="799c9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="799c9-131">NOTES</span></span>

## <span data-ttu-id="799c9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="799c9-132">RELATED LINKS</span></span>
