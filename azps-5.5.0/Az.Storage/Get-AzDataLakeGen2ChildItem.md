---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221905"
---
# <span data-ttu-id="b00a1-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="b00a1-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="b00a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b00a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b00a1-103">Содержит список под каталогов и файлов из корневого каталога или файловой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="b00a1-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="b00a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b00a1-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b00a1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b00a1-105">DESCRIPTION</span></span>
<span data-ttu-id="b00a1-106">Для **этого с** его учетной записью можно получить список подзаголовков и файлов в каталоге или Filesystem.</span><span class="sxs-lookup"><span data-stu-id="b00a1-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="b00a1-107">Этот cmdlet работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="b00a1-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="b00a1-108">Учетную запись такого типа можно создать с помощью cmdlet "New-AzStorageAccount" с помощью функции "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="b00a1-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="b00a1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b00a1-109">EXAMPLES</span></span>

### <span data-ttu-id="b00a1-110">Пример 1. Список прямых в подсистеме Файлов</span><span class="sxs-lookup"><span data-stu-id="b00a1-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="b00a1-111">Эта команда содержит список непосредственных подсистемы файлов</span><span class="sxs-lookup"><span data-stu-id="b00a1-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="b00a1-112">Пример 2. Рекурсивный список из каталога и извлечение свойств/ACL</span><span class="sxs-lookup"><span data-stu-id="b00a1-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="b00a1-113">Эта команда содержит список непосредственных подсистемы файлов</span><span class="sxs-lookup"><span data-stu-id="b00a1-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="b00a1-114">Пример 3. Элементы списка, рекурсивные с filesystem, в нескольких пакетах</span><span class="sxs-lookup"><span data-stu-id="b00a1-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="b00a1-115">В этом примере *параметры MaxCount* и *ContinuationToken* используются для рекурсивного списка элементов из Filesystem в нескольких пакетах.</span><span class="sxs-lookup"><span data-stu-id="b00a1-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="b00a1-116">Первые четыре команды присваивают значения переменным, которые используются в примере.</span><span class="sxs-lookup"><span data-stu-id="b00a1-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="b00a1-117">Пятая команда указывает на команду **Do-While,** в которую для элементов списка используется командлет **Get-AzDataLakeGen2ChildItem.**</span><span class="sxs-lookup"><span data-stu-id="b00a1-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="b00a1-118">Она включает маркер продолжения, который хранится в переменной $Token продолжения.</span><span class="sxs-lookup"><span data-stu-id="b00a1-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="b00a1-119">$Token изменяет значение по мере его цикла.</span><span class="sxs-lookup"><span data-stu-id="b00a1-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="b00a1-120">Для отображения итогового числа в конечной команде используется команда **Echo.**</span><span class="sxs-lookup"><span data-stu-id="b00a1-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="b00a1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b00a1-121">PARAMETERS</span></span>

### <span data-ttu-id="b00a1-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b00a1-122">-AsJob</span></span>
<span data-ttu-id="b00a1-123">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b00a1-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b00a1-124">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b00a1-124">-Context</span></span>
<span data-ttu-id="b00a1-125">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b00a1-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b00a1-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b00a1-126">-ContinuationToken</span></span>
<span data-ttu-id="b00a1-127">Маркер продолжения.</span><span class="sxs-lookup"><span data-stu-id="b00a1-127">Continuation Token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00a1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00a1-128">-DefaultProfile</span></span>
<span data-ttu-id="b00a1-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b00a1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b00a1-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="b00a1-130">-FetchProperty</span></span>
<span data-ttu-id="b00a1-131">Получить свойства элемента в области данных и получить ACL.</span><span class="sxs-lookup"><span data-stu-id="b00a1-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00a1-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b00a1-132">-FileSystem</span></span>
<span data-ttu-id="b00a1-133">Имя FileSystem</span><span class="sxs-lookup"><span data-stu-id="b00a1-133">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b00a1-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b00a1-134">-MaxCount</span></span>
<span data-ttu-id="b00a1-135">Максимальное количество возвращаемого BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="b00a1-135">The max count of the blobs that can return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00a1-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b00a1-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="b00a1-137">Если задан этот параметр, значения идентификаторов пользователей, возвращаемые в полях владельца и группы каждой записи списка, будут преобразованы из идентификаторов объектов Azure Active Directory в имена участников-пользователей.</span><span class="sxs-lookup"><span data-stu-id="b00a1-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="b00a1-138">Если значение этого параметра не задано, значения возвращаются как ИД объектов Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b00a1-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="b00a1-139">Обратите внимание на то, что группы и ИД объектов приложения не переводятся, так как у них нет уникальных имен.</span><span class="sxs-lookup"><span data-stu-id="b00a1-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00a1-140">-Path</span><span class="sxs-lookup"><span data-stu-id="b00a1-140">-Path</span></span>
<span data-ttu-id="b00a1-141">Путь в указанной Filesystem, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="b00a1-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="b00a1-142">Должен быть каталогом в формате "каталог1/каталог2/".</span><span class="sxs-lookup"><span data-stu-id="b00a1-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b00a1-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="b00a1-143">-Recurse</span></span>
<span data-ttu-id="b00a1-144">Указывает на то, будет ли элемент рекурсивно получать элемент ребенка.</span><span class="sxs-lookup"><span data-stu-id="b00a1-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="b00a1-145">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="b00a1-145">The default is false.</span></span>

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

### <span data-ttu-id="b00a1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00a1-146">CommonParameters</span></span>
<span data-ttu-id="b00a1-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00a1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00a1-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00a1-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00a1-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b00a1-149">INPUTS</span></span>

### <span data-ttu-id="b00a1-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b00a1-150">System.String</span></span>

### <span data-ttu-id="b00a1-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b00a1-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b00a1-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b00a1-152">OUTPUTS</span></span>

### <span data-ttu-id="b00a1-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b00a1-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="b00a1-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b00a1-154">NOTES</span></span>

## <span data-ttu-id="b00a1-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b00a1-155">RELATED LINKS</span></span>
