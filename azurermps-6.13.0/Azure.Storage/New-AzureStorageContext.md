---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 9de6b2b52205bdf80de9c57e3e338f4b7216c5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566019"
---
# <span data-ttu-id="2e0a9-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e0a9-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="2e0a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0a9-103">Создает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e0a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e0a9-104">SYNTAX</span></span>

### <span data-ttu-id="2e0a9-105">OAuthAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e0a9-105">OAuthAccount (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="2e0a9-106">AccountNameAndKey</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="2e0a9-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="2e0a9-108">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="2e0a9-109">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="2e0a9-110">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2e0a9-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="2e0a9-112">OAuthAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-113">Подключения</span><span class="sxs-lookup"><span data-stu-id="2e0a9-113">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="2e0a9-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="2e0a9-114">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="2e0a9-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e0a9-115">DESCRIPTION</span></span>
<span data-ttu-id="2e0a9-116">Командлет **New-AzureStorageContext** создает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-116">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="2e0a9-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e0a9-117">EXAMPLES</span></span>

### <span data-ttu-id="2e0a9-118">Пример 1: создание контекста с указанием имени и ключа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2e0a9-118">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="2e0a9-119">Эта команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-119">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="2e0a9-120">Пример 2: создание контекста путем указания строки соединения</span><span class="sxs-lookup"><span data-stu-id="2e0a9-120">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="2e0a9-121">Эта команда создает контекст на основе указанной строки подключения для учетной записи ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-121">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="2e0a9-122">Пример 3: создание контекста для анонимной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2e0a9-122">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="2e0a9-123">Эта команда создает контекст для анонимного использования учетной записи с именем ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-123">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="2e0a9-124">Команда указывает HTTP как протокол подключения.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-124">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="2e0a9-125">Пример 4: создание контекста с помощью локальной учетной записи хранения для разработки</span><span class="sxs-lookup"><span data-stu-id="2e0a9-125">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="2e0a9-126">Эта команда создает контекст с помощью локальной учетной записи хранения разработки.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-126">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="2e0a9-127">Команда задает *локальный* параметр.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-127">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="2e0a9-128">Пример 5: получение контейнера для локальной учетной записи хранения разработчика</span><span class="sxs-lookup"><span data-stu-id="2e0a9-128">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="2e0a9-129">Эта команда создает контекст с помощью локальной учетной записи хранения разработки, а затем передает новый контекст командлету **Get-AzureStorageContainer** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-129">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2e0a9-130">Команда получает контейнер хранилища Azure для локальной учетной записи хранилища разработчика.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-130">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="2e0a9-131">Пример 6: получение нескольких контейнеров</span><span class="sxs-lookup"><span data-stu-id="2e0a9-131">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="2e0a9-132">Первая команда создает контекст с помощью локальной учетной записи хранения разработки и сохраняет этот контекст в переменной $Context 01.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-132">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="2e0a9-133">Вторая команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ, и сохраняет этот контекст в переменной $Context 02.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-133">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="2e0a9-134">Последняя команда получает контейнеры для контекстов, которые хранятся в $Context 01 и $Context 02 с помощью **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-134">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="2e0a9-135">Пример 7: создание контекста с конечной точкой</span><span class="sxs-lookup"><span data-stu-id="2e0a9-135">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="2e0a9-136">Эта команда создает контекст хранилища Azure, который содержит указанную конечную точку хранилища.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-136">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="2e0a9-137">Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-137">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="2e0a9-138">Пример 8: создание контекста с указанной средой</span><span class="sxs-lookup"><span data-stu-id="2e0a9-138">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="2e0a9-139">Эта команда создает контекст хранилища Azure, который содержит указанную среду Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-139">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="2e0a9-140">Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-140">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="2e0a9-141">Пример 9: создание контекста с помощью маркера SAS</span><span class="sxs-lookup"><span data-stu-id="2e0a9-141">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="2e0a9-142">Первая команда создает маркер SAS с помощью командлета **New-AzureStorageContainerSASToken** для контейнера с именем ContosoMain и сохраняет этот маркер в переменной $SasToken.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-142">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="2e0a9-143">Этот маркер предназначен для чтения, добавления, обновления и удаления разрешений.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-143">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="2e0a9-144">Вторая команда создает контекст для учетной записи с именем ContosoGeneral, который использует маркер SAS, хранящийся в $SasToken, и сохраняет этот контекст в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-144">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="2e0a9-145">В последней команде перечисляются все BLOB-объекты, связанные с контейнером с именем ContosoMain, используя контекст, хранящийся в $Context.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-145">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="2e0a9-146">Пример 10: создание контекста с использованием проверки подлинности OAuth</span><span class="sxs-lookup"><span data-stu-id="2e0a9-146">Example 10: Create a context by using the OAuth Authentication</span></span>
```
C:\PS>Connect-AzureRmAccount
C:\PS> $Context = New-AzureStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="2e0a9-147">Эта команда создает контекст с использованием проверки подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-147">This command creates a context by using the OAuth Authentication.</span></span>

## <span data-ttu-id="2e0a9-148">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e0a9-148">PARAMETERS</span></span>

### <span data-ttu-id="2e0a9-149">-Анонимный</span><span class="sxs-lookup"><span data-stu-id="2e0a9-149">-Anonymous</span></span>
<span data-ttu-id="2e0a9-150">Указывает на то, что этот командлет создает контекст хранилища Azure для анонимного входа.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-150">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="2e0a9-151">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2e0a9-151">-ConnectionString</span></span>
<span data-ttu-id="2e0a9-152">Указывает строку подключения для контекста хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-152">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="2e0a9-153">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="2e0a9-153">-Endpoint</span></span>
<span data-ttu-id="2e0a9-154">Задает конечную точку контекста хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-154">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="2e0a9-155">-Environment</span><span class="sxs-lookup"><span data-stu-id="2e0a9-155">-Environment</span></span>
<span data-ttu-id="2e0a9-156">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-156">Specifies the Azure environment.</span></span>
<span data-ttu-id="2e0a9-157">Допустимые значения этого параметра: AzureCloud и AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-157">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="2e0a9-158">Для получения дополнительных сведений введите `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="2e0a9-158">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

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

