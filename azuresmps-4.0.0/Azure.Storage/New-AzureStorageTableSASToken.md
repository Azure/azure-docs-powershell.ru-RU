---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556420"
---
# <span data-ttu-id="605a2-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="605a2-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="605a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="605a2-102">SYNOPSIS</span></span>
<span data-ttu-id="605a2-103">Создание маркера SAS для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="605a2-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="605a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="605a2-104">SYNTAX</span></span>

### <span data-ttu-id="605a2-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="605a2-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="605a2-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="605a2-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="605a2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="605a2-107">DESCRIPTION</span></span>
<span data-ttu-id="605a2-108">Командлет **New-AzureStorageTableSASToken** создает маркер подписи общего доступа (SAS) для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="605a2-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="605a2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="605a2-109">EXAMPLES</span></span>

### <span data-ttu-id="605a2-110">Пример 1: создание маркера SAS с полными разрешениями для таблицы</span><span class="sxs-lookup"><span data-stu-id="605a2-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="605a2-111">Эта команда создает маркер SAS с полными разрешениями для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="605a2-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="605a2-112">Этот маркер предназначен для чтения, добавления, обновления и удаления разрешений.</span><span class="sxs-lookup"><span data-stu-id="605a2-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="605a2-113">Пример 2: создание маркера SAS для диапазона разделов</span><span class="sxs-lookup"><span data-stu-id="605a2-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="605a2-114">Эта команда генерирует и маркер SAS с полными разрешениями для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="605a2-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="605a2-115">Команда ограничивает маркер диапазоном, указанным в параметрах *StartPartitionKey* и *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="605a2-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="605a2-116">Пример 3: создание маркера SAS с политикой хранения с сохранением доступа к таблице</span><span class="sxs-lookup"><span data-stu-id="605a2-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="605a2-117">Эта команда создает маркер SAS для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="605a2-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="605a2-118">Команда задает политику сохранения для доступа с именем ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="605a2-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="605a2-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="605a2-119">PARAMETERS</span></span>

### <span data-ttu-id="605a2-120">-Context</span><span class="sxs-lookup"><span data-stu-id="605a2-120">-Context</span></span>
<span data-ttu-id="605a2-121">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="605a2-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="605a2-122">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="605a2-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="605a2-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="605a2-123">-EndPartitionKey</span></span>
<span data-ttu-id="605a2-124">Задает ключ секции конца диапазона для маркера, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="605a2-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="605a2-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="605a2-125">-EndRowKey</span></span>
<span data-ttu-id="605a2-126">Задает ключ строки для конца диапазона для маркера, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="605a2-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="605a2-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="605a2-127">-ExpiryTime</span></span>
<span data-ttu-id="605a2-128">Указывает, когда истекает срок действия маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="605a2-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="605a2-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="605a2-129">-FullUri</span></span>
<span data-ttu-id="605a2-130">Указывает на то, что этот командлет возвращает URI всей очереди с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="605a2-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="605a2-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="605a2-131">-IPAddressOrRange</span></span>
<span data-ttu-id="605a2-132">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="605a2-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="605a2-133">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="605a2-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="605a2-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="605a2-134">-Name</span></span>
<span data-ttu-id="605a2-135">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="605a2-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="605a2-136">Этот командлет создает маркер SAS для таблицы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="605a2-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="605a2-137">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="605a2-137">-Permission</span></span>
<span data-ttu-id="605a2-138">Задает разрешения для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="605a2-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="605a2-139">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="605a2-139">-Policy</span></span>
<span data-ttu-id="605a2-140">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="605a2-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="605a2-141">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="605a2-141">-Protocol</span></span>
<span data-ttu-id="605a2-142">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="605a2-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="605a2-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="605a2-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="605a2-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="605a2-144">HttpsOnly</span></span>
* <span data-ttu-id="605a2-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="605a2-145">HttpsOrHttp</span></span>

<span data-ttu-id="605a2-146">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="605a2-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="605a2-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="605a2-147">-StartPartitionKey</span></span>
<span data-ttu-id="605a2-148">Задает ключ раздела для начала диапазона для маркера, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="605a2-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="605a2-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="605a2-149">-StartRowKey</span></span>
<span data-ttu-id="605a2-150">Задает ключ строки для начала диапазона для маркера, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="605a2-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="605a2-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="605a2-151">-StartTime</span></span>
<span data-ttu-id="605a2-152">Указывает, когда токен SAS становится действительным.</span><span class="sxs-lookup"><span data-stu-id="605a2-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="605a2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605a2-153">CommonParameters</span></span>
<span data-ttu-id="605a2-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="605a2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605a2-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="605a2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605a2-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="605a2-156">INPUTS</span></span>

## <span data-ttu-id="605a2-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="605a2-157">OUTPUTS</span></span>

## <span data-ttu-id="605a2-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="605a2-158">NOTES</span></span>

## <span data-ttu-id="605a2-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="605a2-159">RELATED LINKS</span></span>

[<span data-ttu-id="605a2-160">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="605a2-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
