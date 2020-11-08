---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236687"
---
# <span data-ttu-id="8ef89-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="8ef89-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="8ef89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ef89-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef89-103">Создайте объект DriverList для ImportExport.</span><span class="sxs-lookup"><span data-stu-id="8ef89-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="8ef89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ef89-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ef89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ef89-105">DESCRIPTION</span></span>
<span data-ttu-id="8ef89-106">Создайте объект DriverList для ImportExport.</span><span class="sxs-lookup"><span data-stu-id="8ef89-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="8ef89-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ef89-107">EXAMPLES</span></span>

### <span data-ttu-id="8ef89-108">Пример 1: создание нового DriveList для задания ImportExport</span><span class="sxs-lookup"><span data-stu-id="8ef89-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="8ef89-109">Эти командлеты создают новую DriveList для задания ImportExport.</span><span class="sxs-lookup"><span data-stu-id="8ef89-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="8ef89-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ef89-110">PARAMETERS</span></span>

### <span data-ttu-id="8ef89-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="8ef89-111">-BitLockerKey</span></span>
<span data-ttu-id="8ef89-112">Ключ BitLocker, используемый для шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="8ef89-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="8ef89-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="8ef89-113">-BytesSucceeded</span></span>
<span data-ttu-id="8ef89-114">Байт успешно переданы на диск.</span><span class="sxs-lookup"><span data-stu-id="8ef89-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="8ef89-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="8ef89-115">-CopyStatus</span></span>
<span data-ttu-id="8ef89-116">Подробные сведения о состоянии процесса передачи данных.</span><span class="sxs-lookup"><span data-stu-id="8ef89-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="8ef89-117">Это поле не возвращается в ответе до тех пор, пока диск не находится в состоянии перепередачи.</span><span class="sxs-lookup"><span data-stu-id="8ef89-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="8ef89-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="8ef89-118">-DriveHeaderHash</span></span>
<span data-ttu-id="8ef89-119">Хэш-значение заголовка диска.</span><span class="sxs-lookup"><span data-stu-id="8ef89-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="8ef89-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="8ef89-120">-DriveId</span></span>
<span data-ttu-id="8ef89-121">Серийный номер устройства, без пробелов.</span><span class="sxs-lookup"><span data-stu-id="8ef89-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="8ef89-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="8ef89-122">-ErrorLogUri</span></span>
<span data-ttu-id="8ef89-123">Универсальный код ресурса (URI), который указывает на большой двоичный объект, содержащий журнал ошибок для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="8ef89-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="8ef89-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="8ef89-124">-ManifestFile</span></span>
<span data-ttu-id="8ef89-125">Относительный путь к файлу манифеста на диске.</span><span class="sxs-lookup"><span data-stu-id="8ef89-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="8ef89-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="8ef89-126">-ManifestHash</span></span>
<span data-ttu-id="8ef89-127">Хеш MD5 для файла манифеста на диске, закодированный Base16.</span><span class="sxs-lookup"><span data-stu-id="8ef89-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="8ef89-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="8ef89-128">-ManifestUri</span></span>
<span data-ttu-id="8ef89-129">Универсальный код ресурса (URI), который указывает на большой двоичный объект, который содержит файл манифеста диска.</span><span class="sxs-lookup"><span data-stu-id="8ef89-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="8ef89-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="8ef89-130">-PercentComplete</span></span>
<span data-ttu-id="8ef89-131">Процент завершения для диска.</span><span class="sxs-lookup"><span data-stu-id="8ef89-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="8ef89-132">-State</span><span class="sxs-lookup"><span data-stu-id="8ef89-132">-State</span></span>
<span data-ttu-id="8ef89-133">Текущее состояние диска.</span><span class="sxs-lookup"><span data-stu-id="8ef89-133">The drive's current state.</span></span>

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

### <span data-ttu-id="8ef89-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="8ef89-134">-VerboseLogUri</span></span>
<span data-ttu-id="8ef89-135">URI, указывающий на большой двоичный объект, содержащий подробный журнал для операции передачи данных.</span><span class="sxs-lookup"><span data-stu-id="8ef89-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="8ef89-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef89-136">CommonParameters</span></span>
<span data-ttu-id="8ef89-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ef89-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef89-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ef89-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef89-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ef89-139">INPUTS</span></span>

## <span data-ttu-id="8ef89-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ef89-140">OUTPUTS</span></span>

### <span data-ttu-id="8ef89-141">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. Api20161101. IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="8ef89-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="8ef89-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ef89-142">NOTES</span></span>

<span data-ttu-id="8ef89-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="8ef89-143">ALIASES</span></span>

## <span data-ttu-id="8ef89-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ef89-144">RELATED LINKS</span></span>

