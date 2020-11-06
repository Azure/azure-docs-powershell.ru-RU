---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
ms.openlocfilehash: 44080736635a5b4e8964340aeeee448798ffaefc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565063"
---
# <span data-ttu-id="c408a-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="c408a-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="c408a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c408a-102">SYNOPSIS</span></span>
<span data-ttu-id="c408a-103">Создание маркера подписи общего доступа для общей папки хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c408a-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c408a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c408a-104">SYNTAX</span></span>

### <span data-ttu-id="c408a-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="c408a-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="c408a-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="c408a-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="c408a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c408a-107">DESCRIPTION</span></span>
<span data-ttu-id="c408a-108">Командлет **New-AzureStorageShareSASToken** создает маркер подписи для общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="c408a-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="c408a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c408a-109">EXAMPLES</span></span>

### <span data-ttu-id="c408a-110">Пример 1: создание маркера цифровой подписи для общего доступа</span><span class="sxs-lookup"><span data-stu-id="c408a-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="c408a-111">Эта команда создает маркер подписи общего доступа для общей папки с именем ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="c408a-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="c408a-112">Пример 2: создание нескольких маркеров общего доступа к подписи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c408a-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="c408a-113">Эта команда получает все общие ресурсы хранилища, соответствующие проверке префикса.</span><span class="sxs-lookup"><span data-stu-id="c408a-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="c408a-114">Команда передает их в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="c408a-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c408a-115">Текущий командлет создает маркер общего доступа для каждой общей папки хранения с указанными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="c408a-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="c408a-116">Пример 3: создание маркера подписи общего доступа, использующего политику общего доступа</span><span class="sxs-lookup"><span data-stu-id="c408a-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="c408a-117">Эта команда создает маркер подписи общего доступа для общей папки хранения с именем ContosoShare, имеющей политику с именем ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="c408a-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="c408a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c408a-118">PARAMETERS</span></span>

### <span data-ttu-id="c408a-119">-Context</span><span class="sxs-lookup"><span data-stu-id="c408a-119">-Context</span></span>
<span data-ttu-id="c408a-120">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c408a-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c408a-121">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c408a-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c408a-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c408a-122">-ExpiryTime</span></span>
<span data-ttu-id="c408a-123">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="c408a-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="c408a-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c408a-124">-FullUri</span></span>
<span data-ttu-id="c408a-125">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c408a-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c408a-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c408a-126">-IPAddressOrRange</span></span>
<span data-ttu-id="c408a-127">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="c408a-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c408a-128">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="c408a-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="c408a-129">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="c408a-129">-Permission</span></span>
<span data-ttu-id="c408a-130">Задает разрешения в маркере для доступа к общему доступу и файлам в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="c408a-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

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

### <span data-ttu-id="c408a-131">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="c408a-131">-Policy</span></span>
<span data-ttu-id="c408a-132">Указывает политику сохраненных прав доступа для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c408a-132">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="c408a-133">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c408a-133">-Protocol</span></span>
<span data-ttu-id="c408a-134">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="c408a-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c408a-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c408a-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c408a-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c408a-136">HttpsOnly</span></span>
* <span data-ttu-id="c408a-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="c408a-137">HttpsOrHttp</span></span>

<span data-ttu-id="c408a-138">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c408a-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c408a-139">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="c408a-139">-ShareName</span></span>
<span data-ttu-id="c408a-140">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="c408a-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c408a-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c408a-141">-StartTime</span></span>
<span data-ttu-id="c408a-142">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="c408a-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c408a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c408a-143">CommonParameters</span></span>
<span data-ttu-id="c408a-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c408a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c408a-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c408a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c408a-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c408a-146">INPUTS</span></span>

### <span data-ttu-id="c408a-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c408a-147">IStorageContext</span></span>

<span data-ttu-id="c408a-148">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c408a-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c408a-149">Подстрок</span><span class="sxs-lookup"><span data-stu-id="c408a-149">String</span></span>

<span data-ttu-id="c408a-150">Параметр ShareName принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c408a-150">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c408a-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c408a-151">OUTPUTS</span></span>

### <span data-ttu-id="c408a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c408a-152">System.String</span></span>

## <span data-ttu-id="c408a-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="c408a-153">NOTES</span></span>
* <span data-ttu-id="c408a-154">Ключевые слова: общие, Azure, службы, данные, хранилище, большой двоичный объект, очередь, таблица</span><span class="sxs-lookup"><span data-stu-id="c408a-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="c408a-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c408a-155">RELATED LINKS</span></span>

[<span data-ttu-id="c408a-156">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c408a-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="c408a-157">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="c408a-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
