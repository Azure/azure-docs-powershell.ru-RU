---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077505"
---
# <span data-ttu-id="cee9f-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="cee9f-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="cee9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cee9f-102">SYNOPSIS</span></span>
<span data-ttu-id="cee9f-103">Восстановление учетной записи хранения для определенных диапазонов BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cee9f-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="cee9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cee9f-104">SYNTAX</span></span>

### <span data-ttu-id="cee9f-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cee9f-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee9f-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cee9f-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee9f-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cee9f-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee9f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cee9f-108">DESCRIPTION</span></span>
<span data-ttu-id="cee9f-109">Командлет **RESTORE-AzStorageBlobRange** восстанавливает большие двоичные объекты в учетной записи хранения для определенных диапазонов BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cee9f-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="cee9f-110">Начальный диапазон включается, а конечный диапазон исключается из восстановления большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="cee9f-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="cee9f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cee9f-111">EXAMPLES</span></span>

### <span data-ttu-id="cee9f-112">Пример 1: Start восстанавливает большие двоичные объекты в учетной записи хранения с определенным диапазоном BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cee9f-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
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

<span data-ttu-id="cee9f-113">Эта команда сначала создает диапазоны BLOB-объектов, а затем запускает восстановление больших двоичных объектов в учетной записи хранения с диапазоном больших двоичных объектов 2, начиная с 1 дня назад.</span><span class="sxs-lookup"><span data-stu-id="cee9f-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="cee9f-114">Вы можете использовать Get-AzStorageAccount для отслеживания состояния восстановления позже.</span><span class="sxs-lookup"><span data-stu-id="cee9f-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="cee9f-115">Пример 2: восстановление всех больших двоичных объектов в учетной записи хранения в серверной части</span><span class="sxs-lookup"><span data-stu-id="cee9f-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="cee9f-116">Эта команда восстанавливает все большие двоичные объекты в учетной записи хранения, начиная с 30 минут назад, и дождитесь завершения восстановления.</span><span class="sxs-lookup"><span data-stu-id="cee9f-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="cee9f-117">Так как восстановление больших двоичных объектов может занять много времени, запустите его в серверной части с параметром-AsJob, а затем дождитесь завершения задания и отобразите результат.</span><span class="sxs-lookup"><span data-stu-id="cee9f-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="cee9f-118">Пример 3: восстановление больших двоичных объектов путем ввода диапазонов больших двоичных объектов напрямую и ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="cee9f-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="cee9f-119">Эта команда восстанавливает большие двоичные объекты в учетной записи хранения, начиная с 1 дня назад, путем ввода диапазонов больших двоичных объектов непосредственно в командлет Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="cee9f-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="cee9f-120">Эта команда будет ожидать завершения восстановления.</span><span class="sxs-lookup"><span data-stu-id="cee9f-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="cee9f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cee9f-121">PARAMETERS</span></span>

### <span data-ttu-id="cee9f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cee9f-122">-AsJob</span></span>
<span data-ttu-id="cee9f-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cee9f-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cee9f-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="cee9f-124">-BlobRestoreRange</span></span>
<span data-ttu-id="cee9f-125">Диапазон больших двоичных объектов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="cee9f-125">The blob range to Restore.</span></span>
<span data-ttu-id="cee9f-126">Если этот параметр не указан, будут восстановлены все большие двоичные объекты.</span><span class="sxs-lookup"><span data-stu-id="cee9f-126">If not specify this parameter, will restore all blobs.</span></span>

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

### <span data-ttu-id="cee9f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee9f-127">-DefaultProfile</span></span>
<span data-ttu-id="cee9f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cee9f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cee9f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee9f-129">-ResourceGroupName</span></span>
<span data-ttu-id="cee9f-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cee9f-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="cee9f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cee9f-131">-ResourceId</span></span>
<span data-ttu-id="cee9f-132">Идентификатор ресурса учетной записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="cee9f-132">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="cee9f-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cee9f-133">-StorageAccount</span></span>
<span data-ttu-id="cee9f-134">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cee9f-134">Storage account object</span></span>

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

### <span data-ttu-id="cee9f-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cee9f-135">-StorageAccountName</span></span>
<span data-ttu-id="cee9f-136">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cee9f-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="cee9f-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="cee9f-137">-TimeToRestore</span></span>
<span data-ttu-id="cee9f-138">Время восстановления большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="cee9f-138">The Time to Restore Blob.</span></span>

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

### <span data-ttu-id="cee9f-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="cee9f-139">-WaitForComplete</span></span>
<span data-ttu-id="cee9f-140">Ожидание завершения задачи восстановления</span><span class="sxs-lookup"><span data-stu-id="cee9f-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="cee9f-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cee9f-141">-Confirm</span></span>
<span data-ttu-id="cee9f-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cee9f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cee9f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee9f-143">-WhatIf</span></span>
<span data-ttu-id="cee9f-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cee9f-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cee9f-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cee9f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cee9f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee9f-146">CommonParameters</span></span>
<span data-ttu-id="cee9f-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cee9f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee9f-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee9f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee9f-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cee9f-149">INPUTS</span></span>

### <span data-ttu-id="cee9f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cee9f-150">System.String</span></span>

### <span data-ttu-id="cee9f-151">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cee9f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="cee9f-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cee9f-152">OUTPUTS</span></span>

### <span data-ttu-id="cee9f-153">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="cee9f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="cee9f-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="cee9f-154">NOTES</span></span>

## <span data-ttu-id="cee9f-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cee9f-155">RELATED LINKS</span></span>
