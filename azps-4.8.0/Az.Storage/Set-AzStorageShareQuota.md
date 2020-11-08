---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: d029a00a2ddba5974fb473e58b933820e2e14757
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078581"
---
# <span data-ttu-id="2cfe2-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="2cfe2-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="2cfe2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cfe2-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfe2-103">Задает емкость хранилища для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="2cfe2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cfe2-104">SYNTAX</span></span>

### <span data-ttu-id="2cfe2-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cfe2-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2cfe2-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="2cfe2-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cfe2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cfe2-107">DESCRIPTION</span></span>
<span data-ttu-id="2cfe2-108">Командлет **Set-AzStorageShareQuota** Задает емкость хранилища для указанной общей записи.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="2cfe2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cfe2-109">EXAMPLES</span></span>

### <span data-ttu-id="2cfe2-110">Пример 1: Настройка емкости хранилища для общего доступа</span><span class="sxs-lookup"><span data-stu-id="2cfe2-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="2cfe2-111">Эта команда задает емкость хранилища для общего ресурса с именем ContosoShare01 на 1024 ГБ.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="2cfe2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cfe2-112">PARAMETERS</span></span>

### <span data-ttu-id="2cfe2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2cfe2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2cfe2-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2cfe2-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2cfe2-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfe2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2cfe2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2cfe2-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2cfe2-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2cfe2-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2cfe2-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2cfe2-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="2cfe2-123">-Context</span><span class="sxs-lookup"><span data-stu-id="2cfe2-123">-Context</span></span>
<span data-ttu-id="2cfe2-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2cfe2-125">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="2cfe2-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cfe2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfe2-126">-DefaultProfile</span></span>
<span data-ttu-id="2cfe2-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cfe2-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="2cfe2-128">-Quota</span></span>
<span data-ttu-id="2cfe2-129">Указывает значение квоты в гигабайтах (ГБ).</span><span class="sxs-lookup"><span data-stu-id="2cfe2-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="2cfe2-130">Ознакомьтесь с раздельными квотами https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="2cfe2-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: QuotaGiB

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfe2-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2cfe2-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2cfe2-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-132">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfe2-133">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="2cfe2-133">-Share</span></span>
<span data-ttu-id="2cfe2-134">Указывает объект **CloudFileShare** для представления общего доступа, для которого этот командлет устанавливает квоту.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="2cfe2-135">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cfe2-136">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="2cfe2-136">-ShareName</span></span>
<span data-ttu-id="2cfe2-137">Указывает имя общей файловой панели, для которой задается квота.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cfe2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfe2-138">CommonParameters</span></span>
<span data-ttu-id="2cfe2-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cfe2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfe2-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cfe2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfe2-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cfe2-141">INPUTS</span></span>

### <span data-ttu-id="2cfe2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfe2-142">System.String</span></span>

### <span data-ttu-id="2cfe2-143">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2cfe2-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="2cfe2-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2cfe2-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2cfe2-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cfe2-145">OUTPUTS</span></span>

### <span data-ttu-id="2cfe2-146">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="2cfe2-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="2cfe2-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cfe2-147">NOTES</span></span>

## <span data-ttu-id="2cfe2-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cfe2-148">RELATED LINKS</span></span>

[<span data-ttu-id="2cfe2-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2cfe2-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="2cfe2-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="2cfe2-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="2cfe2-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2cfe2-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)