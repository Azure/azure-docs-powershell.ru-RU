---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: eca1322f1638039fce6c478b19e94b586fd83bbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907293"
---
# <span data-ttu-id="d8670-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8670-101">New-AzStorageContext</span></span>

## <span data-ttu-id="d8670-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8670-102">SYNOPSIS</span></span>
<span data-ttu-id="d8670-103">Создает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d8670-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="d8670-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8670-104">SYNTAX</span></span>

### <span data-ttu-id="d8670-105">OAuthAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8670-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8670-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="d8670-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8670-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="d8670-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d8670-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="d8670-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8670-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d8670-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d8670-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="d8670-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8670-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d8670-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d8670-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d8670-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d8670-113">Подключения</span><span class="sxs-lookup"><span data-stu-id="d8670-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="d8670-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="d8670-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="d8670-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8670-115">DESCRIPTION</span></span>
<span data-ttu-id="d8670-116">Командлет **New-AzStorageContext** создает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d8670-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="d8670-117">Проверка подлинности контекста хранения по умолчанию — OAuth (Azure AD), если только имя учетной записи хранения ввода.</span><span class="sxs-lookup"><span data-stu-id="d8670-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="d8670-118">Ознакомьтесь с подробными сведениями о проверке подлинности службы хранилища в https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="d8670-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="d8670-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8670-119">EXAMPLES</span></span>

### <span data-ttu-id="d8670-120">Пример 1: создание контекста с указанием имени и ключа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d8670-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="d8670-121">Эта команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="d8670-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d8670-122">Пример 2: создание контекста путем указания строки соединения</span><span class="sxs-lookup"><span data-stu-id="d8670-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="d8670-123">Эта команда создает контекст на основе указанной строки подключения для учетной записи ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="d8670-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="d8670-124">Пример 3: создание контекста для анонимной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d8670-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="d8670-125">Эта команда создает контекст для анонимного использования учетной записи с именем ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="d8670-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="d8670-126">Команда указывает HTTP как протокол подключения.</span><span class="sxs-lookup"><span data-stu-id="d8670-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="d8670-127">Пример 4: создание контекста с помощью локальной учетной записи хранения для разработки</span><span class="sxs-lookup"><span data-stu-id="d8670-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="d8670-128">Эта команда создает контекст с помощью локальной учетной записи хранения разработки.</span><span class="sxs-lookup"><span data-stu-id="d8670-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="d8670-129">Команда задает *локальный* параметр.</span><span class="sxs-lookup"><span data-stu-id="d8670-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="d8670-130">Пример 5: получение контейнера для локальной учетной записи хранения разработчика</span><span class="sxs-lookup"><span data-stu-id="d8670-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="d8670-131">Эта команда создает контекст с помощью локальной учетной записи хранения разработки, а затем передает новый контекст командлету **Get-AzStorageContainer** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d8670-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d8670-132">Команда получает контейнер хранилища Azure для локальной учетной записи хранилища разработчика.</span><span class="sxs-lookup"><span data-stu-id="d8670-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="d8670-133">Пример 6: получение нескольких контейнеров</span><span class="sxs-lookup"><span data-stu-id="d8670-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="d8670-134">Первая команда создает контекст с помощью локальной учетной записи хранения разработки и сохраняет этот контекст в переменной $Context 01.</span><span class="sxs-lookup"><span data-stu-id="d8670-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="d8670-135">Вторая команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ, и сохраняет этот контекст в переменной $Context 02.</span><span class="sxs-lookup"><span data-stu-id="d8670-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="d8670-136">Последняя команда получает контейнеры для контекстов, которые хранятся в $Context 01 и $Context 02 с помощью **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="d8670-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="d8670-137">Пример 7: создание контекста с конечной точкой</span><span class="sxs-lookup"><span data-stu-id="d8670-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="d8670-138">Эта команда создает контекст хранилища Azure, который содержит указанную конечную точку хранилища.</span><span class="sxs-lookup"><span data-stu-id="d8670-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="d8670-139">Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="d8670-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d8670-140">Пример 8: создание контекста с указанной средой</span><span class="sxs-lookup"><span data-stu-id="d8670-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="d8670-141">Эта команда создает контекст хранилища Azure, который содержит указанную среду Azure.</span><span class="sxs-lookup"><span data-stu-id="d8670-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="d8670-142">Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="d8670-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d8670-143">Пример 9: создание контекста с помощью маркера SAS</span><span class="sxs-lookup"><span data-stu-id="d8670-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="d8670-144">Первая команда создает маркер SAS с помощью командлета **New-AzStorageContainerSASToken** для контейнера с именем ContosoMain и сохраняет этот маркер в переменной $SasToken.</span><span class="sxs-lookup"><span data-stu-id="d8670-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="d8670-145">Этот маркер предназначен для чтения, добавления, обновления и удаления разрешений.</span><span class="sxs-lookup"><span data-stu-id="d8670-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="d8670-146">Вторая команда создает контекст для учетной записи с именем ContosoGeneral, который использует маркер SAS, хранящийся в $SasToken, и сохраняет этот контекст в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="d8670-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="d8670-147">В последней команде перечисляются все BLOB-объекты, связанные с контейнером с именем ContosoMain, используя контекст, хранящийся в $Context.</span><span class="sxs-lookup"><span data-stu-id="d8670-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="d8670-148">Пример 10: создание контекста с использованием проверки подлинности OAuth</span><span class="sxs-lookup"><span data-stu-id="d8670-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="d8670-149">Эта команда создает контекст с использованием проверки подлинности OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="d8670-149">This command creates a context by using the OAuth (Azure AD)  Authentication.</span></span>

