---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: aa2fe76f221ce412c0e47f7a43b1dba551131f45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994395"
---
# <span data-ttu-id="421fb-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="421fb-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="421fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="421fb-102">SYNOPSIS</span></span>
<span data-ttu-id="421fb-103">Добавляет содержимое к элементу в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="421fb-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="421fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="421fb-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="421fb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="421fb-105">DESCRIPTION</span></span>
<span data-ttu-id="421fb-106">**Cmdlet Add-AzDataLakeStoreItemContent** добавляет содержимое к элементу в Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="421fb-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="421fb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="421fb-107">EXAMPLES</span></span>

### <span data-ttu-id="421fb-108">Пример 1. Добавление содержимого в файл</span><span class="sxs-lookup"><span data-stu-id="421fb-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="421fb-109">Эта команда добавляет содержимое в myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="421fb-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="421fb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="421fb-110">PARAMETERS</span></span>

### <span data-ttu-id="421fb-111">-Account</span><span class="sxs-lookup"><span data-stu-id="421fb-111">-Account</span></span>
<span data-ttu-id="421fb-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="421fb-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="421fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421fb-113">-DefaultProfile</span></span>
<span data-ttu-id="421fb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="421fb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="421fb-115">-Кодировидная кодировидная</span><span class="sxs-lookup"><span data-stu-id="421fb-115">-Encoding</span></span>
<span data-ttu-id="421fb-116">Определяет кодию элемента, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="421fb-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="421fb-117">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="421fb-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="421fb-118">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="421fb-118">Unknown</span></span>
- <span data-ttu-id="421fb-119">Строка</span><span class="sxs-lookup"><span data-stu-id="421fb-119">String</span></span>
- <span data-ttu-id="421fb-120">Юникод</span><span class="sxs-lookup"><span data-stu-id="421fb-120">Unicode</span></span>
- <span data-ttu-id="421fb-121">Byte</span><span class="sxs-lookup"><span data-stu-id="421fb-121">Byte</span></span>
- <span data-ttu-id="421fb-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="421fb-122">BigEndianUnicode</span></span>
- <span data-ttu-id="421fb-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="421fb-123">UTF8</span></span>
- <span data-ttu-id="421fb-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="421fb-124">UTF7</span></span>
- <span data-ttu-id="421fb-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="421fb-125">Ascii</span></span>
- <span data-ttu-id="421fb-126">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="421fb-126">Default</span></span>
- <span data-ttu-id="421fb-127">Oem</span><span class="sxs-lookup"><span data-stu-id="421fb-127">Oem</span></span>
- <span data-ttu-id="421fb-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="421fb-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="421fb-129">-Path</span><span class="sxs-lookup"><span data-stu-id="421fb-129">-Path</span></span>
<span data-ttu-id="421fb-130">Путь к элементу, который нужно изменить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="421fb-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="421fb-131">-Value</span><span class="sxs-lookup"><span data-stu-id="421fb-131">-Value</span></span>
<span data-ttu-id="421fb-132">Определяет содержимое, которое нужно добавить к элементу.</span><span class="sxs-lookup"><span data-stu-id="421fb-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="421fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421fb-133">CommonParameters</span></span>
<span data-ttu-id="421fb-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="421fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421fb-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="421fb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421fb-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="421fb-136">INPUTS</span></span>

### <span data-ttu-id="421fb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="421fb-137">System.String</span></span>

### <span data-ttu-id="421fb-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="421fb-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="421fb-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="421fb-139">System.Object</span></span>

### <span data-ttu-id="421fb-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="421fb-140">System.Text.Encoding</span></span>

## <span data-ttu-id="421fb-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="421fb-141">OUTPUTS</span></span>

### <span data-ttu-id="421fb-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="421fb-142">System.Boolean</span></span>

## <span data-ttu-id="421fb-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="421fb-143">NOTES</span></span>

## <span data-ttu-id="421fb-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="421fb-144">RELATED LINKS</span></span>

[<span data-ttu-id="421fb-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="421fb-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


