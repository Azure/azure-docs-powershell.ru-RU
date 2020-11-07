---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 1727c0960d90a8566d2247e8d8e091f6ce66f9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731080"
---
# <span data-ttu-id="0d63c-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="0d63c-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="0d63c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d63c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d63c-103">Добавляет содержимое в элемент в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d63c-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="0d63c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d63c-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d63c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d63c-105">DESCRIPTION</span></span>
<span data-ttu-id="0d63c-106">Командлет **Add-AzDataLakeStoreItemContent** добавляет содержимое в элемент в Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d63c-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="0d63c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d63c-107">EXAMPLES</span></span>

### <span data-ttu-id="0d63c-108">Пример 1: Добавление содержимого в файл</span><span class="sxs-lookup"><span data-stu-id="0d63c-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="0d63c-109">Эта команда добавляет содержимое в myFile.txt файла.</span><span class="sxs-lookup"><span data-stu-id="0d63c-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="0d63c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d63c-110">PARAMETERS</span></span>

### <span data-ttu-id="0d63c-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0d63c-111">-Account</span></span>
<span data-ttu-id="0d63c-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d63c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0d63c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d63c-113">-DefaultProfile</span></span>
<span data-ttu-id="0d63c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0d63c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d63c-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="0d63c-115">-Encoding</span></span>
<span data-ttu-id="0d63c-116">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="0d63c-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="0d63c-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d63c-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d63c-118">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="0d63c-118">Unknown</span></span>
- <span data-ttu-id="0d63c-119">Подстрок</span><span class="sxs-lookup"><span data-stu-id="0d63c-119">String</span></span>
- <span data-ttu-id="0d63c-120">Стандарт</span><span class="sxs-lookup"><span data-stu-id="0d63c-120">Unicode</span></span>
- <span data-ttu-id="0d63c-121">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="0d63c-121">Byte</span></span>
- <span data-ttu-id="0d63c-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="0d63c-122">BigEndianUnicode</span></span>
- <span data-ttu-id="0d63c-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="0d63c-123">UTF8</span></span>
- <span data-ttu-id="0d63c-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="0d63c-124">UTF7</span></span>
- <span data-ttu-id="0d63c-125">Текстов</span><span class="sxs-lookup"><span data-stu-id="0d63c-125">Ascii</span></span>
- <span data-ttu-id="0d63c-126">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="0d63c-126">Default</span></span>
- <span data-ttu-id="0d63c-127">Поставщики</span><span class="sxs-lookup"><span data-stu-id="0d63c-127">Oem</span></span>
- <span data-ttu-id="0d63c-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="0d63c-128">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d63c-129">-Path</span><span class="sxs-lookup"><span data-stu-id="0d63c-129">-Path</span></span>
<span data-ttu-id="0d63c-130">Указывает путь к Data Lake Store для элемента, который нужно изменить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="0d63c-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0d63c-131">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="0d63c-131">-Value</span></span>
<span data-ttu-id="0d63c-132">Указывает содержимое, которое нужно добавить к элементу.</span><span class="sxs-lookup"><span data-stu-id="0d63c-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="0d63c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d63c-133">CommonParameters</span></span>
<span data-ttu-id="0d63c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d63c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d63c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d63c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d63c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d63c-136">INPUTS</span></span>

### <span data-ttu-id="0d63c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0d63c-137">System.String</span></span>

### <span data-ttu-id="0d63c-138">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0d63c-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0d63c-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="0d63c-139">System.Object</span></span>

### <span data-ttu-id="0d63c-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="0d63c-140">System.Text.Encoding</span></span>

## <span data-ttu-id="0d63c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d63c-141">OUTPUTS</span></span>

### <span data-ttu-id="0d63c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d63c-142">System.Boolean</span></span>

## <span data-ttu-id="0d63c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d63c-143">NOTES</span></span>

## <span data-ttu-id="0d63c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d63c-144">RELATED LINKS</span></span>

[<span data-ttu-id="0d63c-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="0d63c-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


