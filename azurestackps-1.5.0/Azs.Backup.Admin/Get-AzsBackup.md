---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb306ed03cb9ab1f06209345474b2ef196d9e1d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555968"
---
# <span data-ttu-id="4e5bb-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="4e5bb-101">Get-AzsBackup</span></span>

## <span data-ttu-id="4e5bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5bb-103">Возвращает резервное копирование из расположения на основе имени.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="4e5bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e5bb-104">SYNTAX</span></span>

### <span data-ttu-id="4e5bb-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e5bb-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e5bb-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4e5bb-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4e5bb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5bb-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="4e5bb-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="4e5bb-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4e5bb-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e5bb-109">DESCRIPTION</span></span>
<span data-ttu-id="4e5bb-110">Возвращает резервное копирование из расположения на основе имени.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="4e5bb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e5bb-111">EXAMPLES</span></span>

### <span data-ttu-id="4e5bb-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4e5bb-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="4e5bb-113">Получение сведений обо всех резервных копиях стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="4e5bb-114">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4e5bb-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="4e5bb-115">Получение сведений об указанной резервной копии стека Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="4e5bb-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e5bb-116">PARAMETERS</span></span>

### <span data-ttu-id="4e5bb-117">-Location</span><span class="sxs-lookup"><span data-stu-id="4e5bb-117">-Location</span></span>
<span data-ttu-id="4e5bb-118">Заархивировано расположение.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-118">Location backed up.</span></span>

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

### <span data-ttu-id="4e5bb-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e5bb-119">-Name</span></span>
<span data-ttu-id="4e5bb-120">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-120">Name of the backup.</span></span>

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

### <span data-ttu-id="4e5bb-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="4e5bb-121">-ParentResource</span></span>
<span data-ttu-id="4e5bb-122">При передаче места для резервного копирования будет возвращен список всех резервных копий в этом расположении резервной копии.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e5bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e5bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="4e5bb-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="4e5bb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5bb-125">-ResourceId</span></span>
<span data-ttu-id="4e5bb-126">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-126">The resource id.</span></span>

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

### <span data-ttu-id="4e5bb-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="4e5bb-127">-Skip</span></span>
<span data-ttu-id="4e5bb-128">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-128">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5bb-129">-Top</span><span class="sxs-lookup"><span data-stu-id="4e5bb-129">-Top</span></span>
<span data-ttu-id="4e5bb-130">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4e5bb-131">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-131">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5bb-132">CommonParameters</span></span>
<span data-ttu-id="4e5bb-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e5bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5bb-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e5bb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5bb-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e5bb-135">INPUTS</span></span>

## <span data-ttu-id="4e5bb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e5bb-136">OUTPUTS</span></span>

### <span data-ttu-id="4e5bb-137">Microsoft. AzureStack. Management. Backup. admin. Models. Backup</span><span class="sxs-lookup"><span data-stu-id="4e5bb-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="4e5bb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e5bb-138">NOTES</span></span>

## <span data-ttu-id="4e5bb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e5bb-139">RELATED LINKS</span></span>

