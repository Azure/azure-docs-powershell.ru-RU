---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 7a757ca4b310176a71a7b2fe7e5c301137998ff9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568182"
---
# <span data-ttu-id="ecf3a-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="ecf3a-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="ecf3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecf3a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf3a-103">Получает содержимое файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecf3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecf3a-104">SYNTAX</span></span>

### <span data-ttu-id="ecf3a-105">PreviewFileContent (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecf3a-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf3a-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="ecf3a-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf3a-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="ecf3a-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf3a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecf3a-108">DESCRIPTION</span></span>
<span data-ttu-id="ecf3a-109">Командлет **Get-AzureRmDataLakeStoreItemContent** получает содержимое файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="ecf3a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecf3a-110">EXAMPLES</span></span>

### <span data-ttu-id="ecf3a-111">Пример 1: получение содержимого файла</span><span class="sxs-lookup"><span data-stu-id="ecf3a-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="ecf3a-112">Эта команда получает содержимое файла MyFile.txt в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="ecf3a-113">Пример 2: получение первых двух строк файла</span><span class="sxs-lookup"><span data-stu-id="ecf3a-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="ecf3a-114">Эта команда получает первые две строки, разделенные строками в файле, MyFile.txt в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="ecf3a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecf3a-115">PARAMETERS</span></span>

### <span data-ttu-id="ecf3a-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ecf3a-116">-Account</span></span>
<span data-ttu-id="ecf3a-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ecf3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf3a-118">-DefaultProfile</span></span>
<span data-ttu-id="ecf3a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecf3a-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="ecf3a-120">-Encoding</span></span>
<span data-ttu-id="ecf3a-121">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="ecf3a-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ecf3a-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecf3a-123">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="ecf3a-123">Unknown</span></span>
- <span data-ttu-id="ecf3a-124">Подстрок</span><span class="sxs-lookup"><span data-stu-id="ecf3a-124">String</span></span>
- <span data-ttu-id="ecf3a-125">Стандарт</span><span class="sxs-lookup"><span data-stu-id="ecf3a-125">Unicode</span></span>
- <span data-ttu-id="ecf3a-126">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="ecf3a-126">Byte</span></span>
- <span data-ttu-id="ecf3a-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="ecf3a-127">BigEndianUnicode</span></span>
- <span data-ttu-id="ecf3a-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="ecf3a-128">UTF8</span></span>
- <span data-ttu-id="ecf3a-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="ecf3a-129">UTF7</span></span>
- <span data-ttu-id="ecf3a-130">Текстов</span><span class="sxs-lookup"><span data-stu-id="ecf3a-130">Ascii</span></span>
- <span data-ttu-id="ecf3a-131">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ecf3a-131">Default</span></span>
- <span data-ttu-id="ecf3a-132">Поставщики</span><span class="sxs-lookup"><span data-stu-id="ecf3a-132">Oem</span></span>
- <span data-ttu-id="ecf3a-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="ecf3a-133">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf3a-134">-Force</span><span class="sxs-lookup"><span data-stu-id="ecf3a-134">-Force</span></span>
<span data-ttu-id="ecf3a-135">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ecf3a-136">-Head</span><span class="sxs-lookup"><span data-stu-id="ecf3a-136">-Head</span></span>
<span data-ttu-id="ecf3a-137">Количество строк (с разделением новой строки) от начала файла до просмотра.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="ecf3a-138">Если в первых 4 МБ данных нет новой строки, будут возвращены только эти данные.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="ecf3a-139">-Length</span><span class="sxs-lookup"><span data-stu-id="ecf3a-139">-Length</span></span>
<span data-ttu-id="ecf3a-140">Задает длину получаемого содержимого в байтах.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="ecf3a-141">-Offset (смещение)</span><span class="sxs-lookup"><span data-stu-id="ecf3a-141">-Offset</span></span>
<span data-ttu-id="ecf3a-142">Указывает число байтов, которые нужно пропустить в файле, прежде чем получить содержимое.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="ecf3a-143">-Path</span><span class="sxs-lookup"><span data-stu-id="ecf3a-143">-Path</span></span>
<span data-ttu-id="ecf3a-144">Задает путь к файлу Data Lake Store для файла, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="ecf3a-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ecf3a-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="ecf3a-145">-Tail</span></span>
<span data-ttu-id="ecf3a-146">Количество строк (с разделением новой строки) от конца файла до предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="ecf3a-147">Если в первых 4 МБ данных нет новой строки, будут возвращены только эти данные.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="ecf3a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecf3a-148">-Confirm</span></span>
<span data-ttu-id="ecf3a-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf3a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf3a-150">-WhatIf</span></span>
<span data-ttu-id="ecf3a-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf3a-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf3a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf3a-153">CommonParameters</span></span>
<span data-ttu-id="ecf3a-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf3a-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf3a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf3a-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecf3a-156">INPUTS</span></span>

### <span data-ttu-id="ecf3a-157">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf3a-157">System.String</span></span>

### <span data-ttu-id="ecf3a-158">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ecf3a-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ecf3a-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ecf3a-159">System.Int32</span></span>

### <span data-ttu-id="ecf3a-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="ecf3a-160">System.Int64</span></span>

### <span data-ttu-id="ecf3a-161">Microsoft. Azure. Commands. DataLakeStore. Models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="ecf3a-161">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="ecf3a-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ecf3a-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ecf3a-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecf3a-163">OUTPUTS</span></span>

### <span data-ttu-id="ecf3a-164">System. Byte</span><span class="sxs-lookup"><span data-stu-id="ecf3a-164">System.Byte</span></span>
<span data-ttu-id="ecf3a-165">Строковое представление извлекаемого содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-165">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="ecf3a-166">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf3a-166">System.String</span></span>
<span data-ttu-id="ecf3a-167">Строковое представление (в указанной кодировке) извлекаемого содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-167">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="ecf3a-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecf3a-168">NOTES</span></span>

## <span data-ttu-id="ecf3a-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecf3a-169">RELATED LINKS</span></span>