## <span data-ttu-id="d8670-150">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8670-150">PARAMETERS</span></span>

### <span data-ttu-id="d8670-151">-Анонимный</span><span class="sxs-lookup"><span data-stu-id="d8670-151">-Anonymous</span></span>
<span data-ttu-id="d8670-152">Указывает на то, что этот командлет создает контекст хранилища Azure для анонимного входа.</span><span class="sxs-lookup"><span data-stu-id="d8670-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="d8670-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d8670-153">-ConnectionString</span></span>
<span data-ttu-id="d8670-154">Указывает строку подключения для контекста хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d8670-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="d8670-155">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d8670-155">-Endpoint</span></span>
<span data-ttu-id="d8670-156">Задает конечную точку контекста хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d8670-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="d8670-157">-Environment</span><span class="sxs-lookup"><span data-stu-id="d8670-157">-Environment</span></span>
<span data-ttu-id="d8670-158">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="d8670-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="d8670-159">Допустимые значения этого параметра: AzureCloud и AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="d8670-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="d8670-160">Для получения дополнительных сведений введите `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="d8670-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="d8670-161">-Local</span><span class="sxs-lookup"><span data-stu-id="d8670-161">-Local</span></span>
<span data-ttu-id="d8670-162">Указывает на то, что этот командлет создает контекст с помощью локальной учетной записи хранения разработки.</span><span class="sxs-lookup"><span data-stu-id="d8670-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="d8670-163">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="d8670-163">-Protocol</span></span>
<span data-ttu-id="d8670-164">Протокол передачи (HTTPS/HTTP).</span><span class="sxs-lookup"><span data-stu-id="d8670-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="d8670-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="d8670-165">-SasToken</span></span>
<span data-ttu-id="d8670-166">Указывает маркер общего доступа к подписи (SAS) для контекста.</span><span class="sxs-lookup"><span data-stu-id="d8670-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="d8670-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d8670-167">-StorageAccountKey</span></span>
<span data-ttu-id="d8670-168">Указывает ключ учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8670-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="d8670-169">Этот командлет создает контекст для ключа, указывающего на этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d8670-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8670-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8670-170">-StorageAccountName</span></span>
<span data-ttu-id="d8670-171">Указывает имя учетной записи службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d8670-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="d8670-172">Этот командлет создает контекст для учетной записи, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d8670-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8670-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="d8670-173">-UseConnectedAccount</span></span>
<span data-ttu-id="d8670-174">Указывает на то, что этот командлет создает контекст хранилища Azure с проверкой подлинности OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="d8670-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="d8670-175">Этот командлет использует проверку подлинности OAuth по умолчанию, если не указана другая проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="d8670-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

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

### <span data-ttu-id="d8670-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8670-176">CommonParameters</span></span>
<span data-ttu-id="d8670-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8670-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8670-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8670-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8670-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8670-179">INPUTS</span></span>

### <span data-ttu-id="d8670-180">System. String</span><span class="sxs-lookup"><span data-stu-id="d8670-180">System.String</span></span>

## <span data-ttu-id="d8670-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8670-181">OUTPUTS</span></span>

### <span data-ttu-id="d8670-182">Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8670-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="d8670-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8670-183">NOTES</span></span>

## <span data-ttu-id="d8670-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8670-184">RELATED LINKS</span></span>

[<span data-ttu-id="d8670-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d8670-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="d8670-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d8670-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


