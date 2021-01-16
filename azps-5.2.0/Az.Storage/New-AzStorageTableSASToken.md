---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404084"
---
# <span data-ttu-id="2dda7-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="2dda7-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="2dda7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dda7-102">SYNOPSIS</span></span>
<span data-ttu-id="2dda7-103">Создает токен SAS для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2dda7-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="2dda7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2dda7-104">SYNTAX</span></span>

### <span data-ttu-id="2dda7-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="2dda7-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dda7-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="2dda7-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dda7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dda7-107">DESCRIPTION</span></span>
<span data-ttu-id="2dda7-108">Для таблицы хранилища Azure создается маркер подписи SAS **(New-AzStorageTableSASToken).**</span><span class="sxs-lookup"><span data-stu-id="2dda7-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="2dda7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2dda7-109">EXAMPLES</span></span>

### <span data-ttu-id="2dda7-110">Пример 1. Создание маркера SAS с полными разрешениями для таблицы</span><span class="sxs-lookup"><span data-stu-id="2dda7-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="2dda7-111">Эта команда создает маркер SAS с полными разрешениями для таблицы ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="2dda7-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="2dda7-112">Этот маркер для разрешений на чтение, добавление, обновление и удаление.</span><span class="sxs-lookup"><span data-stu-id="2dda7-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="2dda7-113">Пример 2. Создание маркера SAS для диапазона разделов</span><span class="sxs-lookup"><span data-stu-id="2dda7-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="2dda7-114">Эта команда создает маркер SAS с полными разрешениями для таблицы ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="2dda7-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="2dda7-115">Эта команда ограничивает маркер диапазоном, заданным параметрами *StartPartitionKey* и *EndPartitionKey.*</span><span class="sxs-lookup"><span data-stu-id="2dda7-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="2dda7-116">Пример 3. Создание маркера SAS с хранимой политикой доступа для таблицы</span><span class="sxs-lookup"><span data-stu-id="2dda7-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="2dda7-117">Эта команда создает маркер SAS для таблицы ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="2dda7-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="2dda7-118">Команда определяет хранимую политику доступа ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="2dda7-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="2dda7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dda7-119">PARAMETERS</span></span>

### <span data-ttu-id="2dda7-120">-Контекст</span><span class="sxs-lookup"><span data-stu-id="2dda7-120">-Context</span></span>
<span data-ttu-id="2dda7-121">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2dda7-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2dda7-122">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="2dda7-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2dda7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dda7-123">-DefaultProfile</span></span>
<span data-ttu-id="2dda7-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dda7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dda7-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="2dda7-125">-EndPartitionKey</span></span>
<span data-ttu-id="2dda7-126">Определяет ключ раздела в конце диапазона для маркера, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dda7-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2dda7-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="2dda7-127">-EndRowKey</span></span>
<span data-ttu-id="2dda7-128">Определяет ключ строки для конца диапазона для маркера, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dda7-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2dda7-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2dda7-129">-ExpiryTime</span></span>
<span data-ttu-id="2dda7-130">Указывает, когда истекает срок действия токена SAS.</span><span class="sxs-lookup"><span data-stu-id="2dda7-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="2dda7-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="2dda7-131">-FullUri</span></span>
<span data-ttu-id="2dda7-132">Указывает на то, что этот cmdlet возвращает полный URI очереди с маркером SAS.</span><span class="sxs-lookup"><span data-stu-id="2dda7-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="2dda7-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2dda7-133">-IPAddressOrRange</span></span>
<span data-ttu-id="2dda7-134">Указывает IP-адрес или диапазон IP-адресов, с которых нужно принимать запросы, например 168.1.5.65 или 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="2dda7-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="2dda7-135">Диапазон включительно.</span><span class="sxs-lookup"><span data-stu-id="2dda7-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="2dda7-136">-Name</span><span class="sxs-lookup"><span data-stu-id="2dda7-136">-Name</span></span>
<span data-ttu-id="2dda7-137">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2dda7-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="2dda7-138">Этот cmdlet создает маркер SAS для таблицы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="2dda7-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="2dda7-139">-Permission</span><span class="sxs-lookup"><span data-stu-id="2dda7-139">-Permission</span></span>
<span data-ttu-id="2dda7-140">Определяет разрешения для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2dda7-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="2dda7-141">Важно отметить, что это строка (для `rwd` чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="2dda7-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="2dda7-142">-Политика</span><span class="sxs-lookup"><span data-stu-id="2dda7-142">-Policy</span></span>
<span data-ttu-id="2dda7-143">Определяет хранимую политику доступа, которая включает разрешения для этого токена SAS.</span><span class="sxs-lookup"><span data-stu-id="2dda7-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="2dda7-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2dda7-144">-Protocol</span></span>
<span data-ttu-id="2dda7-145">Определяет протокол, допустимый для запроса.</span><span class="sxs-lookup"><span data-stu-id="2dda7-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="2dda7-146">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="2dda7-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="2dda7-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2dda7-147">HttpsOnly</span></span>
* <span data-ttu-id="2dda7-148">По умолчанию httpsOrHttp имеет значение httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="2dda7-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="2dda7-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="2dda7-149">-StartPartitionKey</span></span>
<span data-ttu-id="2dda7-150">Определяет ключ раздела в начале диапазона для маркера, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dda7-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2dda7-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="2dda7-151">-StartRowKey</span></span>
<span data-ttu-id="2dda7-152">Указывает ключ строки для начала диапазона для маркера, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dda7-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2dda7-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2dda7-153">-StartTime</span></span>
<span data-ttu-id="2dda7-154">Указывает, когда маркер SAS становится допустимым.</span><span class="sxs-lookup"><span data-stu-id="2dda7-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="2dda7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dda7-155">CommonParameters</span></span>
<span data-ttu-id="2dda7-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dda7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dda7-157">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dda7-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dda7-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2dda7-158">INPUTS</span></span>

### <span data-ttu-id="2dda7-159">System.String</span><span class="sxs-lookup"><span data-stu-id="2dda7-159">System.String</span></span>

### <span data-ttu-id="2dda7-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2dda7-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2dda7-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2dda7-161">OUTPUTS</span></span>

### <span data-ttu-id="2dda7-162">System.String</span><span class="sxs-lookup"><span data-stu-id="2dda7-162">System.String</span></span>

## <span data-ttu-id="2dda7-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2dda7-163">NOTES</span></span>

## <span data-ttu-id="2dda7-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dda7-164">RELATED LINKS</span></span>

[<span data-ttu-id="2dda7-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2dda7-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
