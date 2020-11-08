---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073458"
---
# <span data-ttu-id="c1b71-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="c1b71-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="c1b71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1b71-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b71-103">Создание маркера подписи общего доступа для общей папки хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b71-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="c1b71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1b71-104">SYNTAX</span></span>

### <span data-ttu-id="c1b71-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="c1b71-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1b71-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="c1b71-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b71-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1b71-107">DESCRIPTION</span></span>
<span data-ttu-id="c1b71-108">Командлет **New-AzStorageShareSASToken** создает маркер подписи для общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b71-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="c1b71-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1b71-109">EXAMPLES</span></span>

### <span data-ttu-id="c1b71-110">Пример 1: создание маркера цифровой подписи для общего доступа</span><span class="sxs-lookup"><span data-stu-id="c1b71-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="c1b71-111">Эта команда создает маркер подписи общего доступа для общей папки с именем ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="c1b71-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="c1b71-112">Пример 2: создание нескольких маркеров общего доступа к подписи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c1b71-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="c1b71-113">Эта команда получает все общие ресурсы хранилища, соответствующие проверке префикса.</span><span class="sxs-lookup"><span data-stu-id="c1b71-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="c1b71-114">Команда передает их в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="c1b71-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c1b71-115">Текущий командлет создает маркер общего доступа для каждой общей папки хранения с указанными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="c1b71-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="c1b71-116">Пример 3: создание маркера подписи общего доступа, использующего политику общего доступа</span><span class="sxs-lookup"><span data-stu-id="c1b71-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="c1b71-117">Эта команда создает маркер подписи общего доступа для общей папки хранения с именем ContosoShare, имеющей политику с именем ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="c1b71-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="c1b71-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1b71-118">PARAMETERS</span></span>

### <span data-ttu-id="c1b71-119">-Context</span><span class="sxs-lookup"><span data-stu-id="c1b71-119">-Context</span></span>
<span data-ttu-id="c1b71-120">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b71-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c1b71-121">Чтобы получить контекст, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c1b71-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c1b71-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b71-122">-DefaultProfile</span></span>
<span data-ttu-id="c1b71-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b71-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1b71-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c1b71-124">-ExpiryTime</span></span>
<span data-ttu-id="c1b71-125">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="c1b71-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="c1b71-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c1b71-126">-FullUri</span></span>
<span data-ttu-id="c1b71-127">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c1b71-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c1b71-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c1b71-128">-IPAddressOrRange</span></span>
<span data-ttu-id="c1b71-129">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="c1b71-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c1b71-130">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="c1b71-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="c1b71-131">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="c1b71-131">-Permission</span></span>
<span data-ttu-id="c1b71-132">Задает разрешения в маркере для доступа к общему доступу и файлам в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="c1b71-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="c1b71-133">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="c1b71-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c1b71-134">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="c1b71-134">-Policy</span></span>
<span data-ttu-id="c1b71-135">Указывает политику сохраненных прав доступа для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c1b71-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="c1b71-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c1b71-136">-Protocol</span></span>
<span data-ttu-id="c1b71-137">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="c1b71-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c1b71-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c1b71-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c1b71-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c1b71-139">HttpsOnly</span></span>
* <span data-ttu-id="c1b71-140">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c1b71-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c1b71-141">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="c1b71-141">-ShareName</span></span>
<span data-ttu-id="c1b71-142">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="c1b71-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b71-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c1b71-143">-StartTime</span></span>
<span data-ttu-id="c1b71-144">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="c1b71-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c1b71-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b71-145">CommonParameters</span></span>
<span data-ttu-id="c1b71-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1b71-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b71-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b71-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b71-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1b71-148">INPUTS</span></span>

### <span data-ttu-id="c1b71-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c1b71-149">System.String</span></span>

### <span data-ttu-id="c1b71-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c1b71-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c1b71-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1b71-151">OUTPUTS</span></span>

### <span data-ttu-id="c1b71-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c1b71-152">System.String</span></span>

## <span data-ttu-id="c1b71-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1b71-153">NOTES</span></span>
* <span data-ttu-id="c1b71-154">Ключевые слова: общие, Azure, службы, данные, хранилище, большой двоичный объект, очередь, таблица</span><span class="sxs-lookup"><span data-stu-id="c1b71-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="c1b71-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1b71-155">RELATED LINKS</span></span>

[<span data-ttu-id="c1b71-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1b71-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c1b71-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="c1b71-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
