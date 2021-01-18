---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: e5aaff4f915143e2e7695c9f650aed6fb01ba389
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504593"
---
# <span data-ttu-id="1c95c-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="1c95c-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="1c95c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c95c-102">SYNOPSIS</span></span>
<span data-ttu-id="1c95c-103">Получает содержимое файла в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c95c-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="1c95c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c95c-104">SYNTAX</span></span>

### <span data-ttu-id="1c95c-105">PreviewFileContent (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c95c-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c95c-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="1c95c-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c95c-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="1c95c-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c95c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c95c-108">DESCRIPTION</span></span>
<span data-ttu-id="1c95c-109">**Cmdlet Get-AzDataLakeStoreItemContent** получает содержимое файла в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c95c-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="1c95c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c95c-110">EXAMPLES</span></span>

### <span data-ttu-id="1c95c-111">Пример 1. Просмотр содержимого файла</span><span class="sxs-lookup"><span data-stu-id="1c95c-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="1c95c-112">Эта команда возвращает содержимое файла, MyFile.txt учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="1c95c-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="1c95c-113">Пример 2. Получить первые две строки файла</span><span class="sxs-lookup"><span data-stu-id="1c95c-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="1c95c-114">Эта команда получает две первых строки в файле, разделенных строками, MyFile.txt в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="1c95c-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="1c95c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c95c-115">PARAMETERS</span></span>

### <span data-ttu-id="1c95c-116">-Account</span><span class="sxs-lookup"><span data-stu-id="1c95c-116">-Account</span></span>
<span data-ttu-id="1c95c-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c95c-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c95c-118">-DefaultProfile</span></span>
<span data-ttu-id="1c95c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c95c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-120">-Кодировидная кодировидная</span><span class="sxs-lookup"><span data-stu-id="1c95c-120">-Encoding</span></span>
<span data-ttu-id="1c95c-121">Определяет кодию элемента, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="1c95c-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="1c95c-122">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="1c95c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1c95c-123">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="1c95c-123">Unknown</span></span>
- <span data-ttu-id="1c95c-124">Строка</span><span class="sxs-lookup"><span data-stu-id="1c95c-124">String</span></span>
- <span data-ttu-id="1c95c-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="1c95c-125">Unicode</span></span>
- <span data-ttu-id="1c95c-126">Byte</span><span class="sxs-lookup"><span data-stu-id="1c95c-126">Byte</span></span>
- <span data-ttu-id="1c95c-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="1c95c-127">BigEndianUnicode</span></span>
- <span data-ttu-id="1c95c-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="1c95c-128">UTF8</span></span>
- <span data-ttu-id="1c95c-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="1c95c-129">UTF7</span></span>
- <span data-ttu-id="1c95c-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="1c95c-130">Ascii</span></span>
- <span data-ttu-id="1c95c-131">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1c95c-131">Default</span></span>
- <span data-ttu-id="1c95c-132">Oem</span><span class="sxs-lookup"><span data-stu-id="1c95c-132">Oem</span></span>
- <span data-ttu-id="1c95c-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="1c95c-133">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="1c95c-134">-Force</span></span>
<span data-ttu-id="1c95c-135">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1c95c-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-136">-Head</span><span class="sxs-lookup"><span data-stu-id="1c95c-136">-Head</span></span>
<span data-ttu-id="1c95c-137">Количество строк (с делегированной новой строкой) от начала файла до предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="1c95c-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="1c95c-138">Если в первых 4 Мбит/с данных не было новой линии, возвращаются только эти данные.</span><span class="sxs-lookup"><span data-stu-id="1c95c-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-139">-Length</span><span class="sxs-lookup"><span data-stu-id="1c95c-139">-Length</span></span>
<span data-ttu-id="1c95c-140">Определяет длину вбайтов содержимого.</span><span class="sxs-lookup"><span data-stu-id="1c95c-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="1c95c-141">-Offset</span></span>
<span data-ttu-id="1c95c-142">Определяет количествобайтов, которые нужно пропустить в файле перед получением содержимого.</span><span class="sxs-lookup"><span data-stu-id="1c95c-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-143">-Path</span><span class="sxs-lookup"><span data-stu-id="1c95c-143">-Path</span></span>
<span data-ttu-id="1c95c-144">Путь к файлу, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="1c95c-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="1c95c-145">-Tail</span></span>
<span data-ttu-id="1c95c-146">Количество строк (с делегированной новой строкой) в конце файла для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="1c95c-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="1c95c-147">Если в первых 4 Мбит/с данных не было новой линии, возвращаются только эти данные.</span><span class="sxs-lookup"><span data-stu-id="1c95c-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c95c-148">-Confirm</span></span>
<span data-ttu-id="1c95c-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1c95c-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c95c-150">-WhatIf</span></span>
<span data-ttu-id="1c95c-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c95c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c95c-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c95c-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c95c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c95c-153">CommonParameters</span></span>
<span data-ttu-id="1c95c-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c95c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c95c-155">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c95c-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c95c-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c95c-156">INPUTS</span></span>

### <span data-ttu-id="1c95c-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1c95c-157">System.String</span></span>

### <span data-ttu-id="1c95c-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1c95c-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1c95c-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1c95c-159">System.Int32</span></span>

### <span data-ttu-id="1c95c-160">System.Int64</span><span class="sxs-lookup"><span data-stu-id="1c95c-160">System.Int64</span></span>

### <span data-ttu-id="1c95c-161">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="1c95c-161">System.Text.Encoding</span></span>

### <span data-ttu-id="1c95c-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1c95c-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1c95c-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c95c-163">OUTPUTS</span></span>

### <span data-ttu-id="1c95c-164">System.Byte</span><span class="sxs-lookup"><span data-stu-id="1c95c-164">System.Byte</span></span>

### <span data-ttu-id="1c95c-165">System.String</span><span class="sxs-lookup"><span data-stu-id="1c95c-165">System.String</span></span>

## <span data-ttu-id="1c95c-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c95c-166">NOTES</span></span>

## <span data-ttu-id="1c95c-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c95c-167">RELATED LINKS</span></span>
