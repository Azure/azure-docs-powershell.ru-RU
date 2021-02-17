---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241864"
---
# <span data-ttu-id="365d9-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="365d9-101">New-AzStorageContext</span></span>

## <span data-ttu-id="365d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="365d9-102">SYNOPSIS</span></span>
<span data-ttu-id="365d9-103">Создает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="365d9-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="365d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="365d9-104">SYNTAX</span></span>

### <span data-ttu-id="365d9-105">OAuthAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="365d9-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="365d9-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="365d9-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="365d9-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="365d9-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="365d9-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="365d9-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="365d9-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="365d9-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="365d9-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="365d9-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="365d9-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="365d9-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="365d9-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="365d9-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="365d9-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="365d9-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="365d9-114">Local Темы</span><span class="sxs-lookup"><span data-stu-id="365d9-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="365d9-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="365d9-115">DESCRIPTION</span></span>
<span data-ttu-id="365d9-116">Для создания контекста хранилища Azure создается **cmdlet New-AzStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="365d9-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="365d9-117">По умолчанию для контекста хранилища задается проверка подлинности OAuth (Azure AD), если только входная учетная запись хранилища называется.</span><span class="sxs-lookup"><span data-stu-id="365d9-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="365d9-118">Подробные сведения о проверке подлинности службы хранилища см. в https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="365d9-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="365d9-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="365d9-119">EXAMPLES</span></span>

### <span data-ttu-id="365d9-120">Пример 1. Создание контекста путем указания имени учетной записи хранения и ключа</span><span class="sxs-lookup"><span data-stu-id="365d9-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="365d9-121">Эта команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="365d9-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="365d9-122">Пример 2. Создание контекста путем указания строки подключения</span><span class="sxs-lookup"><span data-stu-id="365d9-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="365d9-123">Эта команда создает контекст на основе указанной строки подключения для учетной записи ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="365d9-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="365d9-124">Пример 3. Создание контекста для анонимной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="365d9-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="365d9-125">Эта команда создает контекст для анонимного использования учетной записи ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="365d9-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="365d9-126">Команда определяет HTTP как протокол подключения.</span><span class="sxs-lookup"><span data-stu-id="365d9-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="365d9-127">Пример 4. Создание контекста с помощью локальной учетной записи хранилища разработки</span><span class="sxs-lookup"><span data-stu-id="365d9-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="365d9-128">Эта команда создает контекст с использованием локальной учетной записи хранилища разработки.</span><span class="sxs-lookup"><span data-stu-id="365d9-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="365d9-129">Команда определяет *локальный* параметр.</span><span class="sxs-lookup"><span data-stu-id="365d9-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="365d9-130">Пример 5. Получите контейнер для локальной учетной записи разработчика</span><span class="sxs-lookup"><span data-stu-id="365d9-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="365d9-131">Эта команда создает контекст с использованием локальной учетной записи хранилища разработки, а затем передает новый контекст **командлету Get-AzStorageContainer** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="365d9-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="365d9-132">Команда получает контейнер хранилища Azure для локальной учетной записи разработчика.</span><span class="sxs-lookup"><span data-stu-id="365d9-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="365d9-133">Пример 6. Получите несколько контейнеров</span><span class="sxs-lookup"><span data-stu-id="365d9-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="365d9-134">Первая команда создает контекст с использованием локальной учетной записи хранилища разработки, а затем сохраняет его в переменной $Context 01.</span><span class="sxs-lookup"><span data-stu-id="365d9-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="365d9-135">Вторая команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ, а затем сохраняет этот контекст в переменной $Context 02.</span><span class="sxs-lookup"><span data-stu-id="365d9-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="365d9-136">Конечная команда получает контейнеры контекстов, хранимых в $Context 01 и $Context 02, с помощью **Get-AzStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="365d9-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="365d9-137">Пример 7. Создание контекста с конечной точкой</span><span class="sxs-lookup"><span data-stu-id="365d9-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="365d9-138">Эта команда создает контекст хранилища Azure с указанной конечной точкой хранилища.</span><span class="sxs-lookup"><span data-stu-id="365d9-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="365d9-139">Эта команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="365d9-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="365d9-140">Пример 8. Создание контекста с определенной средой</span><span class="sxs-lookup"><span data-stu-id="365d9-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="365d9-141">Эта команда создает контекст хранилища Azure с указанной средой Azure.</span><span class="sxs-lookup"><span data-stu-id="365d9-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="365d9-142">Эта команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="365d9-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="365d9-143">Пример 9. Создание контекста с помощью маркера SAS</span><span class="sxs-lookup"><span data-stu-id="365d9-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="365d9-144">Первая команда создает токен SAS с помощью командлета **New-AzStorageContainerSASToken** для контейнера ContosoMain, а затем сохраняет его в переменной $SasToken.</span><span class="sxs-lookup"><span data-stu-id="365d9-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="365d9-145">Этот маркер для разрешений на чтение, добавление, обновление и удаление.</span><span class="sxs-lookup"><span data-stu-id="365d9-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="365d9-146">Вторая команда создает контекст для учетной записи ContosoGeneral, использующей маркер SAS из $SasToken, а затем сохраняет этот контекст в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="365d9-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="365d9-147">В конечной команде перечислены все BLOB-lob-lob, связанные с контейнером ContosoMain, используя контекст, $Context.</span><span class="sxs-lookup"><span data-stu-id="365d9-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="365d9-148">Пример 10. Создание контекста с помощью проверки подлинности OAuth</span><span class="sxs-lookup"><span data-stu-id="365d9-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="365d9-149">Эта команда создает контекст с помощью проверки подлинности OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="365d9-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="365d9-150">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="365d9-150">PARAMETERS</span></span>

