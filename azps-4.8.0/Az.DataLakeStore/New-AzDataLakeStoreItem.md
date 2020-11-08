---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235590"
---
# <span data-ttu-id="43774-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="43774-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="43774-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43774-102">SYNOPSIS</span></span>
<span data-ttu-id="43774-103">Создание нового файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="43774-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="43774-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43774-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43774-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43774-105">DESCRIPTION</span></span>
<span data-ttu-id="43774-106">Командлет **New-AzDataLakeStoreItem** создает новый файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="43774-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="43774-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43774-107">EXAMPLES</span></span>

### <span data-ttu-id="43774-108">Пример 1: создание нового файла и новой папки</span><span class="sxs-lookup"><span data-stu-id="43774-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="43774-109">Первая команда создает файл NewFile.txt для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="43774-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="43774-110">Вторая команда создает папку NewFolder в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="43774-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="43774-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43774-111">PARAMETERS</span></span>

### <span data-ttu-id="43774-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="43774-112">-Account</span></span>
<span data-ttu-id="43774-113">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="43774-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="43774-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43774-114">-DefaultProfile</span></span>
<span data-ttu-id="43774-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43774-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43774-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="43774-116">-Encoding</span></span>
<span data-ttu-id="43774-117">Задает кодировку для создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="43774-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="43774-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43774-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43774-119">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="43774-119">Unknown</span></span>
- <span data-ttu-id="43774-120">Подстрок</span><span class="sxs-lookup"><span data-stu-id="43774-120">String</span></span>
- <span data-ttu-id="43774-121">Стандарт</span><span class="sxs-lookup"><span data-stu-id="43774-121">Unicode</span></span>
- <span data-ttu-id="43774-122">Двухбайтового</span><span class="sxs-lookup"><span data-stu-id="43774-122">Byte</span></span>
- <span data-ttu-id="43774-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="43774-123">BigEndianUnicode</span></span>
- <span data-ttu-id="43774-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="43774-124">UTF8</span></span>
- <span data-ttu-id="43774-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="43774-125">UTF7</span></span>
- <span data-ttu-id="43774-126">Текстов</span><span class="sxs-lookup"><span data-stu-id="43774-126">Ascii</span></span>
- <span data-ttu-id="43774-127">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="43774-127">Default</span></span>
- <span data-ttu-id="43774-128">Поставщики</span><span class="sxs-lookup"><span data-stu-id="43774-128">Oem</span></span>
- <span data-ttu-id="43774-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="43774-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="43774-130">-Папка</span><span class="sxs-lookup"><span data-stu-id="43774-130">-Folder</span></span>
<span data-ttu-id="43774-131">Указывает на то, что эта операция создает папку.</span><span class="sxs-lookup"><span data-stu-id="43774-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="43774-132">-Force</span><span class="sxs-lookup"><span data-stu-id="43774-132">-Force</span></span>
<span data-ttu-id="43774-133">Указывает на то, что эта операция может перезаписать целевой элемент, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="43774-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="43774-134">-Path</span><span class="sxs-lookup"><span data-stu-id="43774-134">-Path</span></span>
<span data-ttu-id="43774-135">Указывает путь к Data Lake Store для создаваемого элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="43774-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="43774-136">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="43774-136">-Value</span></span>
<span data-ttu-id="43774-137">Указывает содержимое, которое будет добавлено к созданному элементу.</span><span class="sxs-lookup"><span data-stu-id="43774-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="43774-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43774-138">-Confirm</span></span>
<span data-ttu-id="43774-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43774-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43774-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43774-140">-WhatIf</span></span>
<span data-ttu-id="43774-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43774-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43774-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43774-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43774-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43774-143">CommonParameters</span></span>
<span data-ttu-id="43774-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43774-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43774-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43774-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43774-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43774-146">INPUTS</span></span>

### <span data-ttu-id="43774-147">System. String</span><span class="sxs-lookup"><span data-stu-id="43774-147">System.String</span></span>

### <span data-ttu-id="43774-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="43774-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="43774-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="43774-149">System.Object</span></span>

### <span data-ttu-id="43774-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="43774-150">System.Text.Encoding</span></span>

### <span data-ttu-id="43774-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="43774-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="43774-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43774-152">OUTPUTS</span></span>

### <span data-ttu-id="43774-153">System. String</span><span class="sxs-lookup"><span data-stu-id="43774-153">System.String</span></span>

## <span data-ttu-id="43774-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="43774-154">NOTES</span></span>

## <span data-ttu-id="43774-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43774-155">RELATED LINKS</span></span>

[<span data-ttu-id="43774-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="43774-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="43774-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="43774-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="43774-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="43774-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="43774-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="43774-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="43774-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="43774-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="43774-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="43774-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)

