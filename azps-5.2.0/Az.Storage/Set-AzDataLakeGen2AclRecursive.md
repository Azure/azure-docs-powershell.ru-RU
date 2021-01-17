---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 1d2a4bc1dd9dab05e56f8b69c92d98985cf98e15
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403372"
---
# <span data-ttu-id="0e63d-101">Set-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="0e63d-101">Set-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="0e63d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e63d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e63d-103">Задан рекурсивно заданный путь к ACL.</span><span class="sxs-lookup"><span data-stu-id="0e63d-103">Set ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="0e63d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0e63d-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e63d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e63d-105">DESCRIPTION</span></span>
<span data-ttu-id="0e63d-106">Для этого задан рекурсивный набор ACL-2AclRecursive cmdlet **Set-AzDataLakeGen2AclRecursive.**</span><span class="sxs-lookup"><span data-stu-id="0e63d-106">The **Set-AzDataLakeGen2AclRecursive** cmdlet sets ACL recursively on the specified path.</span></span> <span data-ttu-id="0e63d-107">Входной ACL полностью заменит исходный ACL.</span><span class="sxs-lookup"><span data-stu-id="0e63d-107">The input ACL will replace original ACL completely.</span></span>

## <span data-ttu-id="0e63d-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0e63d-108">EXAMPLES</span></span>

### <span data-ttu-id="0e63d-109">Пример 1. Рекурсивное настройка ACL для прямого выбора</span><span class="sxs-lookup"><span data-stu-id="0e63d-109">Example 1: Set ACL recursively on a directiry</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="0e63d-110">Эта команда сначала создает объект ACL с 3 записями acl, а затем рекурсивно настраивает ACL в каталоге.</span><span class="sxs-lookup"><span data-stu-id="0e63d-110">This command first creates an ACL object with 3 acl entries, then sets ACL recursively on a directory.</span></span>

### <span data-ttu-id="0e63d-111">Пример 2. Рекурсивное настройка ACL для корневого прямого выбора filesystem</span><span class="sxs-lookup"><span data-stu-id="0e63d-111">Example 2: Set ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="0e63d-112">Эта команда сначала задает ACL рекурсивно в корневом каталоге и не удается, а затем возобновляется с помощью ContinuationToken после исправления пользователем сбойного файла.</span><span class="sxs-lookup"><span data-stu-id="0e63d-112">This command first sets ACL recursively to a root directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="0e63d-113">Пример 3. Настройка aCL, рекурсивно блок-блоков</span><span class="sxs-lookup"><span data-stu-id="0e63d-113">Example 3: Set ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 2 -ContinuationToken $token -Context $ctx

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

<span data-ttu-id="0e63d-114">Этот сценарий задает рекурсивно aCL на фрагментах каталога по блоков с размером блоков как BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="0e63d-114">This script sets ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="0e63d-115">В этом сценарии размер блоков составляет 200.</span><span class="sxs-lookup"><span data-stu-id="0e63d-115">Chunk size is 200 in this script.</span></span>

### <span data-ttu-id="0e63d-116">Пример 4. Рекурсивное настройка ACL для каталога и ContinueOnFailure, а затем резюме из сбоев по одному</span><span class="sxs-lookup"><span data-stu-id="0e63d-116">Example 4: Set ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="0e63d-117">Эта команда сначала задает рекурсивный ACL каталог с ContinueOnFailure, после чего некоторые элементы не удалось, а затем возобновляют их по одному.</span><span class="sxs-lookup"><span data-stu-id="0e63d-117">This command first sets ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="0e63d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e63d-118">PARAMETERS</span></span>

### <span data-ttu-id="0e63d-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="0e63d-119">-Acl</span></span>
<span data-ttu-id="0e63d-120">Список управления доступом POSIX для рекурсивного набора для файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="0e63d-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="0e63d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e63d-121">-AsJob</span></span>
<span data-ttu-id="0e63d-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0e63d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e63d-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="0e63d-123">-BatchSize</span></span>
<span data-ttu-id="0e63d-124">Если размер набора данных превышает размер пакета, операция будет разделена на несколько запросов, чтобы можно было отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="0e63d-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="0e63d-125">Пакет может иметь размер от 1 до 2000.</span><span class="sxs-lookup"><span data-stu-id="0e63d-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="0e63d-126">Значение по умолчанию — 2000.</span><span class="sxs-lookup"><span data-stu-id="0e63d-126">Default is 2000.</span></span>

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

