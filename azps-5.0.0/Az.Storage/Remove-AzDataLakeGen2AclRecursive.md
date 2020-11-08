---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: cb2c409ae2bbe7734c433de74ef4a21c368221e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249341"
---
# <span data-ttu-id="3a930-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="3a930-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="3a930-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a930-102">SYNOPSIS</span></span>
<span data-ttu-id="3a930-103">Рекурсивно удалите список ACL по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="3a930-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="3a930-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a930-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a930-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a930-105">DESCRIPTION</span></span>
<span data-ttu-id="3a930-106">Командлет **recurs-AzDataLakeGen2AclRecursive** удаляет список ACL на заданном пути рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="3a930-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="3a930-107">Записи ACL в исходном списке ACL, которые имеют одинаковые AccessControlType, DefaultScope и EntityId с записями ACL ввода (даже с разными разрешениями) будет LBE удален.</span><span class="sxs-lookup"><span data-stu-id="3a930-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="3a930-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a930-108">EXAMPLES</span></span>

### <span data-ttu-id="3a930-109">Пример 1: рекурсивное удаление ACL для корневого directiry файловой системы</span><span class="sxs-lookup"><span data-stu-id="3a930-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl
PS C:\> Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="3a930-110">Эта команда сначала создает объект ACL с двумя записями ACL, а затем удаляет список управления доступом (ACL) в корневом каталоге файловой системы.</span><span class="sxs-lookup"><span data-stu-id="3a930-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="3a930-111">Пример 2: рекурсивное удаление списка управления доступом в каталоге</span><span class="sxs-lookup"><span data-stu-id="3a930-111">Example 2: Remove ACL recursively on a directory</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="3a930-112">Эта команда сначала удаляет список управления доступом (ACL) в каталоге и завершился сбоем, после чего возобновите ContinuationToken после того, как пользователь исправит неудачный файл.</span><span class="sxs-lookup"><span data-stu-id="3a930-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="3a930-113">Пример 3: удаление рекурсивного блока ACL с помощью блока</span><span class="sxs-lookup"><span data-stu-id="3a930-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 1000 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="3a930-114">Этот сценарий удаляет список ACL rescursively в блоке каталогов с помощью блока, в котором размер блока равен BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="3a930-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="3a930-115">Размер блока — 50000 в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="3a930-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="3a930-116">Пример 4: Удаление списка управления доступом (ACL) в каталоге и ContinueOnFailure, а затем возобновление из сбоев по одному</span><span class="sxs-lookup"><span data-stu-id="3a930-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="3a930-117">Эта команда сначала удаляет список ACL в каталог с ContinueOnFailure, а некоторые элементы произошел сбой, после чего возобновите неудачные элементы по одному.</span><span class="sxs-lookup"><span data-stu-id="3a930-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="3a930-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a930-118">PARAMETERS</span></span>

### <span data-ttu-id="3a930-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="3a930-119">-Acl</span></span>
<span data-ttu-id="3a930-120">Список управления доступом POSIX для рекурсивной настройки файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="3a930-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a930-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a930-121">-AsJob</span></span>
<span data-ttu-id="3a930-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3a930-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a930-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="3a930-123">-BatchSize</span></span>
<span data-ttu-id="3a930-124">Если размер множества данных превышает размер пакета, операция будет разбита на несколько запросов, чтобы можно было отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="3a930-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="3a930-125">Размер пакета должен составлять от 1 до 2000.</span><span class="sxs-lookup"><span data-stu-id="3a930-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="3a930-126">Значение по умолчанию — 2000.</span><span class="sxs-lookup"><span data-stu-id="3a930-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a930-127">-Context</span><span class="sxs-lookup"><span data-stu-id="3a930-127">-Context</span></span>
<span data-ttu-id="3a930-128">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="3a930-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="3a930-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="3a930-129">-ContinuationToken</span></span>
<span data-ttu-id="3a930-130">Маркер продолжения.</span><span class="sxs-lookup"><span data-stu-id="3a930-130">Continuation Token.</span></span>

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

### <span data-ttu-id="3a930-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="3a930-131">-ContinueOnFailure</span></span>
<span data-ttu-id="3a930-132">Установите этот параметр, чтобы игнорировать ошибки и продолжить proceeing с операцией с другими вложенными сущностями каталога.</span><span class="sxs-lookup"><span data-stu-id="3a930-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="3a930-133">По умолчанию операция будет быстро прервана при возникновении ошибок.</span><span class="sxs-lookup"><span data-stu-id="3a930-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="3a930-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a930-134">-DefaultProfile</span></span>
<span data-ttu-id="3a930-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a930-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a930-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="3a930-136">-FileSystem</span></span>
<span data-ttu-id="3a930-137">Имя файловой системы</span><span class="sxs-lookup"><span data-stu-id="3a930-137">FileSystem name</span></span>

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

### <span data-ttu-id="3a930-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="3a930-138">-MaxBatchCount</span></span>
<span data-ttu-id="3a930-139">Максимальное количество пакетов, которые могут быть выполнены с одной операцией управления доступом на изменение.</span><span class="sxs-lookup"><span data-stu-id="3a930-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="3a930-140">Если размер множества данных превышает MaxBatchCount умножить на BatchSize, маркер продолжения будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="3a930-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a930-141">-Path</span><span class="sxs-lookup"><span data-stu-id="3a930-141">-Path</span></span>
<span data-ttu-id="3a930-142">Путь в указанной файловой системе для рекурсивного изменения ACL.</span><span class="sxs-lookup"><span data-stu-id="3a930-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="3a930-143">Может быть файлом или каталогом.</span><span class="sxs-lookup"><span data-stu-id="3a930-143">Can be a file or directory.</span></span>
<span data-ttu-id="3a930-144">В формате "Directory/file.txt" или "Directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="3a930-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="3a930-145">Пропустить задать этот параметр для рекурсивного изменения ACL из корневого каталога файловой системы.</span><span class="sxs-lookup"><span data-stu-id="3a930-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="3a930-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a930-146">-Confirm</span></span>
<span data-ttu-id="3a930-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a930-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a930-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a930-148">-WhatIf</span></span>
<span data-ttu-id="3a930-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a930-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a930-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a930-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a930-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a930-151">CommonParameters</span></span>
<span data-ttu-id="3a930-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a930-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a930-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a930-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a930-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a930-154">INPUTS</span></span>

### <span data-ttu-id="3a930-155">System. String</span><span class="sxs-lookup"><span data-stu-id="3a930-155">System.String</span></span>

### <span data-ttu-id="3a930-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a930-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3a930-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a930-157">OUTPUTS</span></span>

### <span data-ttu-id="3a930-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3a930-158">System.String</span></span>

## <span data-ttu-id="3a930-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a930-159">NOTES</span></span>

## <span data-ttu-id="3a930-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a930-160">RELATED LINKS</span></span>
