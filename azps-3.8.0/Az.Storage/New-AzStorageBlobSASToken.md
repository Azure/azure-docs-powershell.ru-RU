---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 6bcb5163e31f2acbdd3e180cf76aef8fcfb33571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073137"
---
# <span data-ttu-id="e555b-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e555b-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="e555b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e555b-102">SYNOPSIS</span></span>
<span data-ttu-id="e555b-103">Создание маркера SAS для блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e555b-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="e555b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e555b-104">SYNTAX</span></span>

### <span data-ttu-id="e555b-105">BlobNameWithPermission (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e555b-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e555b-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e555b-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e555b-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="e555b-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e555b-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e555b-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e555b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e555b-109">DESCRIPTION</span></span>
<span data-ttu-id="e555b-110">Командлет **New-AzStorageBlobSASToken** создает маркер подписи общего доступа (SAS) для блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e555b-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="e555b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e555b-111">EXAMPLES</span></span>

### <span data-ttu-id="e555b-112">Пример 1: создание маркера SAS BLOB с полным разрешением BLOB</span><span class="sxs-lookup"><span data-stu-id="e555b-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="e555b-113">В этом примере создается маркер SAS BLOB с полным разрешением BLOB.</span><span class="sxs-lookup"><span data-stu-id="e555b-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="e555b-114">Пример 2: создание маркера SAS BLOB со сроком жизни</span><span class="sxs-lookup"><span data-stu-id="e555b-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="e555b-115">В этом примере создается маркер SAS BLOB со сроком жизни.</span><span class="sxs-lookup"><span data-stu-id="e555b-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="e555b-116">Пример 3: создание маркера SAS для удостоверения пользователя с контекстом хранилища на основе проверки подлинности OAuth</span><span class="sxs-lookup"><span data-stu-id="e555b-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="e555b-117">В этом примере создается маркер SAS удостоверения пользователя BLOB-объектов с контекстом хранилища на основе проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="e555b-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="e555b-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e555b-118">PARAMETERS</span></span>

### <span data-ttu-id="e555b-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="e555b-119">-Blob</span></span>
<span data-ttu-id="e555b-120">Указывает имя BLOB-объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="e555b-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="e555b-121">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e555b-121">-CloudBlob</span></span>
<span data-ttu-id="e555b-122">Указывает объект **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="e555b-122">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="e555b-123">Чтобы получить объект **CloudBlob** , используйте командлет [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="e555b-123">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e555b-124">-Container</span><span class="sxs-lookup"><span data-stu-id="e555b-124">-Container</span></span>
<span data-ttu-id="e555b-125">Указывает имя контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="e555b-125">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="e555b-126">-Context</span><span class="sxs-lookup"><span data-stu-id="e555b-126">-Context</span></span>
<span data-ttu-id="e555b-127">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="e555b-127">Specifies the storage context.</span></span>
<span data-ttu-id="e555b-128">Если контекст хранилища основан на проверке подлинности OAuth, он создаст маркер SAS удостоверения пользователя для блоба.</span><span class="sxs-lookup"><span data-stu-id="e555b-128">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="e555b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e555b-129">-DefaultProfile</span></span>
<span data-ttu-id="e555b-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e555b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e555b-131">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e555b-131">-ExpiryTime</span></span>
<span data-ttu-id="e555b-132">Указывает, когда истекает срок действия подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e555b-132">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="e555b-133">Если контекст хранилища основан на проверке подлинности OAuth, срок действия истекает через 7 дней с текущего времени и не должен предшествовать текущему времени.</span><span class="sxs-lookup"><span data-stu-id="e555b-133">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="e555b-134">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e555b-134">-FullUri</span></span>
<span data-ttu-id="e555b-135">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e555b-135">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e555b-136">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e555b-136">-IPAddressOrRange</span></span>
<span data-ttu-id="e555b-137">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="e555b-137">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e555b-138">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="e555b-138">The range is inclusive.</span></span>

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

### <span data-ttu-id="e555b-139">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="e555b-139">-Permission</span></span>
<span data-ttu-id="e555b-140">Задает разрешения для BLOB-объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="e555b-140">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="e555b-141">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="e555b-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="e555b-142">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e555b-142">-Policy</span></span>
<span data-ttu-id="e555b-143">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="e555b-143">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="e555b-144">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e555b-144">-Protocol</span></span>
<span data-ttu-id="e555b-145">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="e555b-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e555b-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e555b-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e555b-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e555b-147">HttpsOnly</span></span>
* <span data-ttu-id="e555b-148">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="e555b-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e555b-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e555b-149">-StartTime</span></span>
<span data-ttu-id="e555b-150">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="e555b-150">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="e555b-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e555b-151">-Confirm</span></span>
<span data-ttu-id="e555b-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e555b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e555b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e555b-153">-WhatIf</span></span>
<span data-ttu-id="e555b-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e555b-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e555b-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e555b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e555b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e555b-156">CommonParameters</span></span>
<span data-ttu-id="e555b-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e555b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e555b-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e555b-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e555b-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e555b-159">INPUTS</span></span>

### <span data-ttu-id="e555b-160">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e555b-160">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="e555b-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e555b-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e555b-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e555b-162">OUTPUTS</span></span>

### <span data-ttu-id="e555b-163">System. String</span><span class="sxs-lookup"><span data-stu-id="e555b-163">System.String</span></span>

## <span data-ttu-id="e555b-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="e555b-164">NOTES</span></span>

## <span data-ttu-id="e555b-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e555b-165">RELATED LINKS</span></span>

[<span data-ttu-id="e555b-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e555b-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="e555b-167">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e555b-167">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
