---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
ms.openlocfilehash: 0e8ad44ebbd8a5585626de27317caa14b408f87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567035"
---
# <span data-ttu-id="60c01-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="60c01-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="60c01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60c01-102">SYNOPSIS</span></span>
<span data-ttu-id="60c01-103">Создание маркера SAS для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="60c01-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60c01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60c01-104">SYNTAX</span></span>

### <span data-ttu-id="60c01-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="60c01-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="60c01-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="60c01-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="60c01-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60c01-107">DESCRIPTION</span></span>
<span data-ttu-id="60c01-108">Командлет **New-AzureStorageContainerSASToken** создает маркер подписи общего доступа (SAS) для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="60c01-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="60c01-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60c01-109">EXAMPLES</span></span>

### <span data-ttu-id="60c01-110">Пример 1: создание маркера безопасности контейнера с разрешениями полного контейнера</span><span class="sxs-lookup"><span data-stu-id="60c01-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="60c01-111">В этом примере создается маркер безопасности контейнера с разрешениями полного контейнера.</span><span class="sxs-lookup"><span data-stu-id="60c01-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="60c01-112">Пример 2: создание маркера SAS с несколькими контейнерами с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="60c01-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="60c01-113">В этом примере создается несколько маркеров сопоставления безопасности контейнера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="60c01-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="60c01-114">Пример 3: создание маркера SAS контейнера с политикой общего доступа</span><span class="sxs-lookup"><span data-stu-id="60c01-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="60c01-115">В этом примере создается маркер SAS контейнера с политикой общего доступа.</span><span class="sxs-lookup"><span data-stu-id="60c01-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="60c01-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60c01-116">PARAMETERS</span></span>

### <span data-ttu-id="60c01-117">-Context</span><span class="sxs-lookup"><span data-stu-id="60c01-117">-Context</span></span>
<span data-ttu-id="60c01-118">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="60c01-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="60c01-119">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="60c01-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="60c01-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="60c01-120">-ExpiryTime</span></span>
<span data-ttu-id="60c01-121">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="60c01-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="60c01-122">Если пользователь задает время начала, но не время окончания срока действия, в качестве времени окончания устанавливается время начала плюс один час.</span><span class="sxs-lookup"><span data-stu-id="60c01-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="60c01-123">Если не задано ни время начала, ни время окончания срока действия, в качестве времени окончания устанавливается текущее время плюс один час.</span><span class="sxs-lookup"><span data-stu-id="60c01-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="60c01-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="60c01-124">-FullUri</span></span>
<span data-ttu-id="60c01-125">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="60c01-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="60c01-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="60c01-126">-IPAddressOrRange</span></span>
<span data-ttu-id="60c01-127">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="60c01-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="60c01-128">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="60c01-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="60c01-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60c01-129">-Name</span></span>
<span data-ttu-id="60c01-130">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="60c01-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60c01-131">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="60c01-131">-Permission</span></span>
<span data-ttu-id="60c01-132">Задает разрешения для контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="60c01-132">Specifies permissions for a storage container.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c01-133">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="60c01-133">-Policy</span></span>
<span data-ttu-id="60c01-134">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="60c01-134">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c01-135">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="60c01-135">-Protocol</span></span>
<span data-ttu-id="60c01-136">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="60c01-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="60c01-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="60c01-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="60c01-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="60c01-138">HttpsOnly</span></span>
* <span data-ttu-id="60c01-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="60c01-139">HttpsOrHttp</span></span>

<span data-ttu-id="60c01-140">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="60c01-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="60c01-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="60c01-141">-StartTime</span></span>
<span data-ttu-id="60c01-142">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="60c01-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="60c01-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c01-143">CommonParameters</span></span>
<span data-ttu-id="60c01-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60c01-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c01-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c01-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c01-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60c01-146">INPUTS</span></span>

### <span data-ttu-id="60c01-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="60c01-147">IStorageContext</span></span>

<span data-ttu-id="60c01-148">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="60c01-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="60c01-149">Подстрок</span><span class="sxs-lookup"><span data-stu-id="60c01-149">String</span></span>

<span data-ttu-id="60c01-150">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="60c01-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="60c01-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60c01-151">OUTPUTS</span></span>

### <span data-ttu-id="60c01-152">System. String</span><span class="sxs-lookup"><span data-stu-id="60c01-152">System.String</span></span>

## <span data-ttu-id="60c01-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="60c01-153">NOTES</span></span>

## <span data-ttu-id="60c01-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60c01-154">RELATED LINKS</span></span>

[<span data-ttu-id="60c01-155">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="60c01-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
