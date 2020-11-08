---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: e5aaff4f915143e2e7695c9f650aed6fb01ba389
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077847"
---
# <span data-ttu-id="a1b04-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a1b04-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="a1b04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1b04-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b04-103">Получает содержимое файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a1b04-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="a1b04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1b04-104">SYNTAX</span></span>

### <span data-ttu-id="a1b04-105">PreviewFileContent (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1b04-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b04-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="a1b04-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b04-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="a1b04-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b04-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1b04-108">DESCRIPTION</span></span>
<span data-ttu-id="a1b04-109">Командлет **Get-AzDataLakeStoreItemContent** получает содержимое файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a1b04-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="a1b04-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1b04-110">EXAMPLES</span></span>

### <span data-ttu-id="a1b04-111">Пример 1: получение содержимого файла</span><span class="sxs-lookup"><span data-stu-id="a1b04-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="a1b04-112">Эта команда получает содержимое файла MyFile.txt в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="a1b04-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="a1b04-113">Пример 2: получение первых двух строк файла</span><span class="sxs-lookup"><span data-stu-id="a1b04-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="a1b04-114">Эта команда получает первые две строки, разделенные строками в файле, MyFile.txt в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="a1b04-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="a1b04-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1b04-115">PARAMETERS</span></span>

### <span data-ttu-id="a1b04-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a1b04-116">-Account</span></span>
<span data-ttu-id="a1b04-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a1b04-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a1b04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b04-118">-DefaultProfile</span></span>
<span data-ttu-id="a1b04-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b04-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b04-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="a1b04-120">-Encoding</span></span>
<span data-ttu-id="a1b04-121">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="a1b04-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="a1b04-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a1b04-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1b04-123">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="a1b04-123">Unknown</span></span>
- <span data-ttu-id="a1b04-124">Подстрок</span><span class="sxs-lookup"><span data-stu-id="a1b04-124">String</span></span>
- <span data-ttu-id="a1b04-125">Стандарт</span><span class="sxs-lookup"><span data-stu-id="a1b04-125">Unicode</span></span>
- <span data-ttu-id="a1b04-126">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="a1b04-126">Byte</span></span>
- <span data-ttu-id="a1b04-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="a1b04-127">BigEndianUnicode</span></span>
- <span data-ttu-id="a1b04-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="a1b04-128">UTF8</span></span>
- <span data-ttu-id="a1b04-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="a1b04-129">UTF7</span></span>
- <span data-ttu-id="a1b04-130">Текстов</span><span class="sxs-lookup"><span data-stu-id="a1b04-130">Ascii</span></span>
- <span data-ttu-id="a1b04-131">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a1b04-131">Default</span></span>
- <span data-ttu-id="a1b04-132">Поставщики</span><span class="sxs-lookup"><span data-stu-id="a1b04-132">Oem</span></span>
- <span data-ttu-id="a1b04-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="a1b04-133">BigEndianUTF32</span></span>

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

### <span data-ttu-id="a1b04-134">-Force</span><span class="sxs-lookup"><span data-stu-id="a1b04-134">-Force</span></span>
<span data-ttu-id="a1b04-135">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1b04-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1b04-136">-Head</span><span class="sxs-lookup"><span data-stu-id="a1b04-136">-Head</span></span>
<span data-ttu-id="a1b04-137">Количество строк (с разделением новой строки) от начала файла до просмотра.</span><span class="sxs-lookup"><span data-stu-id="a1b04-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="a1b04-138">Если в первых 4 МБ данных нет новой строки, будут возвращены только эти данные.</span><span class="sxs-lookup"><span data-stu-id="a1b04-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="a1b04-139">-Length</span><span class="sxs-lookup"><span data-stu-id="a1b04-139">-Length</span></span>
<span data-ttu-id="a1b04-140">Задает длину получаемого содержимого в байтах.</span><span class="sxs-lookup"><span data-stu-id="a1b04-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="a1b04-141">-Offset (смещение)</span><span class="sxs-lookup"><span data-stu-id="a1b04-141">-Offset</span></span>
<span data-ttu-id="a1b04-142">Указывает число байтов, которые нужно пропустить в файле, прежде чем получить содержимое.</span><span class="sxs-lookup"><span data-stu-id="a1b04-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="a1b04-143">-Path</span><span class="sxs-lookup"><span data-stu-id="a1b04-143">-Path</span></span>
<span data-ttu-id="a1b04-144">Задает путь к файлу Data Lake Store для файла, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="a1b04-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a1b04-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="a1b04-145">-Tail</span></span>
<span data-ttu-id="a1b04-146">Количество строк (с разделением новой строки) от конца файла до предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="a1b04-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="a1b04-147">Если в первых 4 МБ данных нет новой строки, будут возвращены только эти данные.</span><span class="sxs-lookup"><span data-stu-id="a1b04-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="a1b04-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1b04-148">-Confirm</span></span>
<span data-ttu-id="a1b04-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1b04-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b04-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b04-150">-WhatIf</span></span>
<span data-ttu-id="a1b04-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1b04-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b04-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1b04-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b04-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b04-153">CommonParameters</span></span>
<span data-ttu-id="a1b04-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1b04-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b04-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b04-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b04-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1b04-156">INPUTS</span></span>

### <span data-ttu-id="a1b04-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b04-157">System.String</span></span>

### <span data-ttu-id="a1b04-158">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a1b04-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a1b04-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a1b04-159">System.Int32</span></span>

### <span data-ttu-id="a1b04-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="a1b04-160">System.Int64</span></span>

### <span data-ttu-id="a1b04-161">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="a1b04-161">System.Text.Encoding</span></span>

### <span data-ttu-id="a1b04-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a1b04-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a1b04-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1b04-163">OUTPUTS</span></span>

### <span data-ttu-id="a1b04-164">System. Byte</span><span class="sxs-lookup"><span data-stu-id="a1b04-164">System.Byte</span></span>

### <span data-ttu-id="a1b04-165">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b04-165">System.String</span></span>

## <span data-ttu-id="a1b04-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1b04-166">NOTES</span></span>

## <span data-ttu-id="a1b04-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1b04-167">RELATED LINKS</span></span>