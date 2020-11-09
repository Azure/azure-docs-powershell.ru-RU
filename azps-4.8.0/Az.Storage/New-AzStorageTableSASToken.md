---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243788"
---
# <span data-ttu-id="31fed-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="31fed-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="31fed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31fed-102">SYNOPSIS</span></span>
<span data-ttu-id="31fed-103">Создание маркера SAS для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="31fed-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="31fed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31fed-104">SYNTAX</span></span>

### <span data-ttu-id="31fed-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="31fed-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31fed-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="31fed-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31fed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31fed-107">DESCRIPTION</span></span>
<span data-ttu-id="31fed-108">Командлет **New-AzStorageTableSASToken** создает маркер подписи общего доступа (SAS) для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="31fed-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="31fed-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31fed-109">EXAMPLES</span></span>

### <span data-ttu-id="31fed-110">Пример 1: создание маркера SAS с полными разрешениями для таблицы</span><span class="sxs-lookup"><span data-stu-id="31fed-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="31fed-111">Эта команда создает маркер SAS с полными разрешениями для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="31fed-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="31fed-112">Этот маркер предназначен для чтения, добавления, обновления и удаления разрешений.</span><span class="sxs-lookup"><span data-stu-id="31fed-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="31fed-113">Пример 2: создание маркера SAS для диапазона разделов</span><span class="sxs-lookup"><span data-stu-id="31fed-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="31fed-114">Эта команда генерирует и маркер SAS с полными разрешениями для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="31fed-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="31fed-115">Команда ограничивает маркер диапазоном, указанным в параметрах *StartPartitionKey* и *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="31fed-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="31fed-116">Пример 3: создание маркера SAS с политикой хранения с сохранением доступа к таблице</span><span class="sxs-lookup"><span data-stu-id="31fed-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="31fed-117">Эта команда создает маркер SAS для таблицы с именем ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="31fed-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="31fed-118">Команда задает политику сохранения для доступа с именем ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="31fed-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="31fed-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31fed-119">PARAMETERS</span></span>

### <span data-ttu-id="31fed-120">-Context</span><span class="sxs-lookup"><span data-stu-id="31fed-120">-Context</span></span>
<span data-ttu-id="31fed-121">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="31fed-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="31fed-122">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="31fed-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="31fed-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31fed-123">-DefaultProfile</span></span>
<span data-ttu-id="31fed-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31fed-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31fed-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="31fed-125">-EndPartitionKey</span></span>
<span data-ttu-id="31fed-126">Задает ключ секции конца диапазона для маркера, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="31fed-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="31fed-127">-EndRowKey</span></span>
<span data-ttu-id="31fed-128">Задает ключ строки для конца диапазона для маркера, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="31fed-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="31fed-129">-ExpiryTime</span></span>
<span data-ttu-id="31fed-130">Указывает, когда истекает срок действия маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="31fed-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="31fed-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="31fed-131">-FullUri</span></span>
<span data-ttu-id="31fed-132">Указывает на то, что этот командлет возвращает URI всей очереди с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="31fed-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="31fed-133">-IPAddressOrRange</span></span>
<span data-ttu-id="31fed-134">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="31fed-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="31fed-135">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="31fed-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="31fed-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31fed-136">-Name</span></span>
<span data-ttu-id="31fed-137">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="31fed-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="31fed-138">Этот командлет создает маркер SAS для таблицы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="31fed-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-139">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="31fed-139">-Permission</span></span>
<span data-ttu-id="31fed-140">Задает разрешения для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="31fed-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="31fed-141">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="31fed-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-142">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="31fed-142">-Policy</span></span>
<span data-ttu-id="31fed-143">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="31fed-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-144">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="31fed-144">-Protocol</span></span>
<span data-ttu-id="31fed-145">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="31fed-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="31fed-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31fed-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="31fed-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="31fed-147">HttpsOnly</span></span>
* <span data-ttu-id="31fed-148">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="31fed-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="31fed-149">-StartPartitionKey</span></span>
<span data-ttu-id="31fed-150">Задает ключ раздела для начала диапазона для маркера, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="31fed-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="31fed-151">-StartRowKey</span></span>
<span data-ttu-id="31fed-152">Задает ключ строки для начала диапазона для маркера, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="31fed-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fed-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="31fed-153">-StartTime</span></span>
<span data-ttu-id="31fed-154">Указывает, когда токен SAS становится действительным.</span><span class="sxs-lookup"><span data-stu-id="31fed-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="31fed-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31fed-155">CommonParameters</span></span>
<span data-ttu-id="31fed-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31fed-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31fed-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31fed-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31fed-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31fed-158">INPUTS</span></span>

### <span data-ttu-id="31fed-159">System. String</span><span class="sxs-lookup"><span data-stu-id="31fed-159">System.String</span></span>

### <span data-ttu-id="31fed-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="31fed-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="31fed-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31fed-161">OUTPUTS</span></span>

### <span data-ttu-id="31fed-162">System. String</span><span class="sxs-lookup"><span data-stu-id="31fed-162">System.String</span></span>

## <span data-ttu-id="31fed-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="31fed-163">NOTES</span></span>

## <span data-ttu-id="31fed-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31fed-164">RELATED LINKS</span></span>

[<span data-ttu-id="31fed-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="31fed-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)