---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248464"
---
# <span data-ttu-id="70f44-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="70f44-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="70f44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70f44-102">SYNOPSIS</span></span>
<span data-ttu-id="70f44-103">Вызывает отработку отказа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="70f44-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="70f44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70f44-104">SYNTAX</span></span>

### <span data-ttu-id="70f44-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70f44-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f44-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="70f44-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70f44-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70f44-107">DESCRIPTION</span></span>
<span data-ttu-id="70f44-108">Вызывает отработку отказа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="70f44-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="70f44-109">Для учетной записи хранения в случае проблем с доступностью может быть активирован запрос на отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="70f44-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="70f44-110">Отработка отказа выполняется из основного кластера учетной записи хранения в дополнительный кластер для учетных записей RA-GRS.</span><span class="sxs-lookup"><span data-stu-id="70f44-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="70f44-111">Дополнительный кластер станет основным после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="70f44-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="70f44-112">Прежде чем приступить к переходу на другой ресурс, ознакомьтесь со следующими последствиями для вашей учетной записи хранения: 1,1.</span><span class="sxs-lookup"><span data-stu-id="70f44-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="70f44-113">Проверьте время последней синхронизации с помощью функции получения статистики службы BLOB-объектов (Выбери статистику службы https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) таблиц ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) и получить статистику службы очереди ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) для вашей учетной записи).</span><span class="sxs-lookup"><span data-stu-id="70f44-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="70f44-114">Это может привести к потере данных, если инициируется переход на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="70f44-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="70f44-115">2. После отработки отказа тип учетной записи хранения будет преобразован в локально избыточное хранилище (LRS).</span><span class="sxs-lookup"><span data-stu-id="70f44-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="70f44-116">Вы можете преобразовать учетную запись, чтобы использовать геоизбыточное хранилище (GRS).</span><span class="sxs-lookup"><span data-stu-id="70f44-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="70f44-117">3. После повторного включения GRS для вашей учетной записи хранения Корпорация Майкрософт будет реплицировать данные в новый дополнительный регион.</span><span class="sxs-lookup"><span data-stu-id="70f44-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="70f44-118">Время репликации зависит от объема реплицируемых данных.</span><span class="sxs-lookup"><span data-stu-id="70f44-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="70f44-119">Обратите внимание на то, что для начальной загрузки есть плата за пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="70f44-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="70f44-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="70f44-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="70f44-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70f44-121">EXAMPLES</span></span>

### <span data-ttu-id="70f44-122">Пример 1: вызов отработки отказа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="70f44-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="70f44-123">Эта команда проверяет время последней синхронизации учетной записи хранения, а затем вызывает отработку отказа для него, дополнительный кластер становится основным после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="70f44-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="70f44-124">Так как отработка отказа занимает много времени, предложите выполнить ее в серверной части с параметром-AsJob и дождаться завершения задания.</span><span class="sxs-lookup"><span data-stu-id="70f44-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="70f44-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70f44-125">PARAMETERS</span></span>

### <span data-ttu-id="70f44-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70f44-126">-AsJob</span></span>
<span data-ttu-id="70f44-127">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="70f44-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70f44-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f44-128">-DefaultProfile</span></span>
<span data-ttu-id="70f44-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70f44-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70f44-130">-Force</span><span class="sxs-lookup"><span data-stu-id="70f44-130">-Force</span></span>
<span data-ttu-id="70f44-131">Принудительная отработка отказа учетной записи</span><span class="sxs-lookup"><span data-stu-id="70f44-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="70f44-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70f44-132">-InputObject</span></span>
<span data-ttu-id="70f44-133">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="70f44-133">Storage account object</span></span>

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

### <span data-ttu-id="70f44-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70f44-134">-Name</span></span>
<span data-ttu-id="70f44-135">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="70f44-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="70f44-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f44-136">-ResourceGroupName</span></span>
<span data-ttu-id="70f44-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70f44-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="70f44-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70f44-138">-Confirm</span></span>
<span data-ttu-id="70f44-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70f44-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f44-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f44-140">-WhatIf</span></span>
<span data-ttu-id="70f44-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70f44-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70f44-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70f44-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f44-143">CommonParameters</span></span>
<span data-ttu-id="70f44-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70f44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f44-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f44-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f44-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70f44-146">INPUTS</span></span>

### <span data-ttu-id="70f44-147">System. String</span><span class="sxs-lookup"><span data-stu-id="70f44-147">System.String</span></span>

## <span data-ttu-id="70f44-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70f44-148">OUTPUTS</span></span>

### <span data-ttu-id="70f44-149">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70f44-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="70f44-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="70f44-150">NOTES</span></span>

## <span data-ttu-id="70f44-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70f44-151">RELATED LINKS</span></span>