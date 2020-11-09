---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243786"
---
# <span data-ttu-id="40878-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="40878-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="40878-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40878-102">SYNOPSIS</span></span>
<span data-ttu-id="40878-103">Создание маркера SAS для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="40878-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="40878-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40878-104">SYNTAX</span></span>

### <span data-ttu-id="40878-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="40878-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40878-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="40878-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40878-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40878-107">DESCRIPTION</span></span>
<span data-ttu-id="40878-108">Командлет **New-AzStorageContainerSASToken** создает маркер подписи общего доступа (SAS) для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="40878-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="40878-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40878-109">EXAMPLES</span></span>

### <span data-ttu-id="40878-110">Пример 1: создание маркера безопасности контейнера с разрешениями полного контейнера</span><span class="sxs-lookup"><span data-stu-id="40878-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="40878-111">В этом примере создается маркер безопасности контейнера с разрешениями полного контейнера.</span><span class="sxs-lookup"><span data-stu-id="40878-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="40878-112">Пример 2: создание маркера SAS с несколькими контейнерами с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="40878-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="40878-113">В этом примере создается несколько маркеров сопоставления безопасности контейнера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="40878-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="40878-114">Пример 3: создание маркера SAS контейнера с политикой общего доступа</span><span class="sxs-lookup"><span data-stu-id="40878-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="40878-115">В этом примере создается маркер SAS контейнера с политикой общего доступа.</span><span class="sxs-lookup"><span data-stu-id="40878-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="40878-116">Пример 3: создание маркера SAS контейнера удостоверений пользователя с контекстом хранилища на основе проверки подлинности OAuth</span><span class="sxs-lookup"><span data-stu-id="40878-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="40878-117">В этом примере создается маркер SAS контейнера удостоверения пользователя с контекстом хранилища на основе проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="40878-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="40878-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40878-118">PARAMETERS</span></span>

### <span data-ttu-id="40878-119">-Context</span><span class="sxs-lookup"><span data-stu-id="40878-119">-Context</span></span>
<span data-ttu-id="40878-120">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="40878-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="40878-121">Вы можете создать его с помощью командлета New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="40878-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="40878-122">Когда контекст хранилища основывается на проверке подлинности OAuth, он создает маркер SAS контейнера удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="40878-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="40878-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40878-123">-DefaultProfile</span></span>
<span data-ttu-id="40878-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40878-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40878-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="40878-125">-ExpiryTime</span></span>
<span data-ttu-id="40878-126">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="40878-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="40878-127">Если пользователь задает время начала, но не время окончания срока действия, в качестве времени окончания устанавливается время начала плюс один час.</span><span class="sxs-lookup"><span data-stu-id="40878-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="40878-128">Если не задано ни время начала, ни время окончания срока действия, в качестве времени окончания устанавливается текущее время плюс один час.</span><span class="sxs-lookup"><span data-stu-id="40878-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="40878-129">Если контекст хранилища основан на проверке подлинности OAuth, срок действия истекает через 7 дней с текущего времени и не должен предшествовать текущему времени.</span><span class="sxs-lookup"><span data-stu-id="40878-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="40878-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="40878-130">-FullUri</span></span>
<span data-ttu-id="40878-131">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="40878-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="40878-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="40878-132">-IPAddressOrRange</span></span>
<span data-ttu-id="40878-133">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="40878-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="40878-134">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="40878-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="40878-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40878-135">-Name</span></span>
<span data-ttu-id="40878-136">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="40878-136">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="40878-137">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="40878-137">-Permission</span></span>
<span data-ttu-id="40878-138">Задает разрешения для контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="40878-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="40878-139">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="40878-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="40878-140">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="40878-140">-Policy</span></span>
<span data-ttu-id="40878-141">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="40878-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="40878-142">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="40878-142">-Protocol</span></span>
<span data-ttu-id="40878-143">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="40878-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="40878-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="40878-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="40878-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="40878-145">HttpsOnly</span></span>
* <span data-ttu-id="40878-146">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="40878-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="40878-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="40878-147">-StartTime</span></span>
<span data-ttu-id="40878-148">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="40878-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="40878-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40878-149">-Confirm</span></span>
<span data-ttu-id="40878-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40878-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40878-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40878-151">-WhatIf</span></span>
<span data-ttu-id="40878-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40878-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40878-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40878-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40878-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40878-154">CommonParameters</span></span>
<span data-ttu-id="40878-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40878-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40878-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40878-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40878-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40878-157">INPUTS</span></span>

### <span data-ttu-id="40878-158">System. String</span><span class="sxs-lookup"><span data-stu-id="40878-158">System.String</span></span>

### <span data-ttu-id="40878-159">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="40878-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="40878-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40878-160">OUTPUTS</span></span>

### <span data-ttu-id="40878-161">System. String</span><span class="sxs-lookup"><span data-stu-id="40878-161">System.String</span></span>

## <span data-ttu-id="40878-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="40878-162">NOTES</span></span>

## <span data-ttu-id="40878-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40878-163">RELATED LINKS</span></span>

[<span data-ttu-id="40878-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="40878-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)