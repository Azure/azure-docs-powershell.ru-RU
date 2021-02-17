---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222372"
---
# <span data-ttu-id="0ff2a-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="0ff2a-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="0ff2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff2a-103">Создайте объект ''Список драйверов'' для ImportExport.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="0ff2a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ff2a-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="0ff2a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff2a-106">Создайте объект DriverList для ImportExport.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="0ff2a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff2a-108">Пример 1. Создание нового списка дисков для задания ImportExport</span><span class="sxs-lookup"><span data-stu-id="0ff2a-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="0ff2a-109">Эти cmdlets create a new DriveList for ImportExport job.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="0ff2a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ff2a-110">PARAMETERS</span></span>

### <span data-ttu-id="0ff2a-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="0ff2a-111">-BitLockerKey</span></span>
<span data-ttu-id="0ff2a-112">Ключ BitLocker, используемый для шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-112">The BitLocker key used to encrypt the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="0ff2a-113">-BytesSucceeded</span></span>
<span data-ttu-id="0ff2a-114">Переданные для диска bytes успешно перенесены.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="0ff2a-115">-CopyStatus</span></span>
<span data-ttu-id="0ff2a-116">Подробное состояние процесса передачи данных.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="0ff2a-117">Это поле не возвращается в ответе, пока диск не находится в состоянии переноса.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="0ff2a-118">-DriveHeaderHash</span></span>
<span data-ttu-id="0ff2a-119">Hash value the drive header (Hash value).</span><span class="sxs-lookup"><span data-stu-id="0ff2a-119">The drive header hash value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="0ff2a-120">-DriveId</span></span>
<span data-ttu-id="0ff2a-121">Серийный номер диска без пробелов.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-121">The drive's hardware serial number, without spaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="0ff2a-122">-ErrorLogUri</span></span>
<span data-ttu-id="0ff2a-123">URI, который указывает на BLOB-проект, содержащий журнал ошибок для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="0ff2a-124">-ManifestFile</span></span>
<span data-ttu-id="0ff2a-125">Относительный путь к файлу манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-125">The relative path of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="0ff2a-126">-ManifestHash</span></span>
<span data-ttu-id="0ff2a-127">С кодируемым кодом MD5 базовой кодировки файла манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="0ff2a-128">-ManifestUri</span></span>
<span data-ttu-id="0ff2a-129">URI, который указывает на BLOB-проект, содержащий файл манифеста диска.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-129">A URI that points to the blob containing the drive manifest file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="0ff2a-130">-PercentComplete</span></span>
<span data-ttu-id="0ff2a-131">Процентное завершения для диска.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-131">Percentage completed for the drive.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-132">-State</span><span class="sxs-lookup"><span data-stu-id="0ff2a-132">-State</span></span>
<span data-ttu-id="0ff2a-133">Текущее состояние диска.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="0ff2a-134">-VerboseLogUri</span></span>
<span data-ttu-id="0ff2a-135">URI, который указывает на BLOB-проект, содержащий подробный журнал для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff2a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff2a-136">CommonParameters</span></span>
<span data-ttu-id="0ff2a-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff2a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff2a-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ff2a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff2a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ff2a-139">INPUTS</span></span>

## <span data-ttu-id="0ff2a-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ff2a-140">OUTPUTS</span></span>

### <span data-ttu-id="0ff2a-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="0ff2a-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="0ff2a-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-142">NOTES</span></span>

<span data-ttu-id="0ff2a-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0ff2a-143">ALIASES</span></span>

## <span data-ttu-id="0ff2a-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ff2a-144">RELATED LINKS</span></span>

