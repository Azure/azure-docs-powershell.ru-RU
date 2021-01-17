---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420047"
---
# <span data-ttu-id="b1c4a-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="b1c4a-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="b1c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c4a-103">Вызывает отбой для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="b1c4a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1c4a-104">SYNTAX</span></span>

### <span data-ttu-id="b1c4a-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1c4a-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c4a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b1c4a-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1c4a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="b1c4a-108">Вызывает отбой для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="b1c4a-109">В случае проблем с доступностью для учетной записи хранения может срабатывает запрос на отсчет.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="b1c4a-110">Отбой происходит из основного кластера учетной записи хранилища и дополнительного кластера для учетных записей RA-GRS.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="b1c4a-111">Дополнительный кластер станет основным после отбойной передачи.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="b1c4a-112">Прежде чем инициировать отбой 1.1, следует понять, как это повлияет на вашу учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="b1c4a-113">Проверьте время последней синхронизации, используя статистику служб BLOB-файлов https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) (GET Table Service Stats) и https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) GET Queue Service Stats https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) (для вашей учетной записи).</span><span class="sxs-lookup"><span data-stu-id="b1c4a-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="b1c4a-114">Это данные, которые могут быть потеряете, если вы инициируете отбой.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="b1c4a-115">2. После отсчета тип учетной записи хранения будет преобразован в локально избыточное хранилище (LRS).</span><span class="sxs-lookup"><span data-stu-id="b1c4a-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="b1c4a-116">Вы можете преобразовать свою учетную запись, чтобы использовать гео-избыточное хранилище (GRS).</span><span class="sxs-lookup"><span data-stu-id="b1c4a-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="b1c4a-117">3. После повторного включить grS для учетной записи хранения Майкрософт реплицирует данные в новый дополнительный регион.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="b1c4a-118">Время репликации зависит от объема реплицируемых данных.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="b1c4a-119">Обратите внимание, что за загрузку загрузок взимается плата за пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="b1c4a-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="b1c4a-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="b1c4a-121">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1c4a-121">EXAMPLES</span></span>

### <span data-ttu-id="b1c4a-122">Пример 1. Отбой вызова учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b1c4a-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="b1c4a-123">Эта команда проверяет время последней синхронизации учетной записи хранения, а затем вызывает отбой, и дополнительный кластер становится основным после отсчета.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="b1c4a-124">Так как отбой занимает много времени, предложить выполнить его с параметром -Asjob и дождаться завершения задания.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="b1c4a-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1c4a-125">PARAMETERS</span></span>

### <span data-ttu-id="b1c4a-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1c4a-126">-AsJob</span></span>
<span data-ttu-id="b1c4a-127">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b1c4a-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1c4a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c4a-128">-DefaultProfile</span></span>
<span data-ttu-id="b1c4a-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c4a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="b1c4a-130">-Force</span></span>
<span data-ttu-id="b1c4a-131">Принудительное отсчет учетной записи</span><span class="sxs-lookup"><span data-stu-id="b1c4a-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="b1c4a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1c4a-132">-InputObject</span></span>
<span data-ttu-id="b1c4a-133">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b1c4a-133">Storage account object</span></span>

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

### <span data-ttu-id="b1c4a-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b1c4a-134">-Name</span></span>
<span data-ttu-id="b1c4a-135">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c4a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c4a-136">-ResourceGroupName</span></span>
<span data-ttu-id="b1c4a-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1c4a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1c4a-138">-Confirm</span></span>
<span data-ttu-id="b1c4a-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1c4a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c4a-140">-WhatIf</span></span>
<span data-ttu-id="b1c4a-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c4a-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1c4a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c4a-143">CommonParameters</span></span>
<span data-ttu-id="b1c4a-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c4a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c4a-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c4a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c4a-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1c4a-146">INPUTS</span></span>

### <span data-ttu-id="b1c4a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b1c4a-147">System.String</span></span>

## <span data-ttu-id="b1c4a-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1c4a-148">OUTPUTS</span></span>

### <span data-ttu-id="b1c4a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1c4a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b1c4a-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1c4a-150">NOTES</span></span>

## <span data-ttu-id="b1c4a-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1c4a-151">RELATED LINKS</span></span>
