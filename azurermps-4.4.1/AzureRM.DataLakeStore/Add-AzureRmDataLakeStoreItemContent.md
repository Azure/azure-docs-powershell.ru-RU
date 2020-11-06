---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 4ce79044793bbecc76d72fab015166ccc3d8fba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559847"
---
# <span data-ttu-id="b6862-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b6862-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="b6862-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6862-102">SYNOPSIS</span></span>
<span data-ttu-id="b6862-103">Добавляет содержимое в элемент в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6862-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6862-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6862-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6862-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6862-105">DESCRIPTION</span></span>
<span data-ttu-id="b6862-106">Командлет **Add-AzureRmDataLakeStoreItemContent** добавляет содержимое в элемент в Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6862-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="b6862-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6862-107">EXAMPLES</span></span>

### <span data-ttu-id="b6862-108">Пример 1: Добавление содержимого в файл</span><span class="sxs-lookup"><span data-stu-id="b6862-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="b6862-109">Эта команда добавляет содержимое в myFile.txt файла.</span><span class="sxs-lookup"><span data-stu-id="b6862-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="b6862-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6862-110">PARAMETERS</span></span>

### <span data-ttu-id="b6862-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b6862-111">-Account</span></span>
<span data-ttu-id="b6862-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6862-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b6862-113">-Encoding</span><span class="sxs-lookup"><span data-stu-id="b6862-113">-Encoding</span></span>
<span data-ttu-id="b6862-114">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="b6862-114">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="b6862-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b6862-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6862-116">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="b6862-116">Unknown</span></span>
- <span data-ttu-id="b6862-117">Подстрок</span><span class="sxs-lookup"><span data-stu-id="b6862-117">String</span></span>
- <span data-ttu-id="b6862-118">Стандарт</span><span class="sxs-lookup"><span data-stu-id="b6862-118">Unicode</span></span>
- <span data-ttu-id="b6862-119">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="b6862-119">Byte</span></span>
- <span data-ttu-id="b6862-120">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="b6862-120">BigEndianUnicode</span></span>
- <span data-ttu-id="b6862-121">UTF8</span><span class="sxs-lookup"><span data-stu-id="b6862-121">UTF8</span></span>
- <span data-ttu-id="b6862-122">UTF7</span><span class="sxs-lookup"><span data-stu-id="b6862-122">UTF7</span></span>
- <span data-ttu-id="b6862-123">Текстов</span><span class="sxs-lookup"><span data-stu-id="b6862-123">Ascii</span></span>
- <span data-ttu-id="b6862-124">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="b6862-124">Default</span></span>
- <span data-ttu-id="b6862-125">Поставщики</span><span class="sxs-lookup"><span data-stu-id="b6862-125">Oem</span></span>
- <span data-ttu-id="b6862-126">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="b6862-126">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6862-127">-Path</span><span class="sxs-lookup"><span data-stu-id="b6862-127">-Path</span></span>
<span data-ttu-id="b6862-128">Указывает путь к Data Lake Store для элемента, который нужно изменить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b6862-128">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b6862-129">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="b6862-129">-Value</span></span>
<span data-ttu-id="b6862-130">Указывает содержимое, которое нужно добавить к элементу.</span><span class="sxs-lookup"><span data-stu-id="b6862-130">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6862-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6862-131">-DefaultProfile</span></span>
<span data-ttu-id="b6862-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6862-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6862-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6862-133">CommonParameters</span></span>
<span data-ttu-id="b6862-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6862-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6862-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6862-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6862-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6862-136">INPUTS</span></span>

### <span data-ttu-id="b6862-137">DataObject</span><span class="sxs-lookup"><span data-stu-id="b6862-137">Object</span></span>
<span data-ttu-id="b6862-138">Параметр "значение" принимает значение типа "Object" из конвейера</span><span class="sxs-lookup"><span data-stu-id="b6862-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="b6862-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6862-139">OUTPUTS</span></span>

### <span data-ttu-id="b6862-140">логических</span><span class="sxs-lookup"><span data-stu-id="b6862-140">bool</span></span>
<span data-ttu-id="b6862-141">Возвращает значение истина в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="b6862-141">Returns true on success.</span></span>

## <span data-ttu-id="b6862-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6862-142">NOTES</span></span>

## <span data-ttu-id="b6862-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6862-143">RELATED LINKS</span></span>

[<span data-ttu-id="b6862-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b6862-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


