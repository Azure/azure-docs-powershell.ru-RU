---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415020"
---
# <span data-ttu-id="1de50-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1de50-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="1de50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1de50-102">SYNOPSIS</span></span>
<span data-ttu-id="1de50-103">Создает файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1de50-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1de50-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1de50-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1de50-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1de50-105">DESCRIPTION</span></span>
<span data-ttu-id="1de50-106">Для создания файла или папки в магазине Data Lake Store будет создаваться новый cmdlet **AzDataLakeStoreItem.**</span><span class="sxs-lookup"><span data-stu-id="1de50-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1de50-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1de50-107">EXAMPLES</span></span>

### <span data-ttu-id="1de50-108">Пример 1. Создание файла и новой папки</span><span class="sxs-lookup"><span data-stu-id="1de50-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="1de50-109">Первая команда создает файл NewFile.txt для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1de50-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="1de50-110">Вторая команда создает папку NewFolder в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="1de50-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="1de50-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1de50-111">PARAMETERS</span></span>

### <span data-ttu-id="1de50-112">-Account</span><span class="sxs-lookup"><span data-stu-id="1de50-112">-Account</span></span>
<span data-ttu-id="1de50-113">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1de50-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1de50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de50-114">-DefaultProfile</span></span>
<span data-ttu-id="1de50-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1de50-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1de50-116">-Кодировидная кодировидная</span><span class="sxs-lookup"><span data-stu-id="1de50-116">-Encoding</span></span>
<span data-ttu-id="1de50-117">Определяет кодию элемента, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="1de50-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="1de50-118">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="1de50-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1de50-119">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="1de50-119">Unknown</span></span>
- <span data-ttu-id="1de50-120">Строка</span><span class="sxs-lookup"><span data-stu-id="1de50-120">String</span></span>
- <span data-ttu-id="1de50-121">Юникод</span><span class="sxs-lookup"><span data-stu-id="1de50-121">Unicode</span></span>
- <span data-ttu-id="1de50-122">Byte</span><span class="sxs-lookup"><span data-stu-id="1de50-122">Byte</span></span>
- <span data-ttu-id="1de50-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="1de50-123">BigEndianUnicode</span></span>
- <span data-ttu-id="1de50-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="1de50-124">UTF8</span></span>
- <span data-ttu-id="1de50-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="1de50-125">UTF7</span></span>
- <span data-ttu-id="1de50-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="1de50-126">Ascii</span></span>
- <span data-ttu-id="1de50-127">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1de50-127">Default</span></span>
- <span data-ttu-id="1de50-128">Oem</span><span class="sxs-lookup"><span data-stu-id="1de50-128">Oem</span></span>
- <span data-ttu-id="1de50-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="1de50-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="1de50-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="1de50-130">-Folder</span></span>
<span data-ttu-id="1de50-131">Указывает на то, что в результате этой операции создается папка.</span><span class="sxs-lookup"><span data-stu-id="1de50-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="1de50-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1de50-132">-Force</span></span>
<span data-ttu-id="1de50-133">Указывает на то, что данной операцией можно переписать элемент, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="1de50-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="1de50-134">-Path</span><span class="sxs-lookup"><span data-stu-id="1de50-134">-Path</span></span>
<span data-ttu-id="1de50-135">Путь к создаемой позиции в магазине данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="1de50-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1de50-136">-Value</span><span class="sxs-lookup"><span data-stu-id="1de50-136">-Value</span></span>
<span data-ttu-id="1de50-137">Определяет содержимое, которое нужно добавить к созда создаемому элементу.</span><span class="sxs-lookup"><span data-stu-id="1de50-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="1de50-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1de50-138">-Confirm</span></span>
<span data-ttu-id="1de50-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1de50-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1de50-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1de50-140">-WhatIf</span></span>
<span data-ttu-id="1de50-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1de50-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1de50-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1de50-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1de50-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de50-143">CommonParameters</span></span>
<span data-ttu-id="1de50-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1de50-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de50-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1de50-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de50-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1de50-146">INPUTS</span></span>

### <span data-ttu-id="1de50-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1de50-147">System.String</span></span>

### <span data-ttu-id="1de50-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1de50-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1de50-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="1de50-149">System.Object</span></span>

### <span data-ttu-id="1de50-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="1de50-150">System.Text.Encoding</span></span>

### <span data-ttu-id="1de50-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1de50-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1de50-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1de50-152">OUTPUTS</span></span>

### <span data-ttu-id="1de50-153">System.String</span><span class="sxs-lookup"><span data-stu-id="1de50-153">System.String</span></span>

## <span data-ttu-id="1de50-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1de50-154">NOTES</span></span>

## <span data-ttu-id="1de50-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1de50-155">RELATED LINKS</span></span>

[<span data-ttu-id="1de50-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1de50-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="1de50-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1de50-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="1de50-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1de50-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="1de50-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1de50-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="1de50-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1de50-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="1de50-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1de50-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


