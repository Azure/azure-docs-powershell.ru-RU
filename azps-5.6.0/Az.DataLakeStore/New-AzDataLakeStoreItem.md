---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 46495d5a057de6c7cff21cdc09fe68d80e0c4da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991427"
---
# <span data-ttu-id="af75e-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="af75e-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="af75e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af75e-102">SYNOPSIS</span></span>
<span data-ttu-id="af75e-103">Создает файл или папку в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="af75e-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="af75e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af75e-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af75e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af75e-105">DESCRIPTION</span></span>
<span data-ttu-id="af75e-106">Для создания файла или папки в магазине Data Lake Store будет создаваться новый cmdlet **AzDataLakeStoreItem.**</span><span class="sxs-lookup"><span data-stu-id="af75e-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="af75e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af75e-107">EXAMPLES</span></span>

### <span data-ttu-id="af75e-108">Пример 1. Создание файла и новой папки</span><span class="sxs-lookup"><span data-stu-id="af75e-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="af75e-109">Первая команда создает файл NewFile.txt для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="af75e-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="af75e-110">Вторая команда создает папку NewFolder в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="af75e-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="af75e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af75e-111">PARAMETERS</span></span>

### <span data-ttu-id="af75e-112">-Account</span><span class="sxs-lookup"><span data-stu-id="af75e-112">-Account</span></span>
<span data-ttu-id="af75e-113">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="af75e-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="af75e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af75e-114">-DefaultProfile</span></span>
<span data-ttu-id="af75e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af75e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af75e-116">-Кодировидная кодиро</span><span class="sxs-lookup"><span data-stu-id="af75e-116">-Encoding</span></span>
<span data-ttu-id="af75e-117">Определяет кодию элемента, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="af75e-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="af75e-118">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="af75e-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af75e-119">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="af75e-119">Unknown</span></span>
- <span data-ttu-id="af75e-120">Строка</span><span class="sxs-lookup"><span data-stu-id="af75e-120">String</span></span>
- <span data-ttu-id="af75e-121">Юникод</span><span class="sxs-lookup"><span data-stu-id="af75e-121">Unicode</span></span>
- <span data-ttu-id="af75e-122">Byte</span><span class="sxs-lookup"><span data-stu-id="af75e-122">Byte</span></span>
- <span data-ttu-id="af75e-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="af75e-123">BigEndianUnicode</span></span>
- <span data-ttu-id="af75e-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="af75e-124">UTF8</span></span>
- <span data-ttu-id="af75e-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="af75e-125">UTF7</span></span>
- <span data-ttu-id="af75e-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="af75e-126">Ascii</span></span>
- <span data-ttu-id="af75e-127">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="af75e-127">Default</span></span>
- <span data-ttu-id="af75e-128">Oem</span><span class="sxs-lookup"><span data-stu-id="af75e-128">Oem</span></span>
- <span data-ttu-id="af75e-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="af75e-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="af75e-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="af75e-130">-Folder</span></span>
<span data-ttu-id="af75e-131">Указывает на то, что в результате этой операции создается папка.</span><span class="sxs-lookup"><span data-stu-id="af75e-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="af75e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="af75e-132">-Force</span></span>
<span data-ttu-id="af75e-133">Указывает на то, что данной операцией можно переписать элемент, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="af75e-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="af75e-134">-Path</span><span class="sxs-lookup"><span data-stu-id="af75e-134">-Path</span></span>
<span data-ttu-id="af75e-135">Путь к создаемой позиции в магазине данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="af75e-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="af75e-136">-Значение</span><span class="sxs-lookup"><span data-stu-id="af75e-136">-Value</span></span>
<span data-ttu-id="af75e-137">Определяет содержимое, которое нужно добавить к созда создаемому элементу.</span><span class="sxs-lookup"><span data-stu-id="af75e-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="af75e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af75e-138">-Confirm</span></span>
<span data-ttu-id="af75e-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="af75e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af75e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af75e-140">-WhatIf</span></span>
<span data-ttu-id="af75e-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af75e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af75e-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="af75e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af75e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af75e-143">CommonParameters</span></span>
<span data-ttu-id="af75e-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af75e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af75e-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af75e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af75e-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af75e-146">INPUTS</span></span>

### <span data-ttu-id="af75e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="af75e-147">System.String</span></span>

### <span data-ttu-id="af75e-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="af75e-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="af75e-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="af75e-149">System.Object</span></span>

### <span data-ttu-id="af75e-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="af75e-150">System.Text.Encoding</span></span>

### <span data-ttu-id="af75e-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af75e-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af75e-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af75e-152">OUTPUTS</span></span>

### <span data-ttu-id="af75e-153">System.String</span><span class="sxs-lookup"><span data-stu-id="af75e-153">System.String</span></span>

## <span data-ttu-id="af75e-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af75e-154">NOTES</span></span>

## <span data-ttu-id="af75e-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af75e-155">RELATED LINKS</span></span>

[<span data-ttu-id="af75e-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="af75e-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="af75e-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="af75e-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="af75e-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="af75e-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="af75e-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="af75e-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="af75e-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="af75e-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="af75e-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="af75e-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


