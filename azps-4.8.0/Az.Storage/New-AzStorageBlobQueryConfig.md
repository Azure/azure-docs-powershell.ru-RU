---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243798"
---
# <span data-ttu-id="73c04-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="73c04-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="73c04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73c04-102">SYNOPSIS</span></span>
<span data-ttu-id="73c04-103">Создает объект конфигурации запроса BLOB, который можно использовать в Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="73c04-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="73c04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73c04-104">SYNTAX</span></span>

### <span data-ttu-id="73c04-105">CSV (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73c04-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="73c04-106">JSON</span><span class="sxs-lookup"><span data-stu-id="73c04-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="73c04-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73c04-107">DESCRIPTION</span></span>
<span data-ttu-id="73c04-108">Командлет **New-AzStorageBlobQueryConfig** создает объект конфигурации запроса BLOB, который можно использовать в Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="73c04-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="73c04-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73c04-109">EXAMPLES</span></span>

### <span data-ttu-id="73c04-110">Пример 1: Создание запроса на BLOB-объект и запрос большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="73c04-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="73c04-111">Эта команда сначала создает объект конфигурации ввода как CSV-файл, а выходной объект конфигурации — в формате JSON, а затем с помощью двух конфигураций для запроса BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="73c04-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="73c04-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73c04-112">PARAMETERS</span></span>

### <span data-ttu-id="73c04-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="73c04-113">-AsCsv</span></span>
<span data-ttu-id="73c04-114">Укажите, чтобы создать конфигурацию запроса BLOB для CSV.</span><span class="sxs-lookup"><span data-stu-id="73c04-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c04-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73c04-115">-AsJob</span></span>
<span data-ttu-id="73c04-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="73c04-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c04-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="73c04-117">-AsJson</span></span>
<span data-ttu-id="73c04-118">Укажите, чтобы создать конфигурацию запроса BLOB-объектов для JSON.</span><span class="sxs-lookup"><span data-stu-id="73c04-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c04-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="73c04-119">-ColumnSeparator</span></span>
<span data-ttu-id="73c04-120">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="73c04-120">Optional.</span></span>
<span data-ttu-id="73c04-121">Строка, используемая для разделения столбцов.</span><span class="sxs-lookup"><span data-stu-id="73c04-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c04-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="73c04-122">-EscapeCharacter</span></span>
<span data-ttu-id="73c04-123">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="73c04-123">Optional.</span></span>
<span data-ttu-id="73c04-124">Символ, используемый в качестве escape-символа.</span><span class="sxs-lookup"><span data-stu-id="73c04-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c04-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="73c04-125">-HasHeader</span></span>
<span data-ttu-id="73c04-126">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="73c04-126">Optional.</span></span>
<span data-ttu-id="73c04-127">Укажите, какие данные содержат заголовки.</span><span class="sxs-lookup"><span data-stu-id="73c04-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c04-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="73c04-128">-QuotationCharacter</span></span>
<span data-ttu-id="73c04-129">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="73c04-129">Optional.</span></span>
<span data-ttu-id="73c04-130">Символ, используемый для заключения определенного поля в кавычки.</span><span class="sxs-lookup"><span data-stu-id="73c04-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c04-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="73c04-131">-RecordSeparator</span></span>
<span data-ttu-id="73c04-132">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="73c04-132">Optional.</span></span>
<span data-ttu-id="73c04-133">Строка, используемая для разделения записей.</span><span class="sxs-lookup"><span data-stu-id="73c04-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="73c04-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c04-134">CommonParameters</span></span>
<span data-ttu-id="73c04-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73c04-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c04-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c04-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c04-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73c04-137">INPUTS</span></span>

### <span data-ttu-id="73c04-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="73c04-138">None</span></span>

## <span data-ttu-id="73c04-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73c04-139">OUTPUTS</span></span>

### <span data-ttu-id="73c04-140">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="73c04-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="73c04-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="73c04-141">NOTES</span></span>

## <span data-ttu-id="73c04-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73c04-142">RELATED LINKS</span></span>
