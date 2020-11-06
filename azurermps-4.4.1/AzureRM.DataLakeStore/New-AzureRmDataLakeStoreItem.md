---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a087c2f7cfd4358e137550aa2e916fa2200d2a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567650"
---
# <span data-ttu-id="b07e4-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="b07e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b07e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b07e4-103">Создание нового файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b07e4-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b07e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b07e4-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b07e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b07e4-106">Командлет **New-AzureRmDataLakeStoreItem** создает новый файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b07e4-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b07e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b07e4-107">EXAMPLES</span></span>

### <span data-ttu-id="b07e4-108">Пример 1: создание нового файла и новой папки</span><span class="sxs-lookup"><span data-stu-id="b07e4-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="b07e4-109">Первая команда создает файл NewFile.txt для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b07e4-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="b07e4-110">Вторая команда создает папку NewFolder в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="b07e4-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="b07e4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b07e4-111">PARAMETERS</span></span>

### <span data-ttu-id="b07e4-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b07e4-112">-Account</span></span>
<span data-ttu-id="b07e4-113">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b07e4-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b07e4-114">-Encoding</span><span class="sxs-lookup"><span data-stu-id="b07e4-114">-Encoding</span></span>
<span data-ttu-id="b07e4-115">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="b07e4-115">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="b07e4-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b07e4-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b07e4-117">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="b07e4-117">Unknown</span></span>
- <span data-ttu-id="b07e4-118">Подстрок</span><span class="sxs-lookup"><span data-stu-id="b07e4-118">String</span></span>
- <span data-ttu-id="b07e4-119">Стандарт</span><span class="sxs-lookup"><span data-stu-id="b07e4-119">Unicode</span></span>
- <span data-ttu-id="b07e4-120">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="b07e4-120">Byte</span></span>
- <span data-ttu-id="b07e4-121">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="b07e4-121">BigEndianUnicode</span></span>
- <span data-ttu-id="b07e4-122">UTF8</span><span class="sxs-lookup"><span data-stu-id="b07e4-122">UTF8</span></span>
- <span data-ttu-id="b07e4-123">UTF7</span><span class="sxs-lookup"><span data-stu-id="b07e4-123">UTF7</span></span>
- <span data-ttu-id="b07e4-124">Текстов</span><span class="sxs-lookup"><span data-stu-id="b07e4-124">Ascii</span></span>
- <span data-ttu-id="b07e4-125">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="b07e4-125">Default</span></span>
- <span data-ttu-id="b07e4-126">Поставщики</span><span class="sxs-lookup"><span data-stu-id="b07e4-126">Oem</span></span>
- <span data-ttu-id="b07e4-127">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="b07e4-127">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07e4-128">-Папка</span><span class="sxs-lookup"><span data-stu-id="b07e4-128">-Folder</span></span>
<span data-ttu-id="b07e4-129">Указывает на то, что эта операция создает папку.</span><span class="sxs-lookup"><span data-stu-id="b07e4-129">Indicates that this operation creates a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07e4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="b07e4-130">-Force</span></span>
<span data-ttu-id="b07e4-131">Указывает на то, что эта операция может перезаписать целевой элемент, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="b07e4-131">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07e4-132">-Path</span><span class="sxs-lookup"><span data-stu-id="b07e4-132">-Path</span></span>
<span data-ttu-id="b07e4-133">Указывает путь к Data Lake Store для создаваемого элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b07e4-133">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b07e4-134">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="b07e4-134">-Value</span></span>
<span data-ttu-id="b07e4-135">Указывает содержимое, которое будет добавлено к созданному элементу.</span><span class="sxs-lookup"><span data-stu-id="b07e4-135">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b07e4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b07e4-136">-Confirm</span></span>
<span data-ttu-id="b07e4-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b07e4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07e4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b07e4-138">-WhatIf</span></span>
<span data-ttu-id="b07e4-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b07e4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b07e4-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b07e4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07e4-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07e4-141">-DefaultProfile</span></span>
<span data-ttu-id="b07e4-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b07e4-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b07e4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07e4-143">CommonParameters</span></span>
<span data-ttu-id="b07e4-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b07e4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07e4-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07e4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07e4-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b07e4-146">INPUTS</span></span>

### <span data-ttu-id="b07e4-147">DataObject</span><span class="sxs-lookup"><span data-stu-id="b07e4-147">Object</span></span>
<span data-ttu-id="b07e4-148">Параметр "значение" принимает значение типа "Object" из конвейера</span><span class="sxs-lookup"><span data-stu-id="b07e4-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="b07e4-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07e4-149">OUTPUTS</span></span>

### <span data-ttu-id="b07e4-150">подстрок</span><span class="sxs-lookup"><span data-stu-id="b07e4-150">string</span></span>
<span data-ttu-id="b07e4-151">Полный путь к созданному файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="b07e4-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="b07e4-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="b07e4-152">NOTES</span></span>

## <span data-ttu-id="b07e4-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b07e4-153">RELATED LINKS</span></span>

[<span data-ttu-id="b07e4-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-156">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


