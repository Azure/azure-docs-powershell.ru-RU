---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 500a8e28ceb4eb452d788574b8a80865b5e54b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556168"
---
# <span data-ttu-id="1e5c4-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e5c4-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="1e5c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5c4-103">Возвращает список конфигураций резервных копий.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="1e5c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e5c4-104">SYNTAX</span></span>

### <span data-ttu-id="1e5c4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e5c4-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1e5c4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="1e5c4-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1e5c4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e5c4-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1e5c4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e5c4-108">DESCRIPTION</span></span>
<span data-ttu-id="1e5c4-109">Возвращает список конфигураций резервных копий.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="1e5c4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e5c4-110">EXAMPLES</span></span>

### <span data-ttu-id="1e5c4-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e5c4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="1e5c4-112">Скачайте конфигурацию стека для резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="1e5c4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e5c4-113">PARAMETERS</span></span>

### <span data-ttu-id="1e5c4-114">-Location</span><span class="sxs-lookup"><span data-stu-id="1e5c4-114">-Location</span></span>
<span data-ttu-id="1e5c4-115">Расположение для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5c4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5c4-116">-ResourceGroupName</span></span>
<span data-ttu-id="1e5c4-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="1e5c4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e5c4-118">-ResourceId</span></span>
<span data-ttu-id="1e5c4-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-119">The resource id.</span></span>

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

### <span data-ttu-id="1e5c4-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="1e5c4-120">-Skip</span></span>
<span data-ttu-id="1e5c4-121">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1e5c4-122">-Top</span><span class="sxs-lookup"><span data-stu-id="1e5c4-122">-Top</span></span>
<span data-ttu-id="1e5c4-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1e5c4-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1e5c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5c4-125">CommonParameters</span></span>
<span data-ttu-id="1e5c4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e5c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5c4-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e5c4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5c4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e5c4-128">INPUTS</span></span>

## <span data-ttu-id="1e5c4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e5c4-129">OUTPUTS</span></span>

### <span data-ttu-id="1e5c4-130">Microsoft. AzureStack. Management. Backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="1e5c4-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="1e5c4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e5c4-131">NOTES</span></span>

## <span data-ttu-id="1e5c4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e5c4-132">RELATED LINKS</span></span>

