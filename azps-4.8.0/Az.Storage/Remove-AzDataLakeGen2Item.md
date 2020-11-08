---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236543"
---
# <span data-ttu-id="fc78f-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="fc78f-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="fc78f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc78f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc78f-103">Удаление файла или папки.</span><span class="sxs-lookup"><span data-stu-id="fc78f-103">Remove a file or directory.</span></span>

## <span data-ttu-id="fc78f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc78f-104">SYNTAX</span></span>

### <span data-ttu-id="fc78f-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc78f-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc78f-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="fc78f-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc78f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc78f-107">DESCRIPTION</span></span>
<span data-ttu-id="fc78f-108">Командлет **Remove-AzDataLakeGen2Item** удаляет файл или каталог из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fc78f-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="fc78f-109">Этот командлет работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="fc78f-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="fc78f-110">Учетную запись такого типа можно создать с помощью командлета New-AzStorageAccount с параметром-EnableHierarchicalNamespace $true.</span><span class="sxs-lookup"><span data-stu-id="fc78f-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="fc78f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc78f-111">EXAMPLES</span></span>

### <span data-ttu-id="fc78f-112">Пример 1: Удаление каталога</span><span class="sxs-lookup"><span data-stu-id="fc78f-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="fc78f-113">Эта команда удаляет каталог из файловой системы.</span><span class="sxs-lookup"><span data-stu-id="fc78f-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="fc78f-114">Пример 2: удаление файла без запроса</span><span class="sxs-lookup"><span data-stu-id="fc78f-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="fc78f-115">Эта команда удаляет каталог из файловой системы без запроса.</span><span class="sxs-lookup"><span data-stu-id="fc78f-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="fc78f-116">Пример 3: удаление всех элементов в файловой системе с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="fc78f-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="fc78f-117">Эта команда удаляет все элементы в файловой системе с конвейером.</span><span class="sxs-lookup"><span data-stu-id="fc78f-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="fc78f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc78f-118">PARAMETERS</span></span>

### <span data-ttu-id="fc78f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc78f-119">-AsJob</span></span>
<span data-ttu-id="fc78f-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fc78f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc78f-121">-Context</span><span class="sxs-lookup"><span data-stu-id="fc78f-121">-Context</span></span>
<span data-ttu-id="fc78f-122">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="fc78f-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="fc78f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc78f-123">-DefaultProfile</span></span>
<span data-ttu-id="fc78f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc78f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc78f-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="fc78f-125">-FileSystem</span></span>
<span data-ttu-id="fc78f-126">Имя файловой системы</span><span class="sxs-lookup"><span data-stu-id="fc78f-126">FileSystem name</span></span>

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

### <span data-ttu-id="fc78f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="fc78f-127">-Force</span></span>
<span data-ttu-id="fc78f-128">Принудительное удаление файловой системы и всего содержимого</span><span class="sxs-lookup"><span data-stu-id="fc78f-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="fc78f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc78f-129">-InputObject</span></span>
<span data-ttu-id="fc78f-130">Объект Azure Gen2 Item, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fc78f-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="fc78f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc78f-131">-PassThru</span></span>
<span data-ttu-id="fc78f-132">Возвращение того, успешно ли удалена указанная файловая система</span><span class="sxs-lookup"><span data-stu-id="fc78f-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="fc78f-133">-Path</span><span class="sxs-lookup"><span data-stu-id="fc78f-133">-Path</span></span>
<span data-ttu-id="fc78f-134">Путь в указанной файловой системе, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fc78f-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="fc78f-135">Может быть файлом или каталогом в формате "Directory/file.txt" или "Directory1/Directory2/"</span><span class="sxs-lookup"><span data-stu-id="fc78f-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="fc78f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc78f-136">-Confirm</span></span>
<span data-ttu-id="fc78f-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc78f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc78f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc78f-138">-WhatIf</span></span>
<span data-ttu-id="fc78f-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc78f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc78f-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc78f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc78f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc78f-141">CommonParameters</span></span>
<span data-ttu-id="fc78f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc78f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc78f-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc78f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc78f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc78f-144">INPUTS</span></span>

### <span data-ttu-id="fc78f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="fc78f-145">System.String</span></span>

### <span data-ttu-id="fc78f-146">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="fc78f-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="fc78f-147">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fc78f-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fc78f-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc78f-148">OUTPUTS</span></span>

### <span data-ttu-id="fc78f-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc78f-149">System.Boolean</span></span>

## <span data-ttu-id="fc78f-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc78f-150">NOTES</span></span>

## <span data-ttu-id="fc78f-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc78f-151">RELATED LINKS</span></span>