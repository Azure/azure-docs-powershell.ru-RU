---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: d75111b27b03317f757cbf0def4d9d66c43427c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733305"
---
# <span data-ttu-id="8d1d6-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8d1d6-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="8d1d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1d6-103">Создание маркера SAS для блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d1d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d1d6-104">SYNTAX</span></span>

### <span data-ttu-id="8d1d6-105">BlobNameWithPermission (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d1d6-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="8d1d6-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="8d1d6-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="8d1d6-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="8d1d6-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="8d1d6-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="8d1d6-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="8d1d6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d1d6-109">DESCRIPTION</span></span>
<span data-ttu-id="8d1d6-110">Командлет **New-AzureStorageBlobSASToken** создает маркер подписи общего доступа (SAS) для блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="8d1d6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d1d6-111">EXAMPLES</span></span>

### <span data-ttu-id="8d1d6-112">Пример 1: создание маркера SAS BLOB с полным разрешением BLOB</span><span class="sxs-lookup"><span data-stu-id="8d1d6-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="8d1d6-113">В этом примере создается маркер SAS BLOB с полным разрешением BLOB.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="8d1d6-114">Пример 2: создание маркера SAS BLOB со сроком жизни</span><span class="sxs-lookup"><span data-stu-id="8d1d6-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="8d1d6-115">В этом примере создается маркер SAS BLOB со сроком жизни.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="8d1d6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d1d6-116">PARAMETERS</span></span>

### <span data-ttu-id="8d1d6-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="8d1d6-117">-Blob</span></span>
<span data-ttu-id="8d1d6-118">Указывает имя BLOB-объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8d1d6-119">-CloudBlob</span></span>
<span data-ttu-id="8d1d6-120">Указывает объект **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="8d1d6-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="8d1d6-121">Чтобы получить объект **CloudBlob** , используйте командлет [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1d6-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-122">-Container</span><span class="sxs-lookup"><span data-stu-id="8d1d6-122">-Container</span></span>
<span data-ttu-id="8d1d6-123">Указывает имя контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-124">-Context</span><span class="sxs-lookup"><span data-stu-id="8d1d6-124">-Context</span></span>
<span data-ttu-id="8d1d6-125">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-125">Specifies the storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8d1d6-126">-ExpiryTime</span></span>
<span data-ttu-id="8d1d6-127">Указывает, когда истекает срок действия подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-127">Specifies when the shared access signature expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8d1d6-128">-FullUri</span></span>
<span data-ttu-id="8d1d6-129">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8d1d6-130">-IPAddressOrRange</span></span>
<span data-ttu-id="8d1d6-131">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="8d1d6-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8d1d6-132">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-132">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-133">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="8d1d6-133">-Permission</span></span>
<span data-ttu-id="8d1d6-134">Задает разрешения для BLOB-объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-135">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="8d1d6-135">-Policy</span></span>
<span data-ttu-id="8d1d6-136">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-137">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="8d1d6-137">-Protocol</span></span>
<span data-ttu-id="8d1d6-138">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8d1d6-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8d1d6-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8d1d6-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8d1d6-140">HttpsOnly</span></span>
* <span data-ttu-id="8d1d6-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="8d1d6-141">HttpsOrHttp</span></span>

<span data-ttu-id="8d1d6-142">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-142">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8d1d6-143">-StartTime</span></span>
<span data-ttu-id="8d1d6-144">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-144">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1d6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1d6-145">CommonParameters</span></span>
<span data-ttu-id="8d1d6-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1d6-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d1d6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1d6-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d1d6-148">INPUTS</span></span>

### <span data-ttu-id="8d1d6-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d1d6-149">IStorageContext</span></span>

<span data-ttu-id="8d1d6-150">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8d1d6-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="8d1d6-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d1d6-151">OUTPUTS</span></span>

### <span data-ttu-id="8d1d6-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8d1d6-152">System.String</span></span>

## <span data-ttu-id="8d1d6-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d1d6-153">NOTES</span></span>

## <span data-ttu-id="8d1d6-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d1d6-154">RELATED LINKS</span></span>

[<span data-ttu-id="8d1d6-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8d1d6-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="8d1d6-156">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8d1d6-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
