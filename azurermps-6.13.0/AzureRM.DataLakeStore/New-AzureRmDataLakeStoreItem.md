---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2e50135762826661e82f499f2aec48c67d00c648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556699"
---
# <span data-ttu-id="afc16-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="afc16-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="afc16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="afc16-102">SYNOPSIS</span></span>
<span data-ttu-id="afc16-103">Создание нового файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="afc16-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afc16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="afc16-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afc16-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afc16-105">DESCRIPTION</span></span>
<span data-ttu-id="afc16-106">Командлет **New-AzureRmDataLakeStoreItem** создает новый файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="afc16-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="afc16-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="afc16-107">EXAMPLES</span></span>

### <span data-ttu-id="afc16-108">Пример 1: создание нового файла и новой папки</span><span class="sxs-lookup"><span data-stu-id="afc16-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="afc16-109">Первая команда создает файл NewFile.txt для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="afc16-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="afc16-110">Вторая команда создает папку NewFolder в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="afc16-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="afc16-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="afc16-111">PARAMETERS</span></span>

### <span data-ttu-id="afc16-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="afc16-112">-Account</span></span>
<span data-ttu-id="afc16-113">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="afc16-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="afc16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc16-114">-DefaultProfile</span></span>
<span data-ttu-id="afc16-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afc16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afc16-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="afc16-116">-Encoding</span></span>
<span data-ttu-id="afc16-117">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="afc16-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="afc16-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="afc16-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afc16-119">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="afc16-119">Unknown</span></span>
- <span data-ttu-id="afc16-120">Подстрок</span><span class="sxs-lookup"><span data-stu-id="afc16-120">String</span></span>
- <span data-ttu-id="afc16-121">Стандарт</span><span class="sxs-lookup"><span data-stu-id="afc16-121">Unicode</span></span>
- <span data-ttu-id="afc16-122">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="afc16-122">Byte</span></span>
- <span data-ttu-id="afc16-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="afc16-123">BigEndianUnicode</span></span>
- <span data-ttu-id="afc16-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="afc16-124">UTF8</span></span>
- <span data-ttu-id="afc16-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="afc16-125">UTF7</span></span>
- <span data-ttu-id="afc16-126">Текстов</span><span class="sxs-lookup"><span data-stu-id="afc16-126">Ascii</span></span>
- <span data-ttu-id="afc16-127">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="afc16-127">Default</span></span>
- <span data-ttu-id="afc16-128">Поставщики</span><span class="sxs-lookup"><span data-stu-id="afc16-128">Oem</span></span>
- <span data-ttu-id="afc16-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="afc16-129">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afc16-130">-Папка</span><span class="sxs-lookup"><span data-stu-id="afc16-130">-Folder</span></span>
<span data-ttu-id="afc16-131">Указывает на то, что эта операция создает папку.</span><span class="sxs-lookup"><span data-stu-id="afc16-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="afc16-132">-Force</span><span class="sxs-lookup"><span data-stu-id="afc16-132">-Force</span></span>
<span data-ttu-id="afc16-133">Указывает на то, что эта операция может перезаписать целевой элемент, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="afc16-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="afc16-134">-Path</span><span class="sxs-lookup"><span data-stu-id="afc16-134">-Path</span></span>
<span data-ttu-id="afc16-135">Указывает путь к Data Lake Store для создаваемого элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="afc16-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="afc16-136">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="afc16-136">-Value</span></span>
<span data-ttu-id="afc16-137">Указывает содержимое, которое будет добавлено к созданному элементу.</span><span class="sxs-lookup"><span data-stu-id="afc16-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="afc16-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afc16-138">-Confirm</span></span>
<span data-ttu-id="afc16-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="afc16-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc16-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc16-140">-WhatIf</span></span>
<span data-ttu-id="afc16-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="afc16-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afc16-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="afc16-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc16-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc16-143">CommonParameters</span></span>
<span data-ttu-id="afc16-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="afc16-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc16-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afc16-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc16-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="afc16-146">INPUTS</span></span>

### <span data-ttu-id="afc16-147">System. String</span><span class="sxs-lookup"><span data-stu-id="afc16-147">System.String</span></span>

### <span data-ttu-id="afc16-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="afc16-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="afc16-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="afc16-149">System.Object</span></span>

### <span data-ttu-id="afc16-150">Microsoft. Azure. Commands. DataLakeStore. Models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="afc16-150">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="afc16-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="afc16-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="afc16-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afc16-152">OUTPUTS</span></span>

### <span data-ttu-id="afc16-153">System. String</span><span class="sxs-lookup"><span data-stu-id="afc16-153">System.String</span></span>
<span data-ttu-id="afc16-154">Полный путь к созданному файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="afc16-154">The full path to the created file or folder.</span></span>

## <span data-ttu-id="afc16-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="afc16-155">NOTES</span></span>

## <span data-ttu-id="afc16-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afc16-156">RELATED LINKS</span></span>

[<span data-ttu-id="afc16-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="afc16-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="afc16-158">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="afc16-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="afc16-159">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="afc16-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="afc16-160">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="afc16-160">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="afc16-161">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="afc16-161">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="afc16-162">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="afc16-162">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


