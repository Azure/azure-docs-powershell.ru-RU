---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8b280a13e7eb7a2e6ea3f52b4a121f313504b2ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558083"
---
# <span data-ttu-id="5c655-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="5c655-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="5c655-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c655-102">SYNOPSIS</span></span>
<span data-ttu-id="5c655-103">Создание маркера SAS на уровне учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5c655-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c655-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c655-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c655-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c655-105">DESCRIPTION</span></span>
<span data-ttu-id="5c655-106">Командлет **New-AzureStorageSASToken** создает маркер подписи общего доступа (SAS) для учетной записи хранения Azure на уровне учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5c655-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="5c655-107">Вы можете использовать маркер SAS для делегирования разрешений для нескольких служб или делегирования разрешений для служб, недоступных с маркером SAS уровня объекта.</span><span class="sxs-lookup"><span data-stu-id="5c655-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="5c655-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c655-108">EXAMPLES</span></span>

### <span data-ttu-id="5c655-109">Пример 1: создание маркера SAS уровня учетной записи с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="5c655-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="5c655-110">Эта команда создает маркер SAS уровня учетной записи с полным разрешением.</span><span class="sxs-lookup"><span data-stu-id="5c655-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="5c655-111">Пример 2: создание маркера SAS уровня учетной записи для диапазона IP-адресов</span><span class="sxs-lookup"><span data-stu-id="5c655-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="5c655-112">Эта команда создает маркер SAS уровня учетной записи для запросов HTTPS с указанным диапазоном IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="5c655-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="5c655-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c655-113">PARAMETERS</span></span>

### <span data-ttu-id="5c655-114">-Context</span><span class="sxs-lookup"><span data-stu-id="5c655-114">-Context</span></span>
<span data-ttu-id="5c655-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c655-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5c655-116">Вы можете использовать командлет New-AzureStorageContext, чтобы получить объект **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="5c655-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="5c655-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5c655-117">-ExpiryTime</span></span>
<span data-ttu-id="5c655-118">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="5c655-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="5c655-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5c655-119">-IPAddressOrRange</span></span>
<span data-ttu-id="5c655-120">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="5c655-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5c655-121">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="5c655-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="5c655-122">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="5c655-122">-Permission</span></span>
<span data-ttu-id="5c655-123">Задает разрешения для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5c655-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="5c655-124">Разрешения действительны только в том случае, если они соответствуют указанному типу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c655-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="5c655-125">Дополнительные сведения о допустимых значениях разрешений можно найти в разделе Создание SAS для учетной записиhttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="5c655-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="5c655-126">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="5c655-126">-Protocol</span></span>
<span data-ttu-id="5c655-127">Указывает протокол, разрешенный для запроса, созданного с помощью сопоставлений безопасности учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5c655-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="5c655-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5c655-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c655-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5c655-129">HttpsOnly</span></span>
- <span data-ttu-id="5c655-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="5c655-130">HttpsOrHttp</span></span>

<span data-ttu-id="5c655-131">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="5c655-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="5c655-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5c655-132">-ResourceType</span></span>
<span data-ttu-id="5c655-133">Указывает типы ресурсов, доступные в токене SAS.</span><span class="sxs-lookup"><span data-stu-id="5c655-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="5c655-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5c655-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c655-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="5c655-135">None</span></span>
- <span data-ttu-id="5c655-136">Сервиса</span><span class="sxs-lookup"><span data-stu-id="5c655-136">Service</span></span>
- <span data-ttu-id="5c655-137">Контейнер</span><span class="sxs-lookup"><span data-stu-id="5c655-137">Container</span></span>
- <span data-ttu-id="5c655-138">DataObject</span><span class="sxs-lookup"><span data-stu-id="5c655-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c655-139">-Служба</span><span class="sxs-lookup"><span data-stu-id="5c655-139">-Service</span></span>
<span data-ttu-id="5c655-140">Указывает службу.</span><span class="sxs-lookup"><span data-stu-id="5c655-140">Specifies the service.</span></span>
<span data-ttu-id="5c655-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5c655-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c655-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="5c655-142">None</span></span>
- <span data-ttu-id="5c655-143">Большом</span><span class="sxs-lookup"><span data-stu-id="5c655-143">Blob</span></span>
- <span data-ttu-id="5c655-144">Файл</span><span class="sxs-lookup"><span data-stu-id="5c655-144">File</span></span>
- <span data-ttu-id="5c655-145">Поместить</span><span class="sxs-lookup"><span data-stu-id="5c655-145">Queue</span></span>
- <span data-ttu-id="5c655-146">Таблич</span><span class="sxs-lookup"><span data-stu-id="5c655-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c655-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5c655-147">-StartTime</span></span>
<span data-ttu-id="5c655-148">Указывает время в виде объекта **DateTime** , в котором SA становится действительной.</span><span class="sxs-lookup"><span data-stu-id="5c655-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="5c655-149">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="5c655-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="5c655-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c655-150">CommonParameters</span></span>
<span data-ttu-id="5c655-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c655-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c655-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c655-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c655-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c655-153">INPUTS</span></span>

### <span data-ttu-id="5c655-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c655-154">IStorageContext</span></span>

<span data-ttu-id="5c655-155">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5c655-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="5c655-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c655-156">OUTPUTS</span></span>

### <span data-ttu-id="5c655-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5c655-157">System.String</span></span>

## <span data-ttu-id="5c655-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c655-158">NOTES</span></span>

## <span data-ttu-id="5c655-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c655-159">RELATED LINKS</span></span>

[<span data-ttu-id="5c655-160">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5c655-160">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="5c655-161">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5c655-161">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="5c655-162">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="5c655-162">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="5c655-163">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="5c655-163">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="5c655-164">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="5c655-164">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="5c655-165">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="5c655-165">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


