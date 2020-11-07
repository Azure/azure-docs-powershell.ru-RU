---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 739cd5b12cfc33abb57e4e04d2834b195966b126
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735074"
---
# <span data-ttu-id="5c494-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="5c494-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="5c494-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c494-102">SYNOPSIS</span></span>
<span data-ttu-id="5c494-103">Создание маркера SAS для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c494-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c494-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c494-104">SYNTAX</span></span>

### <span data-ttu-id="5c494-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="5c494-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="5c494-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="5c494-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5c494-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c494-107">DESCRIPTION</span></span>
<span data-ttu-id="5c494-108">Командлет **New-AzureStorageTableSASToken** создает маркер подписи общего доступа (SAS) для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c494-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="5c494-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c494-109">EXAMPLES</span></span>

### <span data-ttu-id="5c494-110">Пример 1: создание маркера SAS с полными разрешениями для таблицы</span><span class="sxs-lookup"><span data-stu-id="5c494-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="5c494-111">Эта команда создает маркер SAS с полными разрешениями для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5c494-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="5c494-112">Этот маркер предназначен для чтения, добавления, обновления и удаления разрешений.</span><span class="sxs-lookup"><span data-stu-id="5c494-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="5c494-113">Пример 2: создание маркера SAS для диапазона разделов</span><span class="sxs-lookup"><span data-stu-id="5c494-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="5c494-114">Эта команда генерирует и маркер SAS с полными разрешениями для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5c494-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="5c494-115">Команда ограничивает маркер диапазоном, указанным в параметрах *StartPartitionKey* и *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="5c494-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="5c494-116">Пример 3: создание маркера SAS с политикой хранения с сохранением доступа к таблице</span><span class="sxs-lookup"><span data-stu-id="5c494-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="5c494-117">Эта команда создает маркер SAS для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5c494-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="5c494-118">Команда задает политику сохранения для доступа с именем ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="5c494-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="5c494-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c494-119">PARAMETERS</span></span>

### <span data-ttu-id="5c494-120">-Context</span><span class="sxs-lookup"><span data-stu-id="5c494-120">-Context</span></span>
<span data-ttu-id="5c494-121">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c494-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5c494-122">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5c494-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5c494-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="5c494-123">-EndPartitionKey</span></span>
<span data-ttu-id="5c494-124">Задает ключ секции конца диапазона для маркера, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5c494-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c494-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="5c494-125">-EndRowKey</span></span>
<span data-ttu-id="5c494-126">Задает ключ строки для конца диапазона для маркера, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5c494-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c494-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5c494-127">-ExpiryTime</span></span>
<span data-ttu-id="5c494-128">Указывает, когда истекает срок действия маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="5c494-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="5c494-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5c494-129">-FullUri</span></span>
<span data-ttu-id="5c494-130">Указывает на то, что этот командлет возвращает URI всей очереди с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="5c494-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c494-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5c494-131">-IPAddressOrRange</span></span>
<span data-ttu-id="5c494-132">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="5c494-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5c494-133">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="5c494-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="5c494-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c494-134">-Name</span></span>
<span data-ttu-id="5c494-135">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c494-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="5c494-136">Этот командлет создает маркер SAS для таблицы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="5c494-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c494-137">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="5c494-137">-Permission</span></span>
<span data-ttu-id="5c494-138">Задает разрешения для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c494-138">Specifies permissions for an Azure Storage table.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c494-139">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="5c494-139">-Policy</span></span>
<span data-ttu-id="5c494-140">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="5c494-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c494-141">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="5c494-141">-Protocol</span></span>
<span data-ttu-id="5c494-142">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="5c494-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5c494-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5c494-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5c494-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5c494-144">HttpsOnly</span></span>
* <span data-ttu-id="5c494-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="5c494-145">HttpsOrHttp</span></span>

<span data-ttu-id="5c494-146">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="5c494-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="5c494-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="5c494-147">-StartPartitionKey</span></span>
<span data-ttu-id="5c494-148">Задает ключ раздела для начала диапазона для маркера, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5c494-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c494-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="5c494-149">-StartRowKey</span></span>
<span data-ttu-id="5c494-150">Задает ключ строки для начала диапазона для маркера, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5c494-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c494-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5c494-151">-StartTime</span></span>
<span data-ttu-id="5c494-152">Указывает, когда токен SAS становится действительным.</span><span class="sxs-lookup"><span data-stu-id="5c494-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="5c494-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c494-153">CommonParameters</span></span>
<span data-ttu-id="5c494-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c494-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c494-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c494-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c494-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c494-156">INPUTS</span></span>

### <span data-ttu-id="5c494-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c494-157">IStorageContext</span></span>

<span data-ttu-id="5c494-158">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5c494-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5c494-159">Подстрок</span><span class="sxs-lookup"><span data-stu-id="5c494-159">String</span></span>

<span data-ttu-id="5c494-160">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5c494-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5c494-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c494-161">OUTPUTS</span></span>

### <span data-ttu-id="5c494-162">System. String</span><span class="sxs-lookup"><span data-stu-id="5c494-162">System.String</span></span>

## <span data-ttu-id="5c494-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c494-163">NOTES</span></span>

## <span data-ttu-id="5c494-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c494-164">RELATED LINKS</span></span>

[<span data-ttu-id="5c494-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c494-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
