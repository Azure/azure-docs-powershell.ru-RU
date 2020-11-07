---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 3da97a14049671f8fff8bc03f7f32609f9b86984
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733754"
---
# <span data-ttu-id="213c7-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="213c7-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="213c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="213c7-102">SYNOPSIS</span></span>
<span data-ttu-id="213c7-103">Получает содержимое файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="213c7-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="213c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="213c7-104">SYNTAX</span></span>

### <span data-ttu-id="213c7-105">Предварительный просмотр содержимого файла (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="213c7-105">Preview file content (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="213c7-106">Просмотр строк файла из заголовка файла</span><span class="sxs-lookup"><span data-stu-id="213c7-106">Preview file rows from the head of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="213c7-107">Просмотр строк файла из хвоста файла</span><span class="sxs-lookup"><span data-stu-id="213c7-107">Preview file rows from the tail of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="213c7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="213c7-108">DESCRIPTION</span></span>
<span data-ttu-id="213c7-109">Командлет **Get-AzureRmDataLakeStoreItemContent** получает содержимое файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="213c7-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="213c7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="213c7-110">EXAMPLES</span></span>

### <span data-ttu-id="213c7-111">Пример 1: получение содержимого файла</span><span class="sxs-lookup"><span data-stu-id="213c7-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="213c7-112">Эта команда получает содержимое файла MyFile.txt в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="213c7-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="213c7-113">Пример 2: получение первых двух строк файла</span><span class="sxs-lookup"><span data-stu-id="213c7-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="213c7-114">Эта команда получает первые две строки, разделенные строками в файле, MyFile.txt в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="213c7-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="213c7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="213c7-115">PARAMETERS</span></span>

### <span data-ttu-id="213c7-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="213c7-116">-Account</span></span>
<span data-ttu-id="213c7-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="213c7-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="213c7-118">-Encoding</span><span class="sxs-lookup"><span data-stu-id="213c7-118">-Encoding</span></span>
<span data-ttu-id="213c7-119">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="213c7-119">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="213c7-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="213c7-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="213c7-121">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="213c7-121">Unknown</span></span>
- <span data-ttu-id="213c7-122">Подстрок</span><span class="sxs-lookup"><span data-stu-id="213c7-122">String</span></span>
- <span data-ttu-id="213c7-123">Стандарт</span><span class="sxs-lookup"><span data-stu-id="213c7-123">Unicode</span></span>
- <span data-ttu-id="213c7-124">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="213c7-124">Byte</span></span>
- <span data-ttu-id="213c7-125">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="213c7-125">BigEndianUnicode</span></span>
- <span data-ttu-id="213c7-126">UTF8</span><span class="sxs-lookup"><span data-stu-id="213c7-126">UTF8</span></span>
- <span data-ttu-id="213c7-127">UTF7</span><span class="sxs-lookup"><span data-stu-id="213c7-127">UTF7</span></span>
- <span data-ttu-id="213c7-128">Текстов</span><span class="sxs-lookup"><span data-stu-id="213c7-128">Ascii</span></span>
- <span data-ttu-id="213c7-129">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="213c7-129">Default</span></span>
- <span data-ttu-id="213c7-130">Поставщики</span><span class="sxs-lookup"><span data-stu-id="213c7-130">Oem</span></span>
- <span data-ttu-id="213c7-131">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="213c7-131">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c7-132">-Force</span><span class="sxs-lookup"><span data-stu-id="213c7-132">-Force</span></span>
<span data-ttu-id="213c7-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="213c7-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c7-134">-Head</span><span class="sxs-lookup"><span data-stu-id="213c7-134">-Head</span></span>
<span data-ttu-id="213c7-135">Количество строк (с разделением новой строки) от начала файла до просмотра.</span><span class="sxs-lookup"><span data-stu-id="213c7-135">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="213c7-136">Если в первых 4 МБ данных нет новой строки, будут возвращены только эти данные.</span><span class="sxs-lookup"><span data-stu-id="213c7-136">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the head of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c7-137">-Length</span><span class="sxs-lookup"><span data-stu-id="213c7-137">-Length</span></span>
<span data-ttu-id="213c7-138">Задает длину получаемого содержимого в байтах.</span><span class="sxs-lookup"><span data-stu-id="213c7-138">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c7-139">-Offset (смещение)</span><span class="sxs-lookup"><span data-stu-id="213c7-139">-Offset</span></span>
<span data-ttu-id="213c7-140">Указывает число байтов, которые нужно пропустить в файле, прежде чем получить содержимое.</span><span class="sxs-lookup"><span data-stu-id="213c7-140">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c7-141">-Path</span><span class="sxs-lookup"><span data-stu-id="213c7-141">-Path</span></span>
<span data-ttu-id="213c7-142">Задает путь к файлу Data Lake Store для файла, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="213c7-142">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="213c7-143">-Tail</span><span class="sxs-lookup"><span data-stu-id="213c7-143">-Tail</span></span>
<span data-ttu-id="213c7-144">Количество строк (с разделением новой строки) от конца файла до предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="213c7-144">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="213c7-145">Если в первых 4 МБ данных нет новой строки, будут возвращены только эти данные.</span><span class="sxs-lookup"><span data-stu-id="213c7-145">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the tail of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c7-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="213c7-146">-Confirm</span></span>
<span data-ttu-id="213c7-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="213c7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="213c7-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="213c7-148">-WhatIf</span></span>
<span data-ttu-id="213c7-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="213c7-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="213c7-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="213c7-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="213c7-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213c7-151">-DefaultProfile</span></span>
<span data-ttu-id="213c7-152">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="213c7-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213c7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213c7-153">CommonParameters</span></span>
<span data-ttu-id="213c7-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="213c7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213c7-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="213c7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213c7-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="213c7-156">INPUTS</span></span>

## <span data-ttu-id="213c7-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="213c7-157">OUTPUTS</span></span>

### <span data-ttu-id="213c7-158">Byte []</span><span class="sxs-lookup"><span data-stu-id="213c7-158">byte[]</span></span>
<span data-ttu-id="213c7-159">Строковое представление извлекаемого содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="213c7-159">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="213c7-160">подстрок</span><span class="sxs-lookup"><span data-stu-id="213c7-160">string</span></span>
<span data-ttu-id="213c7-161">Строковое представление (в указанной кодировке) извлекаемого содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="213c7-161">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="213c7-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="213c7-162">NOTES</span></span>

## <span data-ttu-id="213c7-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="213c7-163">RELATED LINKS</span></span>

