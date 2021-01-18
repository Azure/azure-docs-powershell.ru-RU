---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517045"
---
# <span data-ttu-id="88273-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="88273-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="88273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88273-102">SYNOPSIS</span></span>
<span data-ttu-id="88273-103">Удаление файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="88273-103">Remove a file or directory.</span></span>

## <span data-ttu-id="88273-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88273-104">SYNTAX</span></span>

### <span data-ttu-id="88273-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88273-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88273-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="88273-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88273-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88273-107">DESCRIPTION</span></span>
<span data-ttu-id="88273-108">Для удаления файла или каталога из учетной записи хранения удаляется файл или каталог Из **azDataLakeGen2Item.**</span><span class="sxs-lookup"><span data-stu-id="88273-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="88273-109">Этот cmdlet работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="88273-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="88273-110">Учетную запись такого типа можно создать с помощью cmdlet "New-AzStorageAccount" с помощью функции "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="88273-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="88273-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88273-111">EXAMPLES</span></span>

### <span data-ttu-id="88273-112">Пример 1. Удаление каталога</span><span class="sxs-lookup"><span data-stu-id="88273-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="88273-113">Эта команда удаляет каталог из Filesystem.</span><span class="sxs-lookup"><span data-stu-id="88273-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="88273-114">Пример 2. Удаление файла без запроса</span><span class="sxs-lookup"><span data-stu-id="88273-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="88273-115">Эта команда удаляет каталог из Filesystem без запроса.</span><span class="sxs-lookup"><span data-stu-id="88273-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="88273-116">Пример 3. Удаление всех элементов в filesystem с конвейером</span><span class="sxs-lookup"><span data-stu-id="88273-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="88273-117">Эта команда удаляет все элементы в filesystem с конвейером.</span><span class="sxs-lookup"><span data-stu-id="88273-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="88273-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88273-118">PARAMETERS</span></span>

### <span data-ttu-id="88273-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88273-119">-AsJob</span></span>
<span data-ttu-id="88273-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="88273-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88273-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="88273-121">-Context</span></span>
<span data-ttu-id="88273-122">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="88273-122">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88273-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88273-123">-DefaultProfile</span></span>
<span data-ttu-id="88273-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88273-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88273-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="88273-125">-FileSystem</span></span>
<span data-ttu-id="88273-126">Имя FileSystem</span><span class="sxs-lookup"><span data-stu-id="88273-126">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88273-127">-Force</span><span class="sxs-lookup"><span data-stu-id="88273-127">-Force</span></span>
<span data-ttu-id="88273-128">Принудительное удаление Filesystem и всего содержимого в ней</span><span class="sxs-lookup"><span data-stu-id="88273-128">Force to remove the Filesystem and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88273-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88273-129">-InputObject</span></span>
<span data-ttu-id="88273-130">Объект Элемента Azure Datalake Gen2, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="88273-130">Azure Datalake Gen2 Item Object to remove.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88273-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88273-131">-PassThru</span></span>
<span data-ttu-id="88273-132">Возвращает, успешно ли удалена указанная система Файлов.</span><span class="sxs-lookup"><span data-stu-id="88273-132">Return whether the specified Filesystem is successfully removed</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88273-133">-Path</span><span class="sxs-lookup"><span data-stu-id="88273-133">-Path</span></span>
<span data-ttu-id="88273-134">Путь в указанной Filesystem, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="88273-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="88273-135">Может быть файлом или каталогом в формате "каталог/file.txt" или "каталог1/каталог2/".</span><span class="sxs-lookup"><span data-stu-id="88273-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88273-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88273-136">-Confirm</span></span>
<span data-ttu-id="88273-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88273-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88273-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88273-138">-WhatIf</span></span>
<span data-ttu-id="88273-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88273-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88273-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="88273-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88273-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88273-141">CommonParameters</span></span>
<span data-ttu-id="88273-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88273-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88273-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88273-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88273-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88273-144">INPUTS</span></span>

### <span data-ttu-id="88273-145">System.String</span><span class="sxs-lookup"><span data-stu-id="88273-145">System.String</span></span>

### <span data-ttu-id="88273-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="88273-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="88273-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88273-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88273-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88273-148">OUTPUTS</span></span>

### <span data-ttu-id="88273-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88273-149">System.Boolean</span></span>

## <span data-ttu-id="88273-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88273-150">NOTES</span></span>

## <span data-ttu-id="88273-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88273-151">RELATED LINKS</span></span>
