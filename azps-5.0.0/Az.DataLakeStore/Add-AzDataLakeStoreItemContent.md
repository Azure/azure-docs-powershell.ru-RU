---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313445"
---
# <span data-ttu-id="2c1d2-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="2c1d2-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="2c1d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1d2-103">Добавляет содержимое в элемент в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c1d2-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="2c1d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c1d2-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c1d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c1d2-105">DESCRIPTION</span></span>
<span data-ttu-id="2c1d2-106">Командлет **Add-AzDataLakeStoreItemContent** добавляет содержимое в элемент в Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c1d2-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="2c1d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c1d2-107">EXAMPLES</span></span>

### <span data-ttu-id="2c1d2-108">Пример 1: Добавление содержимого в файл</span><span class="sxs-lookup"><span data-stu-id="2c1d2-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="2c1d2-109">Эта команда добавляет содержимое в myFile.txt файла.</span><span class="sxs-lookup"><span data-stu-id="2c1d2-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="2c1d2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c1d2-110">PARAMETERS</span></span>

### <span data-ttu-id="2c1d2-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2c1d2-111">-Account</span></span>
<span data-ttu-id="2c1d2-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c1d2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2c1d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1d2-113">-DefaultProfile</span></span>
<span data-ttu-id="2c1d2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2c1d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c1d2-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="2c1d2-115">-Encoding</span></span>
<span data-ttu-id="2c1d2-116">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="2c1d2-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="2c1d2-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2c1d2-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2c1d2-118">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="2c1d2-118">Unknown</span></span>
- <span data-ttu-id="2c1d2-119">Подстрок</span><span class="sxs-lookup"><span data-stu-id="2c1d2-119">String</span></span>
- <span data-ttu-id="2c1d2-120">Стандарт</span><span class="sxs-lookup"><span data-stu-id="2c1d2-120">Unicode</span></span>
- <span data-ttu-id="2c1d2-121">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="2c1d2-121">Byte</span></span>
- <span data-ttu-id="2c1d2-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="2c1d2-122">BigEndianUnicode</span></span>
- <span data-ttu-id="2c1d2-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="2c1d2-123">UTF8</span></span>
- <span data-ttu-id="2c1d2-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="2c1d2-124">UTF7</span></span>
- <span data-ttu-id="2c1d2-125">Текстов</span><span class="sxs-lookup"><span data-stu-id="2c1d2-125">Ascii</span></span>
- <span data-ttu-id="2c1d2-126">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c1d2-126">Default</span></span>
- <span data-ttu-id="2c1d2-127">Поставщики</span><span class="sxs-lookup"><span data-stu-id="2c1d2-127">Oem</span></span>
- <span data-ttu-id="2c1d2-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="2c1d2-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="2c1d2-129">-Path</span><span class="sxs-lookup"><span data-stu-id="2c1d2-129">-Path</span></span>
<span data-ttu-id="2c1d2-130">Указывает путь к Data Lake Store для элемента, который нужно изменить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="2c1d2-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2c1d2-131">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="2c1d2-131">-Value</span></span>
<span data-ttu-id="2c1d2-132">Указывает содержимое, которое нужно добавить к элементу.</span><span class="sxs-lookup"><span data-stu-id="2c1d2-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="2c1d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1d2-133">CommonParameters</span></span>
<span data-ttu-id="2c1d2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c1d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1d2-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c1d2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1d2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c1d2-136">INPUTS</span></span>

### <span data-ttu-id="2c1d2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2c1d2-137">System.String</span></span>

### <span data-ttu-id="2c1d2-138">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2c1d2-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2c1d2-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="2c1d2-139">System.Object</span></span>

### <span data-ttu-id="2c1d2-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="2c1d2-140">System.Text.Encoding</span></span>

## <span data-ttu-id="2c1d2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c1d2-141">OUTPUTS</span></span>

### <span data-ttu-id="2c1d2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c1d2-142">System.Boolean</span></span>

## <span data-ttu-id="2c1d2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c1d2-143">NOTES</span></span>

## <span data-ttu-id="2c1d2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c1d2-144">RELATED LINKS</span></span>

[<span data-ttu-id="2c1d2-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="2c1d2-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


