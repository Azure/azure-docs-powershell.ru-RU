---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4db0b752e8bf887e899a4de6a8e4175eaa2d9855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555908"
---
# <span data-ttu-id="7fbf7-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fbf7-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="7fbf7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fbf7-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbf7-103">Создает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="7fbf7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fbf7-104">SYNTAX</span></span>

### <span data-ttu-id="7fbf7-105">AccountNameAndKey (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fbf7-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7fbf7-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="7fbf7-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="7fbf7-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="7fbf7-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fbf7-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="7fbf7-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="7fbf7-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="7fbf7-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7fbf7-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7fbf7-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="7fbf7-111">Подключения</span><span class="sxs-lookup"><span data-stu-id="7fbf7-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="7fbf7-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="7fbf7-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="7fbf7-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fbf7-113">DESCRIPTION</span></span>
<span data-ttu-id="7fbf7-114">Командлет **New-AzureStorageContext** создает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="7fbf7-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fbf7-115">EXAMPLES</span></span>

### <span data-ttu-id="7fbf7-116">Пример 1: создание контекста с указанием имени и ключа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7fbf7-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="7fbf7-117">Эта команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7fbf7-118">Пример 2: создание контекста путем указания строки соединения</span><span class="sxs-lookup"><span data-stu-id="7fbf7-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="7fbf7-119">Эта команда создает контекст на основе указанной строки подключения для учетной записи ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="7fbf7-120">Пример 3: создание контекста для анонимной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7fbf7-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="7fbf7-121">Эта команда создает контекст для анонимного использования учетной записи с именем ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="7fbf7-122">Команда указывает HTTP как протокол подключения.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="7fbf7-123">Пример 4: создание контекста с помощью локальной учетной записи хранения для разработки</span><span class="sxs-lookup"><span data-stu-id="7fbf7-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="7fbf7-124">Эта команда создает контекст с помощью локальной учетной записи хранения разработки.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="7fbf7-125">Команда задает *локальный* параметр.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="7fbf7-126">Пример 5: получение контейнера для локальной учетной записи хранения разработчика</span><span class="sxs-lookup"><span data-stu-id="7fbf7-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="7fbf7-127">Эта команда создает контекст с помощью локальной учетной записи хранения разработки, а затем передает новый контекст командлету **Get-AzureStorageContainer** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7fbf7-128">Команда получает контейнер хранилища Azure для локальной учетной записи хранилища разработчика.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="7fbf7-129">Пример 6: получение нескольких контейнеров</span><span class="sxs-lookup"><span data-stu-id="7fbf7-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="7fbf7-130">Первая команда создает контекст с помощью локальной учетной записи хранения разработки и сохраняет этот контекст в переменной $Context 01.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>

<span data-ttu-id="7fbf7-131">Вторая команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ, и сохраняет этот контекст в переменной $Context 02.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>

<span data-ttu-id="7fbf7-132">Последняя команда получает контейнеры для контекстов, которые хранятся в $Context 01 и $Context 02 с помощью **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="7fbf7-133">Пример 7: создание контекста с конечной точкой</span><span class="sxs-lookup"><span data-stu-id="7fbf7-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="7fbf7-134">Эта команда создает контекст хранилища Azure, который содержит указанную конечную точку хранилища.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="7fbf7-135">Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7fbf7-136">Пример 8: создание контекста с указанной средой</span><span class="sxs-lookup"><span data-stu-id="7fbf7-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="7fbf7-137">Эта команда создает контекст хранилища Azure, который содержит указанную среду Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="7fbf7-138">Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7fbf7-139">Пример 9: создание контекста с помощью маркера SAS</span><span class="sxs-lookup"><span data-stu-id="7fbf7-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="7fbf7-140">Первая команда создает маркер SAS с помощью командлета **New-AzureStorageContainerSASToken** для контейнера с именем ContosoMain и сохраняет этот маркер в переменной $SasToken.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="7fbf7-141">Этот маркер предназначен для чтения, добавления, обновления и удаления разрешений.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-141">That token is for read, add, update, and delete permissions.</span></span>

<span data-ttu-id="7fbf7-142">Вторая команда создает контекст для учетной записи с именем ContosoGeneral, который использует маркер SAS, хранящийся в $SasToken, и сохраняет этот контекст в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>

<span data-ttu-id="7fbf7-143">В последней команде перечисляются все BLOB-объекты, связанные с контейнером с именем ContosoMain, используя контекст, хранящийся в $Context.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="7fbf7-144">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fbf7-144">PARAMETERS</span></span>

### <span data-ttu-id="7fbf7-145">-Анонимный</span><span class="sxs-lookup"><span data-stu-id="7fbf7-145">-Anonymous</span></span>
<span data-ttu-id="7fbf7-146">Указывает на то, что этот командлет создает контекст хранилища Azure для анонимного входа.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7fbf7-147">-ConnectionString</span></span>
<span data-ttu-id="7fbf7-148">Указывает строку подключения для контекста хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-149">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="7fbf7-149">-Endpoint</span></span>
<span data-ttu-id="7fbf7-150">Задает конечную точку контекста хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-151">-Environment</span><span class="sxs-lookup"><span data-stu-id="7fbf7-151">-Environment</span></span>
<span data-ttu-id="7fbf7-152">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="7fbf7-153">Допустимые значения этого параметра: AzureCloud и AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="7fbf7-154">Для получения дополнительных сведений введите `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="7fbf7-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-155">-Local</span><span class="sxs-lookup"><span data-stu-id="7fbf7-155">-Local</span></span>
<span data-ttu-id="7fbf7-156">Указывает на то, что этот командлет создает контекст с помощью локальной учетной записи хранения разработки.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-157">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="7fbf7-157">-Protocol</span></span>
<span data-ttu-id="7fbf7-158">Указывает протокол, разрешенный для запроса, созданного с помощью сопоставлений безопасности учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-158">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="7fbf7-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7fbf7-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7fbf7-160">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7fbf7-160">HttpsOnly</span></span>
- <span data-ttu-id="7fbf7-161">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="7fbf7-161">HttpsOrHttp</span></span>

<span data-ttu-id="7fbf7-162">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-162">The default value is HttpsOrHttp.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="7fbf7-163">-SasToken</span></span>
<span data-ttu-id="7fbf7-164">Указывает маркер общего доступа к подписи (SAS) для контекста.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7fbf7-165">-StorageAccountKey</span></span>
<span data-ttu-id="7fbf7-166">Указывает ключ учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="7fbf7-167">Этот командлет создает контекст для ключа, указывающего на этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7fbf7-168">-StorageAccountName</span></span>
<span data-ttu-id="7fbf7-169">Указывает имя учетной записи службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="7fbf7-170">Этот командлет создает контекст для учетной записи, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbf7-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbf7-171">CommonParameters</span></span>
<span data-ttu-id="7fbf7-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fbf7-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbf7-173">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbf7-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbf7-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fbf7-174">INPUTS</span></span>

## <span data-ttu-id="7fbf7-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fbf7-175">OUTPUTS</span></span>

### <span data-ttu-id="7fbf7-176">AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fbf7-176">AzureStorageContext</span></span>

## <span data-ttu-id="7fbf7-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fbf7-177">NOTES</span></span>

## <span data-ttu-id="7fbf7-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fbf7-178">RELATED LINKS</span></span>

[<span data-ttu-id="7fbf7-179">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7fbf7-179">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="7fbf7-180">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7fbf7-180">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