### <span data-ttu-id="2e0a9-159">-Local</span><span class="sxs-lookup"><span data-stu-id="2e0a9-159">-Local</span></span>
<span data-ttu-id="2e0a9-160">Указывает на то, что этот командлет создает контекст с помощью локальной учетной записи хранения разработки.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-160">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="2e0a9-161">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="2e0a9-161">-Protocol</span></span>
<span data-ttu-id="2e0a9-162">Протокол передачи (HTTPS/HTTP).</span><span class="sxs-lookup"><span data-stu-id="2e0a9-162">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="2e0a9-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="2e0a9-163">-SasToken</span></span>
<span data-ttu-id="2e0a9-164">Указывает маркер общего доступа к подписи (SAS) для контекста.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="2e0a9-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2e0a9-165">-StorageAccountKey</span></span>
<span data-ttu-id="2e0a9-166">Указывает ключ учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="2e0a9-167">Этот командлет создает контекст для ключа, указывающего на этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e0a9-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2e0a9-168">-StorageAccountName</span></span>
<span data-ttu-id="2e0a9-169">Указывает имя учетной записи службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="2e0a9-170">Этот командлет создает контекст для учетной записи, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e0a9-171">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="2e0a9-171">-UseConnectedAccount</span></span>
<span data-ttu-id="2e0a9-172">Указывает на то, что этот командлет создает контекст хранилища Azure с проверкой подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-172">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="2e0a9-173">По умолчанию командлет использует проверку подлинности OAuth, если другие anthentication не указаны.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-173">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e0a9-174">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="2e0a9-174">-UseConnectedAccount</span></span>
<span data-ttu-id="2e0a9-175">Указывает на то, что этот командлет создает контекст хранилища Azure с проверкой подлинности OAuth.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-175">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="2e0a9-176">По умолчанию командлет использует проверку подлинности OAuth, если другие anthentication не указаны.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-176">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e0a9-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0a9-177">CommonParameters</span></span>
<span data-ttu-id="2e0a9-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0a9-179">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e0a9-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0a9-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e0a9-180">INPUTS</span></span>

### <span data-ttu-id="2e0a9-181">System. String</span><span class="sxs-lookup"><span data-stu-id="2e0a9-181">System.String</span></span>

## <span data-ttu-id="2e0a9-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e0a9-182">OUTPUTS</span></span>

### <span data-ttu-id="2e0a9-183">Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e0a9-183">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="2e0a9-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e0a9-184">NOTES</span></span>

## <span data-ttu-id="2e0a9-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e0a9-185">RELATED LINKS</span></span>

[<span data-ttu-id="2e0a9-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2e0a9-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="2e0a9-187">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2e0a9-187">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


