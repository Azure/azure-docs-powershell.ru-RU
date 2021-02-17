---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241845"
---
# <span data-ttu-id="f114f-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="f114f-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="f114f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f114f-102">SYNOPSIS</span></span>
<span data-ttu-id="f114f-103">Создание маркера подписи общего доступа для общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="f114f-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="f114f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f114f-104">SYNTAX</span></span>

### <span data-ttu-id="f114f-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f114f-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f114f-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f114f-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f114f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f114f-107">DESCRIPTION</span></span>
<span data-ttu-id="f114f-108">**Новый-AzStorageShareSASToken cmdlet** создает маркер подписи общего доступа для общей области хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f114f-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="f114f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f114f-109">EXAMPLES</span></span>

### <span data-ttu-id="f114f-110">Пример 1. Создание маркера подписи общего доступа для общего доступа</span><span class="sxs-lookup"><span data-stu-id="f114f-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="f114f-111">Эта команда создает маркер подписи общего доступа для общего доступа ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="f114f-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="f114f-112">Пример 2. Создание нескольких маркеров подписи общего доступа с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="f114f-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="f114f-113">Эта команда возвращает все хранилища, которые соответствуют префиксу.</span><span class="sxs-lookup"><span data-stu-id="f114f-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="f114f-114">Команда передает их текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f114f-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f114f-115">Текущий cmdlet создает общий маркер доступа для каждой общей общей области хранения, которая имеет указанные разрешения.</span><span class="sxs-lookup"><span data-stu-id="f114f-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="f114f-116">Пример 3. Создание маркера подписи общего доступа с использованием политики общего доступа</span><span class="sxs-lookup"><span data-stu-id="f114f-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="f114f-117">Эта команда создает маркер подписи общего доступа для общей области хранения ContosoShare с политикой ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="f114f-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="f114f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f114f-118">PARAMETERS</span></span>

### <span data-ttu-id="f114f-119">-Контекст</span><span class="sxs-lookup"><span data-stu-id="f114f-119">-Context</span></span>
<span data-ttu-id="f114f-120">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f114f-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f114f-121">Для получения контекста используйте New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f114f-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f114f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f114f-122">-DefaultProfile</span></span>
<span data-ttu-id="f114f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f114f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f114f-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f114f-124">-ExpiryTime</span></span>
<span data-ttu-id="f114f-125">Время, в течение которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="f114f-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="f114f-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f114f-126">-FullUri</span></span>
<span data-ttu-id="f114f-127">Указывает на то, что этот cmdlet возвращает полный URI BLOB-приложений и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f114f-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="f114f-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f114f-128">-IPAddressOrRange</span></span>
<span data-ttu-id="f114f-129">Указывает IP-адрес или диапазон IP-адресов, с которых нужно принимать запросы, например 168.1.5.65 или 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="f114f-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f114f-130">Диапазон включительно.</span><span class="sxs-lookup"><span data-stu-id="f114f-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="f114f-131">-Permission</span><span class="sxs-lookup"><span data-stu-id="f114f-131">-Permission</span></span>
<span data-ttu-id="f114f-132">Определяет разрешения в токене для доступа к папке и файлам в этой папке.</span><span class="sxs-lookup"><span data-stu-id="f114f-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="f114f-133">Важно отметить, что это строка (для чтения, записи `rwd` и удаления).</span><span class="sxs-lookup"><span data-stu-id="f114f-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f114f-134">-Политика</span><span class="sxs-lookup"><span data-stu-id="f114f-134">-Policy</span></span>
<span data-ttu-id="f114f-135">Определяет хранимую политику доступа для доступа.</span><span class="sxs-lookup"><span data-stu-id="f114f-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="f114f-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f114f-136">-Protocol</span></span>
<span data-ttu-id="f114f-137">Определяет протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="f114f-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f114f-138">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f114f-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f114f-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f114f-139">HttpsOnly</span></span>
* <span data-ttu-id="f114f-140">По умолчанию httpsOrHttp имеет значение httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="f114f-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="f114f-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f114f-141">-ShareName</span></span>
<span data-ttu-id="f114f-142">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="f114f-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="f114f-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f114f-143">-StartTime</span></span>
<span data-ttu-id="f114f-144">Время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="f114f-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="f114f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f114f-145">CommonParameters</span></span>
<span data-ttu-id="f114f-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f114f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f114f-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f114f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f114f-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f114f-148">INPUTS</span></span>

### <span data-ttu-id="f114f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f114f-149">System.String</span></span>

### <span data-ttu-id="f114f-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f114f-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f114f-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f114f-151">OUTPUTS</span></span>

### <span data-ttu-id="f114f-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f114f-152">System.String</span></span>

## <span data-ttu-id="f114f-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f114f-153">NOTES</span></span>
* <span data-ttu-id="f114f-154">Ключевые слова: общие, azure, службы, данные, хранилище, BLOB-бизнес, очередь, таблица</span><span class="sxs-lookup"><span data-stu-id="f114f-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="f114f-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f114f-155">RELATED LINKS</span></span>

[<span data-ttu-id="f114f-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f114f-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="f114f-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="f114f-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
