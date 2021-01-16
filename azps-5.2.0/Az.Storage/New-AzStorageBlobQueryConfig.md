---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404119"
---
# <span data-ttu-id="39d4b-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="39d4b-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="39d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="39d4b-103">Создает объект конфигурации запроса BLOB-объектов, который можно использовать в get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="39d4b-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="39d4b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39d4b-104">SYNTAX</span></span>

### <span data-ttu-id="39d4b-105">CSV (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39d4b-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="39d4b-106">Json</span><span class="sxs-lookup"><span data-stu-id="39d4b-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="39d4b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39d4b-107">DESCRIPTION</span></span>
<span data-ttu-id="39d4b-108">**Новый-AzStorageBlobQueryConfig** создает объект конфигурации BLOB-запросов, который можно использовать в Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="39d4b-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="39d4b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39d4b-109">EXAMPLES</span></span>

### <span data-ttu-id="39d4b-110">Пример 1. Создание настраиваемых BLOB-запросов и запрос для BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="39d4b-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="39d4b-111">Эта команда сначала создает объект конфигурации ввода в качестве CSV-объекта, а выходной объект конфигурации — в качестве json, а затем запросит BLOB-объект с использованием двух конфигураций.</span><span class="sxs-lookup"><span data-stu-id="39d4b-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="39d4b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39d4b-112">PARAMETERS</span></span>

### <span data-ttu-id="39d4b-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="39d4b-113">-AsCsv</span></span>
<span data-ttu-id="39d4b-114">Указать, что нужно создать конфигурацию запроса BLOB-то для CSV-запроса.</span><span class="sxs-lookup"><span data-stu-id="39d4b-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="39d4b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39d4b-115">-AsJob</span></span>
<span data-ttu-id="39d4b-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="39d4b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39d4b-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="39d4b-117">-AsJson</span></span>
<span data-ttu-id="39d4b-118">Указать, что нужно создать конфигурацию запроса BLOB-то для Json.</span><span class="sxs-lookup"><span data-stu-id="39d4b-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="39d4b-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="39d4b-119">-ColumnSeparator</span></span>
<span data-ttu-id="39d4b-120">Необязательный.</span><span class="sxs-lookup"><span data-stu-id="39d4b-120">Optional.</span></span>
<span data-ttu-id="39d4b-121">Строка, используемая для разных столбцов.</span><span class="sxs-lookup"><span data-stu-id="39d4b-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="39d4b-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="39d4b-122">-EscapeCharacter</span></span>
<span data-ttu-id="39d4b-123">Необязательный.</span><span class="sxs-lookup"><span data-stu-id="39d4b-123">Optional.</span></span>
<span data-ttu-id="39d4b-124">Символ, используемый в качестве escape-символа.</span><span class="sxs-lookup"><span data-stu-id="39d4b-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="39d4b-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="39d4b-125">-HasHeader</span></span>
<span data-ttu-id="39d4b-126">Необязательный.</span><span class="sxs-lookup"><span data-stu-id="39d4b-126">Optional.</span></span>
<span data-ttu-id="39d4b-127">Указать, что данные должны быть с заглавами.</span><span class="sxs-lookup"><span data-stu-id="39d4b-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="39d4b-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="39d4b-128">-QuotationCharacter</span></span>
<span data-ttu-id="39d4b-129">Необязательный.</span><span class="sxs-lookup"><span data-stu-id="39d4b-129">Optional.</span></span>
<span data-ttu-id="39d4b-130">Символ, используемый для кавычка определенного поля.</span><span class="sxs-lookup"><span data-stu-id="39d4b-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="39d4b-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="39d4b-131">-RecordSeparator</span></span>
<span data-ttu-id="39d4b-132">Необязательный.</span><span class="sxs-lookup"><span data-stu-id="39d4b-132">Optional.</span></span>
<span data-ttu-id="39d4b-133">Строка, используемая для разных записей.</span><span class="sxs-lookup"><span data-stu-id="39d4b-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="39d4b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d4b-134">CommonParameters</span></span>
<span data-ttu-id="39d4b-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d4b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d4b-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d4b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d4b-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39d4b-137">INPUTS</span></span>

### <span data-ttu-id="39d4b-138">Нет</span><span class="sxs-lookup"><span data-stu-id="39d4b-138">None</span></span>

## <span data-ttu-id="39d4b-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39d4b-139">OUTPUTS</span></span>

### <span data-ttu-id="39d4b-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d4b-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="39d4b-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39d4b-141">NOTES</span></span>

## <span data-ttu-id="39d4b-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39d4b-142">RELATED LINKS</span></span>
