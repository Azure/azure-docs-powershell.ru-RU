---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 83480321e58d4dbd21d0a13dd6139c2f2d905c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907262"
---
# <span data-ttu-id="49f42-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="49f42-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="49f42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49f42-102">SYNOPSIS</span></span>
<span data-ttu-id="49f42-103">Создание маркера SAS на уровне учетной записи.</span><span class="sxs-lookup"><span data-stu-id="49f42-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="49f42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49f42-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49f42-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49f42-105">DESCRIPTION</span></span>
<span data-ttu-id="49f42-106">Командлет **New-AzStorageSASToken** создает маркер подписи общего доступа (SAS) для учетной записи хранения Azure на уровне учетной записи.</span><span class="sxs-lookup"><span data-stu-id="49f42-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="49f42-107">Вы можете использовать маркер SAS для делегирования разрешений для нескольких служб или делегирования разрешений для служб, недоступных с маркером SAS уровня объекта.</span><span class="sxs-lookup"><span data-stu-id="49f42-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="49f42-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49f42-108">EXAMPLES</span></span>

### <span data-ttu-id="49f42-109">Пример 1: создание маркера SAS уровня учетной записи с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="49f42-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="49f42-110">Эта команда создает маркер SAS уровня учетной записи с полным разрешением.</span><span class="sxs-lookup"><span data-stu-id="49f42-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="49f42-111">Пример 2: создание маркера SAS уровня учетной записи для диапазона IP-адресов</span><span class="sxs-lookup"><span data-stu-id="49f42-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="49f42-112">Эта команда создает маркер SAS уровня учетной записи для запросов HTTPS с указанным диапазоном IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="49f42-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="49f42-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49f42-113">PARAMETERS</span></span>

### <span data-ttu-id="49f42-114">-Context</span><span class="sxs-lookup"><span data-stu-id="49f42-114">-Context</span></span>
<span data-ttu-id="49f42-115">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="49f42-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="49f42-116">Вы можете использовать командлет New-AzStorageContext, чтобы получить объект **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="49f42-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="49f42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f42-117">-DefaultProfile</span></span>
<span data-ttu-id="49f42-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49f42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f42-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="49f42-119">-ExpiryTime</span></span>
<span data-ttu-id="49f42-120">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="49f42-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="49f42-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="49f42-121">-IPAddressOrRange</span></span>
<span data-ttu-id="49f42-122">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="49f42-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="49f42-123">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="49f42-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="49f42-124">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="49f42-124">-Permission</span></span>
<span data-ttu-id="49f42-125">Задает разрешения для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="49f42-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="49f42-126">Разрешения действительны только в том случае, если они соответствуют указанному типу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49f42-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="49f42-127">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="49f42-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="49f42-128">Дополнительные сведения о допустимых значениях разрешений можно найти в разделе Создание SAS для учетной записи https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="49f42-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="49f42-129">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="49f42-129">-Protocol</span></span>
<span data-ttu-id="49f42-130">Указывает протокол, разрешенный для запроса, созданного с помощью сопоставлений безопасности учетной записи.</span><span class="sxs-lookup"><span data-stu-id="49f42-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="49f42-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="49f42-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49f42-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="49f42-132">HttpsOnly</span></span>
- <span data-ttu-id="49f42-133">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="49f42-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="49f42-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="49f42-134">-ResourceType</span></span>
<span data-ttu-id="49f42-135">Указывает типы ресурсов, доступные в токене SAS.</span><span class="sxs-lookup"><span data-stu-id="49f42-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="49f42-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="49f42-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49f42-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="49f42-137">None</span></span>
- <span data-ttu-id="49f42-138">Сервиса</span><span class="sxs-lookup"><span data-stu-id="49f42-138">Service</span></span>
- <span data-ttu-id="49f42-139">Контейнер</span><span class="sxs-lookup"><span data-stu-id="49f42-139">Container</span></span>
- <span data-ttu-id="49f42-140">DataObject</span><span class="sxs-lookup"><span data-stu-id="49f42-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f42-141">-Служба</span><span class="sxs-lookup"><span data-stu-id="49f42-141">-Service</span></span>
<span data-ttu-id="49f42-142">Указывает службу.</span><span class="sxs-lookup"><span data-stu-id="49f42-142">Specifies the service.</span></span>
<span data-ttu-id="49f42-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="49f42-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49f42-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="49f42-144">None</span></span>
- <span data-ttu-id="49f42-145">Большом</span><span class="sxs-lookup"><span data-stu-id="49f42-145">Blob</span></span>
- <span data-ttu-id="49f42-146">Файл</span><span class="sxs-lookup"><span data-stu-id="49f42-146">File</span></span>
- <span data-ttu-id="49f42-147">Поместить</span><span class="sxs-lookup"><span data-stu-id="49f42-147">Queue</span></span>
- <span data-ttu-id="49f42-148">Таблич</span><span class="sxs-lookup"><span data-stu-id="49f42-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f42-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="49f42-149">-StartTime</span></span>
<span data-ttu-id="49f42-150">Указывает время в виде объекта **DateTime** , в котором SA становится действительной.</span><span class="sxs-lookup"><span data-stu-id="49f42-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="49f42-151">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="49f42-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="49f42-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f42-152">CommonParameters</span></span>
<span data-ttu-id="49f42-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49f42-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f42-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f42-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f42-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49f42-155">INPUTS</span></span>

### <span data-ttu-id="49f42-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="49f42-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="49f42-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49f42-157">OUTPUTS</span></span>

### <span data-ttu-id="49f42-158">System. String</span><span class="sxs-lookup"><span data-stu-id="49f42-158">System.String</span></span>

## <span data-ttu-id="49f42-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="49f42-159">NOTES</span></span>

## <span data-ttu-id="49f42-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49f42-160">RELATED LINKS</span></span>

[<span data-ttu-id="49f42-161">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="49f42-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="49f42-162">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="49f42-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="49f42-163">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="49f42-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="49f42-164">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="49f42-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="49f42-165">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="49f42-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="49f42-166">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="49f42-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


