---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8d84b310a16a73456bcd519332fa76ad1a6566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556220"
---
# <span data-ttu-id="7fc7f-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7fc7f-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="7fc7f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fc7f-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc7f-103">Создает маркер SAS для блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-103">Generates an SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="7fc7f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fc7f-104">SYNTAX</span></span>

### <span data-ttu-id="7fc7f-105">BlobNameWithPermission (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fc7f-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="7fc7f-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="7fc7f-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="7fc7f-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="7fc7f-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="7fc7f-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="7fc7f-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="7fc7f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fc7f-109">DESCRIPTION</span></span>
<span data-ttu-id="7fc7f-110">Командлет **New-AzureStorageBlobSASToken** создает маркер подписи общего доступа (SAS) для блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="7fc7f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fc7f-111">EXAMPLES</span></span>

### <span data-ttu-id="7fc7f-112">Пример 1: создание маркера SAS BLOB с полным разрешением BLOB</span><span class="sxs-lookup"><span data-stu-id="7fc7f-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="7fc7f-113">В этом примере создается маркер SAS BLOB с полным разрешением BLOB.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="7fc7f-114">Пример 2: создание маркера SAS BLOB со сроком жизни</span><span class="sxs-lookup"><span data-stu-id="7fc7f-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="7fc7f-115">В этом примере создается маркер SAS BLOB со сроком жизни.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="7fc7f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fc7f-116">PARAMETERS</span></span>

### <span data-ttu-id="7fc7f-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="7fc7f-117">-Blob</span></span>
<span data-ttu-id="7fc7f-118">Указывает имя BLOB-объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-118">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="7fc7f-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7fc7f-119">-CloudBlob</span></span>
<span data-ttu-id="7fc7f-120">Указывает объект **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="7fc7f-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="7fc7f-121">Чтобы получить объект **CloudBlob** , используйте командлет [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc7f-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="7fc7f-122">-Container</span><span class="sxs-lookup"><span data-stu-id="7fc7f-122">-Container</span></span>
<span data-ttu-id="7fc7f-123">Указывает имя контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-123">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="7fc7f-124">-Context</span><span class="sxs-lookup"><span data-stu-id="7fc7f-124">-Context</span></span>
<span data-ttu-id="7fc7f-125">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="7fc7f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7fc7f-126">-ExpiryTime</span></span>
<span data-ttu-id="7fc7f-127">Указывает, когда истекает срок действия подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="7fc7f-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="7fc7f-128">-FullUri</span></span>
<span data-ttu-id="7fc7f-129">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="7fc7f-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7fc7f-130">-IPAddressOrRange</span></span>
<span data-ttu-id="7fc7f-131">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="7fc7f-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="7fc7f-132">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="7fc7f-133">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="7fc7f-133">-Permission</span></span>
<span data-ttu-id="7fc7f-134">Задает разрешения для BLOB-объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-134">Specifies the permissions for a storage blob.</span></span>

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

### <span data-ttu-id="7fc7f-135">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="7fc7f-135">-Policy</span></span>
<span data-ttu-id="7fc7f-136">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-136">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="7fc7f-137">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="7fc7f-137">-Protocol</span></span>
<span data-ttu-id="7fc7f-138">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="7fc7f-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7fc7f-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="7fc7f-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7fc7f-140">HttpsOnly</span></span>
* <span data-ttu-id="7fc7f-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="7fc7f-141">HttpsOrHttp</span></span>

<span data-ttu-id="7fc7f-142">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-142">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="7fc7f-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7fc7f-143">-StartTime</span></span>
<span data-ttu-id="7fc7f-144">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="7fc7f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc7f-145">CommonParameters</span></span>
<span data-ttu-id="7fc7f-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fc7f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc7f-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fc7f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc7f-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fc7f-148">INPUTS</span></span>

## <span data-ttu-id="7fc7f-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fc7f-149">OUTPUTS</span></span>

## <span data-ttu-id="7fc7f-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fc7f-150">NOTES</span></span>

## <span data-ttu-id="7fc7f-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fc7f-151">RELATED LINKS</span></span>

[<span data-ttu-id="7fc7f-152">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7fc7f-152">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="7fc7f-153">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7fc7f-153">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
