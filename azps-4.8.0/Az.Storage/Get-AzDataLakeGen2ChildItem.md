---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080188"
---
# <span data-ttu-id="35e65-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="35e65-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="35e65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35e65-102">SYNOPSIS</span></span>
<span data-ttu-id="35e65-103">Перечисление подкаталогов и файлов из корневой папки или из корня файловой системы.</span><span class="sxs-lookup"><span data-stu-id="35e65-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="35e65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35e65-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35e65-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35e65-105">DESCRIPTION</span></span>
<span data-ttu-id="35e65-106">Командлет **Get-AzDataLakeGen2ChildItem** включает в себя подкаталоги и файлы в каталоге или файловой системе учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="35e65-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="35e65-107">Этот командлет работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="35e65-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="35e65-108">Учетную запись такого типа можно создать с помощью командлета New-AzStorageAccount с параметром-EnableHierarchicalNamespace $true.</span><span class="sxs-lookup"><span data-stu-id="35e65-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="35e65-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35e65-109">EXAMPLES</span></span>

### <span data-ttu-id="35e65-110">Пример 1: список прямых вложенных элементов из файловой системы</span><span class="sxs-lookup"><span data-stu-id="35e65-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="35e65-111">Эта команда перечисляет прямые подразделы в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="35e65-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="35e65-112">Пример 2: рекурсивный список из каталога и выбор свойств и ACL</span><span class="sxs-lookup"><span data-stu-id="35e65-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="35e65-113">Эта команда перечисляет прямые подразделы в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="35e65-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="35e65-114">Пример 3: рекурсивное перечисление элементов из файловой системы в нескольких пакетах</span><span class="sxs-lookup"><span data-stu-id="35e65-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
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

<span data-ttu-id="35e65-115">В этом примере параметры *maxcount* и *ContinuationToken* используются для рекурсивного перечисления элементов из файловой системы в нескольких пакетах.</span><span class="sxs-lookup"><span data-stu-id="35e65-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="35e65-116">Первые четыре команды назначают значения переменным для использования в примере.</span><span class="sxs-lookup"><span data-stu-id="35e65-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="35e65-117">Пятая команда задает оператор **Do-** in, использующий командлет **Get-AzDataLakeGen2ChildItem** для элементов списка.</span><span class="sxs-lookup"><span data-stu-id="35e65-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="35e65-118">Оператор включает токен продолжения, хранящийся в переменной $Token.</span><span class="sxs-lookup"><span data-stu-id="35e65-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="35e65-119">$Token изменения значения по мере выполнения цикла.</span><span class="sxs-lookup"><span data-stu-id="35e65-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="35e65-120">В последней команде используется команда **echo** для отображения итогового значения.</span><span class="sxs-lookup"><span data-stu-id="35e65-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="35e65-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35e65-121">PARAMETERS</span></span>

### <span data-ttu-id="35e65-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35e65-122">-AsJob</span></span>
<span data-ttu-id="35e65-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="35e65-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35e65-124">-Context</span><span class="sxs-lookup"><span data-stu-id="35e65-124">-Context</span></span>
<span data-ttu-id="35e65-125">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="35e65-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="35e65-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="35e65-126">-ContinuationToken</span></span>
<span data-ttu-id="35e65-127">Маркер продолжения.</span><span class="sxs-lookup"><span data-stu-id="35e65-127">Continuation Token.</span></span>

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

### <span data-ttu-id="35e65-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e65-128">-DefaultProfile</span></span>
<span data-ttu-id="35e65-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35e65-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35e65-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="35e65-130">-FetchProperty</span></span>
<span data-ttu-id="35e65-131">Получение свойств и списка ACL для DataItem.</span><span class="sxs-lookup"><span data-stu-id="35e65-131">Fetch the datalake item properties and ACL.</span></span>

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

### <span data-ttu-id="35e65-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="35e65-132">-FileSystem</span></span>
<span data-ttu-id="35e65-133">Имя файловой системы</span><span class="sxs-lookup"><span data-stu-id="35e65-133">FileSystem name</span></span>

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

### <span data-ttu-id="35e65-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="35e65-134">-MaxCount</span></span>
<span data-ttu-id="35e65-135">Максимальное количество больших двоичных объектов, которые могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="35e65-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="35e65-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="35e65-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="35e65-137">Если speicify этот параметр, значения идентификаторов пользователей, возвращаемые в полях владелец и группа каждого элемента списка, будут преобразованы из идентификаторов объектов Azure Active Directory в имена участников-пользователей.</span><span class="sxs-lookup"><span data-stu-id="35e65-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="35e65-138">Если этот параметр не speicify, значения будут возвращены как идентификаторы объектов Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="35e65-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="35e65-139">Обратите внимание, что идентификаторы объектов Group и Application не переводятся, так как они не имеют уникальных понятных имен.</span><span class="sxs-lookup"><span data-stu-id="35e65-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

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

### <span data-ttu-id="35e65-140">-Path</span><span class="sxs-lookup"><span data-stu-id="35e65-140">-Path</span></span>
<span data-ttu-id="35e65-141">Путь в указанной файловой системе, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="35e65-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="35e65-142">Должен быть каталогом в формате "Directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="35e65-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="35e65-143">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="35e65-143">-Recurse</span></span>
<span data-ttu-id="35e65-144">Указывает, будет ли рекурсивно получен дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="35e65-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="35e65-145">По умолчанию используется значение false.</span><span class="sxs-lookup"><span data-stu-id="35e65-145">The default is false.</span></span>

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

### <span data-ttu-id="35e65-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e65-146">CommonParameters</span></span>
<span data-ttu-id="35e65-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35e65-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e65-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35e65-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e65-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35e65-149">INPUTS</span></span>

### <span data-ttu-id="35e65-150">System. String</span><span class="sxs-lookup"><span data-stu-id="35e65-150">System.String</span></span>

### <span data-ttu-id="35e65-151">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="35e65-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="35e65-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35e65-152">OUTPUTS</span></span>

### <span data-ttu-id="35e65-153">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="35e65-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="35e65-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="35e65-154">NOTES</span></span>

## <span data-ttu-id="35e65-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35e65-155">RELATED LINKS</span></span>
