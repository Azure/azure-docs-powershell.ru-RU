---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418796"
---
# <span data-ttu-id="4ac47-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4ac47-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="4ac47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac47-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac47-103">Создает токен SAS для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac47-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="4ac47-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ac47-104">SYNTAX</span></span>

### <span data-ttu-id="4ac47-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="4ac47-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ac47-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="4ac47-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ac47-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ac47-107">DESCRIPTION</span></span>
<span data-ttu-id="4ac47-108">Для контейнера хранилища Azure с его использованием создается маркер подписи SAS **(New-AzStorageContainerSASToken).**</span><span class="sxs-lookup"><span data-stu-id="4ac47-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="4ac47-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ac47-109">EXAMPLES</span></span>

### <span data-ttu-id="4ac47-110">Пример 1. Создание маркера SAS контейнера с полным разрешением контейнера</span><span class="sxs-lookup"><span data-stu-id="4ac47-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="4ac47-111">В этом примере создается токен SAS контейнера с полным разрешением контейнера.</span><span class="sxs-lookup"><span data-stu-id="4ac47-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="4ac47-112">Пример 2. Создание нескольких маркеров SAS контейнера в конвейере</span><span class="sxs-lookup"><span data-stu-id="4ac47-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="4ac47-113">В этом примере с помощью конвейера создается несколько токенов SAS контейнера.</span><span class="sxs-lookup"><span data-stu-id="4ac47-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="4ac47-114">Пример 3. Создание маркера SAS контейнера с помощью политики общего доступа</span><span class="sxs-lookup"><span data-stu-id="4ac47-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="4ac47-115">В этом примере создается маркер SAS контейнера с политикой общего доступа.</span><span class="sxs-lookup"><span data-stu-id="4ac47-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="4ac47-116">Пример 3. Создание маркера SAS контейнера удостоверения пользователя с контекстом хранилища на основе проверки подлинности OAuth</span><span class="sxs-lookup"><span data-stu-id="4ac47-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="4ac47-117">В этом примере создается маркер SAS контейнера удостоверений пользователя с контекстом хранилища на основе проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="4ac47-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="4ac47-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ac47-118">PARAMETERS</span></span>

### <span data-ttu-id="4ac47-119">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4ac47-119">-Context</span></span>
<span data-ttu-id="4ac47-120">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac47-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4ac47-121">Его можно создать с помощью New-AzStorageContext-управления.</span><span class="sxs-lookup"><span data-stu-id="4ac47-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="4ac47-122">Если контекст хранилища основан на проверке подлинности OAuth, создается маркер SAS контейнера удостоверений пользователя.</span><span class="sxs-lookup"><span data-stu-id="4ac47-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="4ac47-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac47-123">-DefaultProfile</span></span>
<span data-ttu-id="4ac47-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac47-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac47-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4ac47-125">-ExpiryTime</span></span>
<span data-ttu-id="4ac47-126">Время, в течение которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="4ac47-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="4ac47-127">Если пользователь устанавливает время начала, но не истекает, то время окончания устанавливается на плюс один час.</span><span class="sxs-lookup"><span data-stu-id="4ac47-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="4ac47-128">Если не указаны ни время начала, ни срок действия, то для истечения установлено текущее время, равное одному часу.</span><span class="sxs-lookup"><span data-stu-id="4ac47-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="4ac47-129">Если контекст хранилища основан на проверке подлинности OAuth, срок действия истекает через 7 дней с текущего и не должен быть раньше текущего времени.</span><span class="sxs-lookup"><span data-stu-id="4ac47-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="4ac47-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="4ac47-130">-FullUri</span></span>
<span data-ttu-id="4ac47-131">Указывает на то, что этот cmdlet возвращает полный URI BLOB-приложений и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="4ac47-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="4ac47-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4ac47-132">-IPAddressOrRange</span></span>
<span data-ttu-id="4ac47-133">Указывает IP-адрес или диапазон IP-адресов, с которых нужно принимать запросы, например 168.1.5.65 или 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="4ac47-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4ac47-134">Диапазон включительно.</span><span class="sxs-lookup"><span data-stu-id="4ac47-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="4ac47-135">-Name</span><span class="sxs-lookup"><span data-stu-id="4ac47-135">-Name</span></span>
<span data-ttu-id="4ac47-136">Имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac47-136">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac47-137">-Permission</span><span class="sxs-lookup"><span data-stu-id="4ac47-137">-Permission</span></span>
<span data-ttu-id="4ac47-138">Определяет разрешения для контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="4ac47-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="4ac47-139">Важно отметить, что это строка (для чтения, записи `rwd` и удаления).</span><span class="sxs-lookup"><span data-stu-id="4ac47-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac47-140">-Политика</span><span class="sxs-lookup"><span data-stu-id="4ac47-140">-Policy</span></span>
<span data-ttu-id="4ac47-141">Определяет политику хранимого доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac47-141">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac47-142">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4ac47-142">-Protocol</span></span>
<span data-ttu-id="4ac47-143">Определяет протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="4ac47-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="4ac47-144">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="4ac47-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="4ac47-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4ac47-145">HttpsOnly</span></span>
* <span data-ttu-id="4ac47-146">По умолчанию httpsOrHttp имеет значение httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="4ac47-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="4ac47-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4ac47-147">-StartTime</span></span>
<span data-ttu-id="4ac47-148">Время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="4ac47-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="4ac47-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ac47-149">-Confirm</span></span>
<span data-ttu-id="4ac47-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ac47-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac47-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac47-151">-WhatIf</span></span>
<span data-ttu-id="4ac47-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ac47-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ac47-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ac47-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac47-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac47-154">CommonParameters</span></span>
<span data-ttu-id="4ac47-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac47-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac47-156">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac47-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac47-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ac47-157">INPUTS</span></span>

### <span data-ttu-id="4ac47-158">System.String</span><span class="sxs-lookup"><span data-stu-id="4ac47-158">System.String</span></span>

### <span data-ttu-id="4ac47-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ac47-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ac47-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ac47-160">OUTPUTS</span></span>

### <span data-ttu-id="4ac47-161">System.String</span><span class="sxs-lookup"><span data-stu-id="4ac47-161">System.String</span></span>

## <span data-ttu-id="4ac47-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ac47-162">NOTES</span></span>

## <span data-ttu-id="4ac47-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ac47-163">RELATED LINKS</span></span>

[<span data-ttu-id="4ac47-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4ac47-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
