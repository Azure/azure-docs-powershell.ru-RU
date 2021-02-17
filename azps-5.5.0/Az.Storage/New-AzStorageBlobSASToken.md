---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232537"
---
# <span data-ttu-id="6f73e-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6f73e-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="6f73e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f73e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f73e-103">Создает токен SAS для BLOB-контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6f73e-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="6f73e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f73e-104">SYNTAX</span></span>

### <span data-ttu-id="6f73e-105">BlobNameWithPermission (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f73e-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f73e-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="6f73e-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f73e-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="6f73e-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f73e-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="6f73e-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f73e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f73e-109">DESCRIPTION</span></span>
<span data-ttu-id="6f73e-110">Для BLOB-blob-хранилища Azure с его использованием создается маркер подписи SAS **(New-AzStorageBlobSASToken).**</span><span class="sxs-lookup"><span data-stu-id="6f73e-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="6f73e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f73e-111">EXAMPLES</span></span>

### <span data-ttu-id="6f73e-112">Пример 1. Создание маркера SAS для BLOB-приложений с полными разрешениями на доступ к BLOB-бизнесу</span><span class="sxs-lookup"><span data-stu-id="6f73e-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="6f73e-113">В этом примере создается токен SAS для BLOB-приложений с полными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="6f73e-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="6f73e-114">Пример 2. Создание маркера SAS для BLOB-приложений с жизненным временем</span><span class="sxs-lookup"><span data-stu-id="6f73e-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="6f73e-115">В этом примере создается токен SAS для BLOB-приложений со сроком жизни.</span><span class="sxs-lookup"><span data-stu-id="6f73e-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="6f73e-116">Пример 3. Создание маркера SAS удостоверения пользователя с контекстом хранилища на основе проверки подлинности OAuth</span><span class="sxs-lookup"><span data-stu-id="6f73e-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="6f73e-117">В этом примере создается маркер SAS BLOB-blob-blob пользователя с контекстом хранилища на основе проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="6f73e-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="6f73e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f73e-118">PARAMETERS</span></span>

### <span data-ttu-id="6f73e-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="6f73e-119">-Blob</span></span>
<span data-ttu-id="6f73e-120">Имя BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="6f73e-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="6f73e-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6f73e-121">-BlobBaseClient</span></span>
<span data-ttu-id="6f73e-122">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6f73e-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f73e-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6f73e-123">-CloudBlob</span></span>
<span data-ttu-id="6f73e-124">Указывает объект **CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="6f73e-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="6f73e-125">Чтобы получить объект **CloudBlob,** используйте [cmdlet Get-AzStorageBlob.](./Get-AzStorageBlob.md)</span><span class="sxs-lookup"><span data-stu-id="6f73e-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="6f73e-126">-Container</span><span class="sxs-lookup"><span data-stu-id="6f73e-126">-Container</span></span>
<span data-ttu-id="6f73e-127">Имя контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="6f73e-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="6f73e-128">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6f73e-128">-Context</span></span>
<span data-ttu-id="6f73e-129">Определяет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="6f73e-129">Specifies the storage context.</span></span>
<span data-ttu-id="6f73e-130">Если контекст хранилища основан на проверке подлинности OAuth, создается маркер SAS BLOB-blob-blob-идентификатора пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f73e-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="6f73e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f73e-131">-DefaultProfile</span></span>
<span data-ttu-id="6f73e-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f73e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f73e-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6f73e-133">-ExpiryTime</span></span>
<span data-ttu-id="6f73e-134">Указывает, когда истекает срок действия подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="6f73e-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="6f73e-135">Если контекст хранилища основан на проверке подлинности OAuth, срок действия истекает через 7 дней с текущего и не должен быть раньше текущего времени.</span><span class="sxs-lookup"><span data-stu-id="6f73e-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="6f73e-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="6f73e-136">-FullUri</span></span>
<span data-ttu-id="6f73e-137">Указывает на то, что этот cmdlet возвращает полный URI BLOB-приложений и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="6f73e-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="6f73e-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6f73e-138">-IPAddressOrRange</span></span>
<span data-ttu-id="6f73e-139">Указывает IP-адрес или диапазон IP-адресов, с которых нужно принимать запросы, например 168.1.5.65 или 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="6f73e-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="6f73e-140">Диапазон включительно.</span><span class="sxs-lookup"><span data-stu-id="6f73e-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="6f73e-141">-Permission</span><span class="sxs-lookup"><span data-stu-id="6f73e-141">-Permission</span></span>
<span data-ttu-id="6f73e-142">Определяет разрешения для BLOB-адреса хранилища.</span><span class="sxs-lookup"><span data-stu-id="6f73e-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="6f73e-143">Важно отметить, что это строка (для чтения, записи `rwd` и удаления).</span><span class="sxs-lookup"><span data-stu-id="6f73e-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="6f73e-144">-Политика</span><span class="sxs-lookup"><span data-stu-id="6f73e-144">-Policy</span></span>
<span data-ttu-id="6f73e-145">Определяет политику хранимого доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="6f73e-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="6f73e-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6f73e-146">-Protocol</span></span>
<span data-ttu-id="6f73e-147">Определяет протокол, допустимый для запроса.</span><span class="sxs-lookup"><span data-stu-id="6f73e-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="6f73e-148">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="6f73e-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="6f73e-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6f73e-149">HttpsOnly</span></span>
* <span data-ttu-id="6f73e-150">По умолчанию httpsOrHttp имеет значение httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="6f73e-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="6f73e-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6f73e-151">-StartTime</span></span>
<span data-ttu-id="6f73e-152">Время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="6f73e-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="6f73e-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f73e-153">-Confirm</span></span>
<span data-ttu-id="6f73e-154">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6f73e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f73e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f73e-155">-WhatIf</span></span>
<span data-ttu-id="6f73e-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f73e-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f73e-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f73e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f73e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f73e-158">CommonParameters</span></span>
<span data-ttu-id="6f73e-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f73e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f73e-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f73e-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f73e-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f73e-161">INPUTS</span></span>

### <span data-ttu-id="6f73e-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6f73e-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6f73e-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f73e-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6f73e-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f73e-164">OUTPUTS</span></span>

### <span data-ttu-id="6f73e-165">System.String</span><span class="sxs-lookup"><span data-stu-id="6f73e-165">System.String</span></span>

## <span data-ttu-id="6f73e-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f73e-166">NOTES</span></span>

## <span data-ttu-id="6f73e-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f73e-167">RELATED LINKS</span></span>

[<span data-ttu-id="6f73e-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6f73e-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6f73e-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6f73e-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
