---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: 8b0eb67808bf4148d93006b24273d55b737adfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566027"
---
# <span data-ttu-id="cc8b0-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="cc8b0-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="cc8b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="cc8b0-103">Создание маркера SAS на уровне учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc8b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc8b0-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc8b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc8b0-105">DESCRIPTION</span></span>
<span data-ttu-id="cc8b0-106">Командлет **New-AzureStorageSASToken** создает маркер подписи общего доступа (SAS) для учетной записи хранения Azure на уровне учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="cc8b0-107">Вы можете использовать маркер SAS для делегирования разрешений для нескольких служб или делегирования разрешений для служб, недоступных с маркером SAS уровня объекта.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="cc8b0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc8b0-108">EXAMPLES</span></span>

### <span data-ttu-id="cc8b0-109">Пример 1: создание маркера SAS уровня учетной записи с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="cc8b0-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="cc8b0-110">Эта команда создает маркер SAS уровня учетной записи с полным разрешением.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="cc8b0-111">Пример 2: создание маркера SAS уровня учетной записи для диапазона IP-адресов</span><span class="sxs-lookup"><span data-stu-id="cc8b0-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="cc8b0-112">Эта команда создает маркер SAS уровня учетной записи для запросов HTTPS с указанным диапазоном IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="cc8b0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc8b0-113">PARAMETERS</span></span>

### <span data-ttu-id="cc8b0-114">-Context</span><span class="sxs-lookup"><span data-stu-id="cc8b0-114">-Context</span></span>
<span data-ttu-id="cc8b0-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cc8b0-116">Вы можете использовать командлет New-AzureStorageContext, чтобы получить объект **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="cc8b0-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="cc8b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc8b0-117">-DefaultProfile</span></span>
<span data-ttu-id="cc8b0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8b0-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cc8b0-119">-ExpiryTime</span></span>
<span data-ttu-id="cc8b0-120">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="cc8b0-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cc8b0-121">-IPAddressOrRange</span></span>
<span data-ttu-id="cc8b0-122">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="cc8b0-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="cc8b0-123">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="cc8b0-124">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="cc8b0-124">-Permission</span></span>
<span data-ttu-id="cc8b0-125">Задает разрешения для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="cc8b0-126">Разрешения действительны только в том случае, если они соответствуют указанному типу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="cc8b0-127">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="cc8b0-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="cc8b0-128">Дополнительные сведения о допустимых значениях разрешений можно найти в разделе Создание SAS для учетной записи https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="cc8b0-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="cc8b0-129">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="cc8b0-129">-Protocol</span></span>
<span data-ttu-id="cc8b0-130">Указывает протокол, разрешенный для запроса, созданного с помощью сопоставлений безопасности учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="cc8b0-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cc8b0-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc8b0-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="cc8b0-132">HttpsOnly</span></span>
- <span data-ttu-id="cc8b0-133">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8b0-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cc8b0-134">-ResourceType</span></span>
<span data-ttu-id="cc8b0-135">Указывает типы ресурсов, доступные в токене SAS.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="cc8b0-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cc8b0-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc8b0-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="cc8b0-137">None</span></span>
- <span data-ttu-id="cc8b0-138">Сервиса</span><span class="sxs-lookup"><span data-stu-id="cc8b0-138">Service</span></span>
- <span data-ttu-id="cc8b0-139">Контейнер</span><span class="sxs-lookup"><span data-stu-id="cc8b0-139">Container</span></span>
- <span data-ttu-id="cc8b0-140">DataObject</span><span class="sxs-lookup"><span data-stu-id="cc8b0-140">Object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8b0-141">-Служба</span><span class="sxs-lookup"><span data-stu-id="cc8b0-141">-Service</span></span>
<span data-ttu-id="cc8b0-142">Указывает службу.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-142">Specifies the service.</span></span>
<span data-ttu-id="cc8b0-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cc8b0-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc8b0-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="cc8b0-144">None</span></span>
- <span data-ttu-id="cc8b0-145">Большом</span><span class="sxs-lookup"><span data-stu-id="cc8b0-145">Blob</span></span>
- <span data-ttu-id="cc8b0-146">Файл</span><span class="sxs-lookup"><span data-stu-id="cc8b0-146">File</span></span>
- <span data-ttu-id="cc8b0-147">Поместить</span><span class="sxs-lookup"><span data-stu-id="cc8b0-147">Queue</span></span>
- <span data-ttu-id="cc8b0-148">Таблич</span><span class="sxs-lookup"><span data-stu-id="cc8b0-148">Table</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8b0-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cc8b0-149">-StartTime</span></span>
<span data-ttu-id="cc8b0-150">Указывает время в виде объекта **DateTime** , в котором SA становится действительной.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="cc8b0-151">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="cc8b0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc8b0-152">CommonParameters</span></span>
<span data-ttu-id="cc8b0-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc8b0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc8b0-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc8b0-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc8b0-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc8b0-155">INPUTS</span></span>

### <span data-ttu-id="cc8b0-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc8b0-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cc8b0-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc8b0-157">OUTPUTS</span></span>

### <span data-ttu-id="cc8b0-158">System. String</span><span class="sxs-lookup"><span data-stu-id="cc8b0-158">System.String</span></span>

## <span data-ttu-id="cc8b0-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc8b0-159">NOTES</span></span>

## <span data-ttu-id="cc8b0-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc8b0-160">RELATED LINKS</span></span>

[<span data-ttu-id="cc8b0-161">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cc8b0-161">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="cc8b0-162">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cc8b0-162">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="cc8b0-163">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="cc8b0-163">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="cc8b0-164">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="cc8b0-164">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="cc8b0-165">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="cc8b0-165">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="cc8b0-166">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="cc8b0-166">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


