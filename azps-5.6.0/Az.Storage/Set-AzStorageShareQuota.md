---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: 132ad47cd52f258b78ac944342d86979a69abbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007544"
---
# <span data-ttu-id="4a9b7-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4a9b7-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="4a9b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4a9b7-103">Задает объем хранилища для поделиться.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="4a9b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a9b7-104">SYNTAX</span></span>

### <span data-ttu-id="4a9b7-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a9b7-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4a9b7-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="4a9b7-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a9b7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a9b7-107">DESCRIPTION</span></span>
<span data-ttu-id="4a9b7-108">**Cmdlet Set-AzStorageShareQuota** задает объем хранилища для указанной доли.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="4a9b7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a9b7-109">EXAMPLES</span></span>

### <span data-ttu-id="4a9b7-110">Пример 1. Настройка емкости хранилища для одной акции</span><span class="sxs-lookup"><span data-stu-id="4a9b7-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="4a9b7-111">Эта команда задает для хранилища ContosoShare01 объем 1024 ГБ.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="4a9b7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a9b7-112">PARAMETERS</span></span>

### <span data-ttu-id="4a9b7-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4a9b7-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4a9b7-114">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4a9b7-115">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4a9b7-116">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4a9b7-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4a9b7-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4a9b7-118">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4a9b7-119">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4a9b7-120">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4a9b7-121">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4a9b7-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-122">The default value is 10.</span></span>

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

### <span data-ttu-id="4a9b7-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4a9b7-123">-Context</span></span>
<span data-ttu-id="4a9b7-124">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4a9b7-125">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="4a9b7-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4a9b7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a9b7-126">-DefaultProfile</span></span>
<span data-ttu-id="4a9b7-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a9b7-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="4a9b7-128">-Quota</span></span>
<span data-ttu-id="4a9b7-129">Квота в гигабайтах (ГБ).</span><span class="sxs-lookup"><span data-stu-id="4a9b7-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="4a9b7-130">См. ограничение квоты в https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="4a9b7-130">See the quota limitation in https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

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

### <span data-ttu-id="4a9b7-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4a9b7-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4a9b7-132">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4a9b7-133">-Share</span><span class="sxs-lookup"><span data-stu-id="4a9b7-133">-Share</span></span>
<span data-ttu-id="4a9b7-134">Задает объект **CloudFileShare,** представляюща долю, для которой этот cmdlets задает квоту.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="4a9b7-135">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="4a9b7-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4a9b7-136">-ShareName</span></span>
<span data-ttu-id="4a9b7-137">Имя папки, для которой нужно установить квоту.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="4a9b7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a9b7-138">CommonParameters</span></span>
<span data-ttu-id="4a9b7-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a9b7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a9b7-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a9b7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a9b7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a9b7-141">INPUTS</span></span>

### <span data-ttu-id="4a9b7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4a9b7-142">System.String</span></span>

### <span data-ttu-id="4a9b7-143">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4a9b7-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="4a9b7-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4a9b7-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4a9b7-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a9b7-145">OUTPUTS</span></span>

### <span data-ttu-id="4a9b7-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="4a9b7-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="4a9b7-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a9b7-147">NOTES</span></span>

## <span data-ttu-id="4a9b7-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a9b7-148">RELATED LINKS</span></span>

[<span data-ttu-id="4a9b7-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4a9b7-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="4a9b7-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4a9b7-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4a9b7-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4a9b7-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
