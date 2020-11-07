---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908833"
---
# <span data-ttu-id="bb341-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="bb341-101">Get-AzsBackup</span></span>

## <span data-ttu-id="bb341-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb341-102">SYNOPSIS</span></span>
<span data-ttu-id="bb341-103">Возвращает резервное копирование из расположения на основе имени.</span><span class="sxs-lookup"><span data-stu-id="bb341-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="bb341-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb341-104">SYNTAX</span></span>

### <span data-ttu-id="bb341-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb341-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb341-106">Получить</span><span class="sxs-lookup"><span data-stu-id="bb341-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bb341-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb341-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="bb341-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="bb341-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bb341-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb341-109">DESCRIPTION</span></span>
<span data-ttu-id="bb341-110">Возвращает резервное копирование из расположения на основе имени.</span><span class="sxs-lookup"><span data-stu-id="bb341-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="bb341-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb341-111">EXAMPLES</span></span>

### <span data-ttu-id="bb341-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bb341-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="bb341-113">Получение сведений sbout всех резервных копий стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="bb341-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="bb341-114">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="bb341-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="bb341-115">Получение сведений для указанной резервной копии стека Azure.</span><span class="sxs-lookup"><span data-stu-id="bb341-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="bb341-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb341-116">PARAMETERS</span></span>

### <span data-ttu-id="bb341-117">-Location</span><span class="sxs-lookup"><span data-stu-id="bb341-117">-Location</span></span>
<span data-ttu-id="bb341-118">Заархивировано расположение.</span><span class="sxs-lookup"><span data-stu-id="bb341-118">Location backed up.</span></span>

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

### <span data-ttu-id="bb341-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb341-119">-Name</span></span>
<span data-ttu-id="bb341-120">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="bb341-120">Name of the backup.</span></span>

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

### <span data-ttu-id="bb341-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="bb341-121">-ParentResource</span></span>
<span data-ttu-id="bb341-122">При передаче места для резервного копирования будет возвращен список всех резервных копий в этом расположении резервной копии.</span><span class="sxs-lookup"><span data-stu-id="bb341-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

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

### <span data-ttu-id="bb341-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb341-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb341-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb341-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="bb341-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb341-125">-ResourceId</span></span>
<span data-ttu-id="bb341-126">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb341-126">The resource id.</span></span>

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

### <span data-ttu-id="bb341-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="bb341-127">-Skip</span></span>
<span data-ttu-id="bb341-128">{{Описание пропуск заполнения}}</span><span class="sxs-lookup"><span data-stu-id="bb341-128">{{Fill Skip Description}}</span></span>

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

### <span data-ttu-id="bb341-129">-Top</span><span class="sxs-lookup"><span data-stu-id="bb341-129">-Top</span></span>
<span data-ttu-id="bb341-130">{{Заливка сверху}}</span><span class="sxs-lookup"><span data-stu-id="bb341-130">{{Fill Top Description}}</span></span>

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

### <span data-ttu-id="bb341-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb341-131">CommonParameters</span></span>
<span data-ttu-id="bb341-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb341-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb341-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb341-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb341-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb341-134">INPUTS</span></span>

## <span data-ttu-id="bb341-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb341-135">OUTPUTS</span></span>

### <span data-ttu-id="bb341-136">Microsoft. AzureStack. Management. Backup. admin. Models. Backup</span><span class="sxs-lookup"><span data-stu-id="bb341-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="bb341-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb341-137">NOTES</span></span>

## <span data-ttu-id="bb341-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb341-138">RELATED LINKS</span></span>

