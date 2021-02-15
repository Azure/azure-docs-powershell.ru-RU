---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224796"
---
# <span data-ttu-id="b22e5-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="b22e5-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="b22e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b22e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b22e5-103">Восстановление учетной записи хранения для определенных диапазонов BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="b22e5-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="b22e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b22e5-104">SYNTAX</span></span>

### <span data-ttu-id="b22e5-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b22e5-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22e5-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="b22e5-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22e5-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b22e5-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b22e5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b22e5-108">DESCRIPTION</span></span>
<span data-ttu-id="b22e5-109">Для определенных диапазонов BLOB-lob-хранилищ с их учетной записью восстанавливается cmdlet **Restore-AzStorageBlobRange.**</span><span class="sxs-lookup"><span data-stu-id="b22e5-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="b22e5-110">Включается диапазон начала, а конечный диапазон исключается при восстановлении BLOB-вообще.</span><span class="sxs-lookup"><span data-stu-id="b22e5-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="b22e5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b22e5-111">EXAMPLES</span></span>

### <span data-ttu-id="b22e5-112">Пример 1. Запуск восстановления BLOB-в учетной записи хранения с определенными диапазонами lob-lob</span><span class="sxs-lookup"><span data-stu-id="b22e5-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="b22e5-113">Эта команда сначала создает два диапазона BLOB-хранилищ, а затем восстанавливает их в учетной записи хранения с 2 диапазонами BLOB-хранилищ, диапазонами от 1 дня до этого.</span><span class="sxs-lookup"><span data-stu-id="b22e5-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="b22e5-114">Пользователь может использовать Get-AzStorageAccount для отслеживания состояния восстановления позже.</span><span class="sxs-lookup"><span data-stu-id="b22e5-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="b22e5-115">Пример 2. Восстановление всех BLOB-ветвей в учетной записи хранения в backend</span><span class="sxs-lookup"><span data-stu-id="b22e5-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="b22e5-116">Эта команда восстанавливает все большой объем в учетной записи хранения за 30 минут до завершения восстановления.</span><span class="sxs-lookup"><span data-stu-id="b22e5-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="b22e5-117">Так как восстановление большой части lob-параметров может занять много времени, выполните ее в backend с параметром -Asjob, а затем дождись завершения задания и откажите результат.</span><span class="sxs-lookup"><span data-stu-id="b22e5-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="b22e5-118">Пример 3. Восстановление BLOB-ресурсов непосредственно по входным диапазонам BLOB-ресурсов и ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="b22e5-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="b22e5-119">Эта команда восстанавливает BLOB-данные учетной записи хранения с 1 дня назад путем ввода 2 диапазонов BLOB-Restore-AzStorageBlobRange в командлет.</span><span class="sxs-lookup"><span data-stu-id="b22e5-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="b22e5-120">Эта команда будет ждать завершения восстановления.</span><span class="sxs-lookup"><span data-stu-id="b22e5-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="b22e5-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b22e5-121">PARAMETERS</span></span>

### <span data-ttu-id="b22e5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b22e5-122">-AsJob</span></span>
<span data-ttu-id="b22e5-123">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b22e5-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b22e5-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="b22e5-124">-BlobRestoreRange</span></span>
<span data-ttu-id="b22e5-125">Диапазон BLOB-то, который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="b22e5-125">The blob range to Restore.</span></span>
<span data-ttu-id="b22e5-126">Если этот параметр не задан, будут восстановлены все BLOB-lob-lob.</span><span class="sxs-lookup"><span data-stu-id="b22e5-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22e5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22e5-127">-DefaultProfile</span></span>
<span data-ttu-id="b22e5-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b22e5-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22e5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22e5-129">-ResourceGroupName</span></span>
<span data-ttu-id="b22e5-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b22e5-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22e5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b22e5-131">-ResourceId</span></span>
<span data-ttu-id="b22e5-132">ИД ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b22e5-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22e5-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b22e5-133">-StorageAccount</span></span>
<span data-ttu-id="b22e5-134">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b22e5-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22e5-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b22e5-135">-StorageAccountName</span></span>
<span data-ttu-id="b22e5-136">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b22e5-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22e5-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="b22e5-137">-TimeToRestore</span></span>
<span data-ttu-id="b22e5-138">Время для восстановления BLOB-lob.</span><span class="sxs-lookup"><span data-stu-id="b22e5-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22e5-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b22e5-139">-WaitForComplete</span></span>
<span data-ttu-id="b22e5-140">Ожидание завершения задачи восстановления</span><span class="sxs-lookup"><span data-stu-id="b22e5-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="b22e5-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b22e5-141">-Confirm</span></span>
<span data-ttu-id="b22e5-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b22e5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b22e5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22e5-143">-WhatIf</span></span>
<span data-ttu-id="b22e5-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b22e5-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b22e5-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b22e5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b22e5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22e5-146">CommonParameters</span></span>
<span data-ttu-id="b22e5-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22e5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22e5-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b22e5-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22e5-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b22e5-149">INPUTS</span></span>

### <span data-ttu-id="b22e5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b22e5-150">System.String</span></span>

### <span data-ttu-id="b22e5-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b22e5-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b22e5-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b22e5-152">OUTPUTS</span></span>

### <span data-ttu-id="b22e5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="b22e5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="b22e5-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b22e5-154">NOTES</span></span>

## <span data-ttu-id="b22e5-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b22e5-155">RELATED LINKS</span></span>
