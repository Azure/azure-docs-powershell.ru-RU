---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556223"
---
# <span data-ttu-id="fa5ce-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="fa5ce-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="fa5ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5ce-103">Создание маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-103">Creates an SAS token.</span></span>

## <span data-ttu-id="fa5ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa5ce-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa5ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa5ce-105">DESCRIPTION</span></span>
<span data-ttu-id="fa5ce-106">Командлет **New-AzureStorageSASToken** создает маркер подписи общего доступа (SAS) для учетной записи хранения Azure на уровне учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="fa5ce-107">Вы можете использовать маркер SAS для делегирования разрешений для нескольких служб или делегирования разрешений для служб, недоступных с маркером SAS уровня объекта.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="fa5ce-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa5ce-108">EXAMPLES</span></span>

### <span data-ttu-id="fa5ce-109">Пример 1: создание маркера SAS</span><span class="sxs-lookup"><span data-stu-id="fa5ce-109">Example 1: Create an SAS token</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="fa5ce-110">Эта команда создает маркер SAS уровня учетной записи с полным разрешением.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="fa5ce-111">Пример 2: создание маркера SAS для диапазона IP-адресов</span><span class="sxs-lookup"><span data-stu-id="fa5ce-111">Example 2: Create an SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="fa5ce-112">Эта команда создает маркер SAS для запросов только HTTPS из указанного диапазона IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-112">This command creates an SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="fa5ce-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa5ce-113">PARAMETERS</span></span>

### <span data-ttu-id="fa5ce-114">-Context</span><span class="sxs-lookup"><span data-stu-id="fa5ce-114">-Context</span></span>
<span data-ttu-id="fa5ce-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="fa5ce-116">Вы можете использовать командлет New-AzureStorageContext, чтобы получить объект **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="fa5ce-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="fa5ce-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fa5ce-117">-ExpiryTime</span></span>
<span data-ttu-id="fa5ce-118">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="fa5ce-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="fa5ce-119">-IPAddressOrRange</span></span>
<span data-ttu-id="fa5ce-120">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="fa5ce-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="fa5ce-121">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="fa5ce-122">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="fa5ce-122">-Permission</span></span>
<span data-ttu-id="fa5ce-123">Задает разрешения для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="fa5ce-124">Разрешения действительны только в том случае, если они соответствуют указанному типу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="fa5ce-125">Дополнительные сведения о допустимых значениях разрешений можно найти в разделе Создание SAS для учетной записиhttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="fa5ce-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="fa5ce-126">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="fa5ce-126">-Protocol</span></span>
<span data-ttu-id="fa5ce-127">Указывает протокол, разрешенный для запроса, созданного с помощью сопоставлений безопасности учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="fa5ce-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa5ce-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa5ce-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="fa5ce-129">HttpsOnly</span></span>
- <span data-ttu-id="fa5ce-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="fa5ce-130">HttpsOrHttp</span></span>

<span data-ttu-id="fa5ce-131">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="fa5ce-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fa5ce-132">-ResourceType</span></span>
<span data-ttu-id="fa5ce-133">Указывает типы ресурсов, доступные в токене SAS.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="fa5ce-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa5ce-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa5ce-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="fa5ce-135">None</span></span>
- <span data-ttu-id="fa5ce-136">Сервиса</span><span class="sxs-lookup"><span data-stu-id="fa5ce-136">Service</span></span>
- <span data-ttu-id="fa5ce-137">Контейнер</span><span class="sxs-lookup"><span data-stu-id="fa5ce-137">Container</span></span>
- <span data-ttu-id="fa5ce-138">DataObject</span><span class="sxs-lookup"><span data-stu-id="fa5ce-138">Object</span></span>

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

### <span data-ttu-id="fa5ce-139">-Служба</span><span class="sxs-lookup"><span data-stu-id="fa5ce-139">-Service</span></span>
<span data-ttu-id="fa5ce-140">Указывает службу.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-140">Specifies the service.</span></span>
<span data-ttu-id="fa5ce-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa5ce-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa5ce-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="fa5ce-142">None</span></span>
- <span data-ttu-id="fa5ce-143">Большом</span><span class="sxs-lookup"><span data-stu-id="fa5ce-143">Blob</span></span>
- <span data-ttu-id="fa5ce-144">Файл</span><span class="sxs-lookup"><span data-stu-id="fa5ce-144">File</span></span>
- <span data-ttu-id="fa5ce-145">Поместить</span><span class="sxs-lookup"><span data-stu-id="fa5ce-145">Queue</span></span>
- <span data-ttu-id="fa5ce-146">Таблич</span><span class="sxs-lookup"><span data-stu-id="fa5ce-146">Table</span></span>

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

### <span data-ttu-id="fa5ce-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fa5ce-147">-StartTime</span></span>
<span data-ttu-id="fa5ce-148">Указывает время в виде объекта **DateTime** , в котором SA становится действительной.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="fa5ce-149">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="fa5ce-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5ce-150">CommonParameters</span></span>
<span data-ttu-id="fa5ce-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5ce-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa5ce-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5ce-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa5ce-153">INPUTS</span></span>

## <span data-ttu-id="fa5ce-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa5ce-154">OUTPUTS</span></span>

## <span data-ttu-id="fa5ce-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa5ce-155">NOTES</span></span>

## <span data-ttu-id="fa5ce-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa5ce-156">RELATED LINKS</span></span>

[<span data-ttu-id="fa5ce-157">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fa5ce-157">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="fa5ce-158">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="fa5ce-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="fa5ce-159">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="fa5ce-159">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="fa5ce-160">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="fa5ce-160">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="fa5ce-161">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="fa5ce-161">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="fa5ce-162">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="fa5ce-162">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


