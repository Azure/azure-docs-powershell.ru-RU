---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
ms.openlocfilehash: 3d2fd2ae65ff343bbe5faeece41194c768bec8c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915433"
---
# <span data-ttu-id="e54da-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e54da-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="e54da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e54da-102">SYNOPSIS</span></span>
<span data-ttu-id="e54da-103">Задает емкость хранилища для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e54da-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e54da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e54da-104">SYNTAX</span></span>

### <span data-ttu-id="e54da-105">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="e54da-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e54da-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="e54da-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e54da-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e54da-107">DESCRIPTION</span></span>
<span data-ttu-id="e54da-108">Командлет **Set-AzureStorageShareQuota** Задает емкость хранилища для указанной общей записи.</span><span class="sxs-lookup"><span data-stu-id="e54da-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="e54da-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e54da-109">EXAMPLES</span></span>

### <span data-ttu-id="e54da-110">Пример 1: Настройка емкости хранилища для общего доступа</span><span class="sxs-lookup"><span data-stu-id="e54da-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="e54da-111">Эта команда задает емкость хранилища для общего ресурса с именем ContosoShare01 на 1024 ГБ.</span><span class="sxs-lookup"><span data-stu-id="e54da-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="e54da-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e54da-112">PARAMETERS</span></span>

### <span data-ttu-id="e54da-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e54da-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e54da-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e54da-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e54da-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="e54da-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e54da-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e54da-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e54da-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e54da-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e54da-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="e54da-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e54da-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="e54da-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e54da-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="e54da-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e54da-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="e54da-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e54da-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="e54da-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e54da-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e54da-123">-Context</span></span>
<span data-ttu-id="e54da-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e54da-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e54da-125">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e54da-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e54da-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54da-126">-DefaultProfile</span></span>
<span data-ttu-id="e54da-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e54da-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54da-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="e54da-128">-Quota</span></span>
<span data-ttu-id="e54da-129">Указывает значение квоты в гигабайтах (ГБ).</span><span class="sxs-lookup"><span data-stu-id="e54da-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="e54da-130">Ознакомьтесь с раздельными квотами https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="e54da-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54da-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e54da-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e54da-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="e54da-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e54da-133">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="e54da-133">-Share</span></span>
<span data-ttu-id="e54da-134">Указывает объект **CloudFileShare** для представления общего доступа, для которого этот командлет устанавливает квоту.</span><span class="sxs-lookup"><span data-stu-id="e54da-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="e54da-135">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="e54da-135">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e54da-136">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="e54da-136">-ShareName</span></span>
<span data-ttu-id="e54da-137">Указывает имя общей файловой панели, для которой задается квота.</span><span class="sxs-lookup"><span data-stu-id="e54da-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="e54da-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54da-138">CommonParameters</span></span>
<span data-ttu-id="e54da-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e54da-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54da-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e54da-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54da-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e54da-141">INPUTS</span></span>

### <span data-ttu-id="e54da-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e54da-142">System.String</span></span>

### <span data-ttu-id="e54da-143">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e54da-143">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="e54da-144">Параметры: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e54da-144">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="e54da-145">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e54da-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e54da-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e54da-146">OUTPUTS</span></span>

### <span data-ttu-id="e54da-147">Microsoft. WindowsAzure. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="e54da-147">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="e54da-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="e54da-148">NOTES</span></span>

## <span data-ttu-id="e54da-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e54da-149">RELATED LINKS</span></span>

[<span data-ttu-id="e54da-150">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e54da-150">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="e54da-151">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e54da-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="e54da-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e54da-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
