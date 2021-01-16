---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324858"
---
# <span data-ttu-id="fdd8b-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="fdd8b-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="fdd8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdd8b-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd8b-103">Создает маркер SAS на уровне учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="fdd8b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fdd8b-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdd8b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdd8b-105">DESCRIPTION</span></span>
<span data-ttu-id="fdd8b-106">**Новый-AzStorageSASToken** создает маркер подписи SAS для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="fdd8b-107">С помощью маркера SAS можно делегировать разрешения для нескольких служб или делегировать разрешения для служб, недоступных с маркером SAS на уровне объекта.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="fdd8b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fdd8b-108">EXAMPLES</span></span>

### <span data-ttu-id="fdd8b-109">Пример 1. Создание маркера SAS на уровне учетной записи с полными разрешениями</span><span class="sxs-lookup"><span data-stu-id="fdd8b-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="fdd8b-110">Эта команда создает маркер SAS на уровне учетной записи с полными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="fdd8b-111">Пример 2. Создание маркера SAS на уровне учетной записи для диапазона IP-адресов</span><span class="sxs-lookup"><span data-stu-id="fdd8b-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="fdd8b-112">Эта команда создает маркер SAS на уровне учетной записи для запросов только HTTPS из указанного диапазона IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="fdd8b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdd8b-113">PARAMETERS</span></span>

### <span data-ttu-id="fdd8b-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="fdd8b-114">-Context</span></span>
<span data-ttu-id="fdd8b-115">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="fdd8b-116">С помощью New-AzStorageContext можно получить объект **AzureStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="fdd8b-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="fdd8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd8b-117">-DefaultProfile</span></span>
<span data-ttu-id="fdd8b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdd8b-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fdd8b-119">-ExpiryTime</span></span>
<span data-ttu-id="fdd8b-120">Время, в течение которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="fdd8b-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="fdd8b-121">-IPAddressOrRange</span></span>
<span data-ttu-id="fdd8b-122">Указывает IP-адрес или диапазон IP-адресов, с которых нужно принимать запросы, например 168.1.5.65 или 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="fdd8b-123">Диапазон включительно.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="fdd8b-124">-Permission</span><span class="sxs-lookup"><span data-stu-id="fdd8b-124">-Permission</span></span>
<span data-ttu-id="fdd8b-125">Определяет разрешения для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="fdd8b-126">Разрешения действительны только в том случае, если они соответствуют указанному типу ресурса.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="fdd8b-127">Важно отметить, что это строка (для `rwd` чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="fdd8b-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="fdd8b-128">Дополнительные сведения о допустимых значениях разрешений см. в теме "Создание SAS учетной записи" http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="fdd8b-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="fdd8b-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="fdd8b-129">-Protocol</span></span>
<span data-ttu-id="fdd8b-130">Определяет протокол, допустимый для запроса, выполненного с учетной записью SAS.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="fdd8b-131">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="fdd8b-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fdd8b-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="fdd8b-132">HttpsOnly</span></span>
- <span data-ttu-id="fdd8b-133">По умолчанию httpsOrHttp имеет значение httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="fdd8b-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fdd8b-134">-ResourceType</span></span>
<span data-ttu-id="fdd8b-135">Определяет типы ресурсов, доступные с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="fdd8b-136">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="fdd8b-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fdd8b-137">Нет</span><span class="sxs-lookup"><span data-stu-id="fdd8b-137">None</span></span>
- <span data-ttu-id="fdd8b-138">Служба</span><span class="sxs-lookup"><span data-stu-id="fdd8b-138">Service</span></span>
- <span data-ttu-id="fdd8b-139">Контейнер</span><span class="sxs-lookup"><span data-stu-id="fdd8b-139">Container</span></span>
- <span data-ttu-id="fdd8b-140">Объект</span><span class="sxs-lookup"><span data-stu-id="fdd8b-140">Object</span></span>

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

### <span data-ttu-id="fdd8b-141">-Service</span><span class="sxs-lookup"><span data-stu-id="fdd8b-141">-Service</span></span>
<span data-ttu-id="fdd8b-142">Указывает службу.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-142">Specifies the service.</span></span>
<span data-ttu-id="fdd8b-143">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="fdd8b-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fdd8b-144">Нет</span><span class="sxs-lookup"><span data-stu-id="fdd8b-144">None</span></span>
- <span data-ttu-id="fdd8b-145">BLOB</span><span class="sxs-lookup"><span data-stu-id="fdd8b-145">Blob</span></span>
- <span data-ttu-id="fdd8b-146">Файл</span><span class="sxs-lookup"><span data-stu-id="fdd8b-146">File</span></span>
- <span data-ttu-id="fdd8b-147">Очередь</span><span class="sxs-lookup"><span data-stu-id="fdd8b-147">Queue</span></span>
- <span data-ttu-id="fdd8b-148">Таблица</span><span class="sxs-lookup"><span data-stu-id="fdd8b-148">Table</span></span>

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

### <span data-ttu-id="fdd8b-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fdd8b-149">-StartTime</span></span>
<span data-ttu-id="fdd8b-150">Время в качестве объекта **даты и времени,** при котором SAS становится допустимым.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="fdd8b-151">Чтобы получить объект **даты и времени,** воспользуйтесь Get-Date.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="fdd8b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd8b-152">CommonParameters</span></span>
<span data-ttu-id="fdd8b-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd8b-154">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd8b-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd8b-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdd8b-155">INPUTS</span></span>

### <span data-ttu-id="fdd8b-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fdd8b-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fdd8b-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fdd8b-157">OUTPUTS</span></span>

### <span data-ttu-id="fdd8b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="fdd8b-158">System.String</span></span>

## <span data-ttu-id="fdd8b-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fdd8b-159">NOTES</span></span>

## <span data-ttu-id="fdd8b-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fdd8b-160">RELATED LINKS</span></span>

[<span data-ttu-id="fdd8b-161">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fdd8b-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="fdd8b-162">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="fdd8b-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="fdd8b-163">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="fdd8b-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="fdd8b-164">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="fdd8b-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="fdd8b-165">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="fdd8b-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="fdd8b-166">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="fdd8b-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