### <span data-ttu-id="365d9-151">-Анонимный</span><span class="sxs-lookup"><span data-stu-id="365d9-151">-Anonymous</span></span>
<span data-ttu-id="365d9-152">Указывает на то, что этот cmdlet создает контекст хранилища Azure для анонимного логотипа.</span><span class="sxs-lookup"><span data-stu-id="365d9-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="365d9-153">-ConnectionString</span></span>
<span data-ttu-id="365d9-154">Указывает строку подключения для контекста хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="365d9-154">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-155">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="365d9-155">-Endpoint</span></span>
<span data-ttu-id="365d9-156">Указывает конечную точку для контекста хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="365d9-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-157">-Среда</span><span class="sxs-lookup"><span data-stu-id="365d9-157">-Environment</span></span>
<span data-ttu-id="365d9-158">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="365d9-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="365d9-159">Допустимыми значениями для этого параметра являются AzureCloud и AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="365d9-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="365d9-160">Для получения дополнительных сведений введите `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="365d9-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-161">-Local</span><span class="sxs-lookup"><span data-stu-id="365d9-161">-Local</span></span>
<span data-ttu-id="365d9-162">Указывает на то, что этот cmdlet создает контекст с использованием локальной учетной записи хранилища разработки.</span><span class="sxs-lookup"><span data-stu-id="365d9-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-163">-Protocol</span><span class="sxs-lookup"><span data-stu-id="365d9-163">-Protocol</span></span>
<span data-ttu-id="365d9-164">Передача протокола (https/http).</span><span class="sxs-lookup"><span data-stu-id="365d9-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="365d9-165">-SasToken</span></span>
<span data-ttu-id="365d9-166">Указывает маркер подписи общего доступа (SAS) для контекста.</span><span class="sxs-lookup"><span data-stu-id="365d9-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="365d9-167">-StorageAccountKey</span></span>
<span data-ttu-id="365d9-168">Указывает ключ учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="365d9-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="365d9-169">Этот cmdlet создает контекст для ключа, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="365d9-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="365d9-170">-StorageAccountName</span></span>
<span data-ttu-id="365d9-171">Указывает имя учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="365d9-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="365d9-172">Этот cmdlet создает контекст для учетной записи, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="365d9-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="365d9-173">-UseConnectedAccount</span></span>
<span data-ttu-id="365d9-174">Указывает на то, что этот cmdlet создает контекст хранилища Azure с проверкой подлинности OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="365d9-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="365d9-175">По умолчанию для этого используется проверка подлинности OAuth, если не указана другая проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="365d9-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365d9-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365d9-176">CommonParameters</span></span>
<span data-ttu-id="365d9-177">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365d9-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365d9-178">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="365d9-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365d9-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="365d9-179">INPUTS</span></span>

### <span data-ttu-id="365d9-180">System.String</span><span class="sxs-lookup"><span data-stu-id="365d9-180">System.String</span></span>

## <span data-ttu-id="365d9-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="365d9-181">OUTPUTS</span></span>

### <span data-ttu-id="365d9-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="365d9-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="365d9-183">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="365d9-183">NOTES</span></span>

## <span data-ttu-id="365d9-184">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="365d9-184">RELATED LINKS</span></span>

[<span data-ttu-id="365d9-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="365d9-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="365d9-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="365d9-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


