---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: 60c93d851e173dd8ee8a5f33ff96bb4e2e12299b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566024"
---
# <span data-ttu-id="8f853-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8f853-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="8f853-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f853-102">SYNOPSIS</span></span>
<span data-ttu-id="8f853-103">Создание маркера SAS для блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8f853-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f853-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f853-104">SYNTAX</span></span>

### <span data-ttu-id="8f853-105">BlobNameWithPermission (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f853-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f853-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="8f853-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f853-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="8f853-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f853-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="8f853-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f853-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f853-109">DESCRIPTION</span></span>
<span data-ttu-id="8f853-110">Командлет **New-AzureStorageBlobSASToken** создает маркер подписи общего доступа (SAS) для блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8f853-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="8f853-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f853-111">EXAMPLES</span></span>

### <span data-ttu-id="8f853-112">Пример 1: создание маркера SAS BLOB с полным разрешением BLOB</span><span class="sxs-lookup"><span data-stu-id="8f853-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="8f853-113">В этом примере создается маркер SAS BLOB с полным разрешением BLOB.</span><span class="sxs-lookup"><span data-stu-id="8f853-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="8f853-114">Пример 2: создание маркера SAS BLOB со сроком жизни</span><span class="sxs-lookup"><span data-stu-id="8f853-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="8f853-115">В этом примере создается маркер SAS BLOB со сроком жизни.</span><span class="sxs-lookup"><span data-stu-id="8f853-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="8f853-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f853-116">PARAMETERS</span></span>

### <span data-ttu-id="8f853-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="8f853-117">-Blob</span></span>
<span data-ttu-id="8f853-118">Указывает имя BLOB-объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f853-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f853-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8f853-119">-CloudBlob</span></span>
<span data-ttu-id="8f853-120">Указывает объект **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="8f853-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="8f853-121">Чтобы получить объект **CloudBlob** , используйте командлет [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="8f853-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f853-122">-Container</span><span class="sxs-lookup"><span data-stu-id="8f853-122">-Container</span></span>
<span data-ttu-id="8f853-123">Указывает имя контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f853-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f853-124">-Context</span><span class="sxs-lookup"><span data-stu-id="8f853-124">-Context</span></span>
<span data-ttu-id="8f853-125">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f853-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="8f853-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f853-126">-DefaultProfile</span></span>
<span data-ttu-id="8f853-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f853-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f853-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8f853-128">-ExpiryTime</span></span>
<span data-ttu-id="8f853-129">Указывает, когда истекает срок действия подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8f853-129">Specifies when the shared access signature expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f853-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8f853-130">-FullUri</span></span>
<span data-ttu-id="8f853-131">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8f853-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="8f853-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8f853-132">-IPAddressOrRange</span></span>
<span data-ttu-id="8f853-133">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="8f853-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8f853-134">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="8f853-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="8f853-135">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="8f853-135">-Permission</span></span>
<span data-ttu-id="8f853-136">Задает разрешения для BLOB-объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f853-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="8f853-137">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="8f853-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f853-138">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="8f853-138">-Policy</span></span>
<span data-ttu-id="8f853-139">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="8f853-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f853-140">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="8f853-140">-Protocol</span></span>
<span data-ttu-id="8f853-141">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="8f853-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8f853-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8f853-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8f853-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8f853-143">HttpsOnly</span></span>
* <span data-ttu-id="8f853-144">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8f853-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f853-145">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8f853-145">-StartTime</span></span>
<span data-ttu-id="8f853-146">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="8f853-146">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f853-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f853-147">CommonParameters</span></span>
<span data-ttu-id="8f853-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f853-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f853-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f853-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f853-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f853-150">INPUTS</span></span>

### <span data-ttu-id="8f853-151">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8f853-151">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="8f853-152">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8f853-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8f853-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f853-153">OUTPUTS</span></span>

### <span data-ttu-id="8f853-154">System. String</span><span class="sxs-lookup"><span data-stu-id="8f853-154">System.String</span></span>

## <span data-ttu-id="8f853-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f853-155">NOTES</span></span>

## <span data-ttu-id="8f853-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f853-156">RELATED LINKS</span></span>

[<span data-ttu-id="8f853-157">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8f853-157">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="8f853-158">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8f853-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