### <span data-ttu-id="0e63d-127">-Контекст</span><span class="sxs-lookup"><span data-stu-id="0e63d-127">-Context</span></span>
<span data-ttu-id="0e63d-128">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="0e63d-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="0e63d-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="0e63d-129">-ContinuationToken</span></span>
<span data-ttu-id="0e63d-130">Маркер продолжения.</span><span class="sxs-lookup"><span data-stu-id="0e63d-130">Continuation Token.</span></span>

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

### <span data-ttu-id="0e63d-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="0e63d-131">-ContinueOnFailure</span></span>
<span data-ttu-id="0e63d-132">С помощью этого параметра можно игнорировать сбои и продолжить операцию над другими подущностями каталога.</span><span class="sxs-lookup"><span data-stu-id="0e63d-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="0e63d-133">По умолчанию операция быстро завершается при сбоях.</span><span class="sxs-lookup"><span data-stu-id="0e63d-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="0e63d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e63d-134">-DefaultProfile</span></span>
<span data-ttu-id="0e63d-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e63d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e63d-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="0e63d-136">-FileSystem</span></span>
<span data-ttu-id="0e63d-137">Имя FileSystem</span><span class="sxs-lookup"><span data-stu-id="0e63d-137">FileSystem name</span></span>

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

### <span data-ttu-id="0e63d-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="0e63d-138">-MaxBatchCount</span></span>
<span data-ttu-id="0e63d-139">Максимальное количество пакетов, которые можно выполнить с одним изменением access Control.</span><span class="sxs-lookup"><span data-stu-id="0e63d-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="0e63d-140">Если размер набора данных превышает умножение MaxBatchCount BatchSize, возвращается маркер продолжения.</span><span class="sxs-lookup"><span data-stu-id="0e63d-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="0e63d-141">-Path</span><span class="sxs-lookup"><span data-stu-id="0e63d-141">-Path</span></span>
<span data-ttu-id="0e63d-142">Путь в указанной FileSystem, который нужно рекурсивно изменить.</span><span class="sxs-lookup"><span data-stu-id="0e63d-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="0e63d-143">Может быть файлом или каталогом.</span><span class="sxs-lookup"><span data-stu-id="0e63d-143">Can be a file or directory.</span></span>
<span data-ttu-id="0e63d-144">В формате "каталог/file.txt" или "каталог1/каталог2/".</span><span class="sxs-lookup"><span data-stu-id="0e63d-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="0e63d-145">Пропустите этот параметр, чтобы рекурсивно изменить Acl из корневого каталога Filesystem.</span><span class="sxs-lookup"><span data-stu-id="0e63d-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="0e63d-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e63d-146">-Confirm</span></span>
<span data-ttu-id="0e63d-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0e63d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e63d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e63d-148">-WhatIf</span></span>
<span data-ttu-id="0e63d-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e63d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e63d-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0e63d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e63d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e63d-151">CommonParameters</span></span>
<span data-ttu-id="0e63d-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e63d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e63d-153">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e63d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e63d-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e63d-154">INPUTS</span></span>

### <span data-ttu-id="0e63d-155">System.String</span><span class="sxs-lookup"><span data-stu-id="0e63d-155">System.String</span></span>

### <span data-ttu-id="0e63d-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0e63d-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0e63d-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e63d-157">OUTPUTS</span></span>

### <span data-ttu-id="0e63d-158">System.String</span><span class="sxs-lookup"><span data-stu-id="0e63d-158">System.String</span></span>

## <span data-ttu-id="0e63d-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0e63d-159">NOTES</span></span>

## <span data-ttu-id="0e63d-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e63d-160">RELATED LINKS</span></span>
