---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
ms.openlocfilehash: 3fa5a642bd5d8c53b81422f54fdb2c133304cc03
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915454"
---
# <span data-ttu-id="8037d-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8037d-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="8037d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8037d-102">SYNOPSIS</span></span>
<span data-ttu-id="8037d-103">Создание маркера SAS для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8037d-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8037d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8037d-104">SYNTAX</span></span>

### <span data-ttu-id="8037d-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="8037d-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8037d-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="8037d-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8037d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8037d-107">DESCRIPTION</span></span>
<span data-ttu-id="8037d-108">Командлет **New-AzureStorageContainerSASToken** создает маркер подписи общего доступа (SAS) для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8037d-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="8037d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8037d-109">EXAMPLES</span></span>

### <span data-ttu-id="8037d-110">Пример 1: создание маркера безопасности контейнера с разрешениями полного контейнера</span><span class="sxs-lookup"><span data-stu-id="8037d-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="8037d-111">В этом примере создается маркер безопасности контейнера с разрешениями полного контейнера.</span><span class="sxs-lookup"><span data-stu-id="8037d-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="8037d-112">Пример 2: создание маркера SAS с несколькими контейнерами с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="8037d-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="8037d-113">В этом примере создается несколько маркеров сопоставления безопасности контейнера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="8037d-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="8037d-114">Пример 3: создание маркера SAS контейнера с политикой общего доступа</span><span class="sxs-lookup"><span data-stu-id="8037d-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="8037d-115">В этом примере создается маркер SAS контейнера с политикой общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8037d-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="8037d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8037d-116">PARAMETERS</span></span>

### <span data-ttu-id="8037d-117">-Context</span><span class="sxs-lookup"><span data-stu-id="8037d-117">-Context</span></span>
<span data-ttu-id="8037d-118">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8037d-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8037d-119">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8037d-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8037d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8037d-120">-DefaultProfile</span></span>
<span data-ttu-id="8037d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8037d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8037d-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8037d-122">-ExpiryTime</span></span>
<span data-ttu-id="8037d-123">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="8037d-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="8037d-124">Если пользователь задает время начала, но не время окончания срока действия, в качестве времени окончания устанавливается время начала плюс один час.</span><span class="sxs-lookup"><span data-stu-id="8037d-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="8037d-125">Если не задано ни время начала, ни время окончания срока действия, в качестве времени окончания устанавливается текущее время плюс один час.</span><span class="sxs-lookup"><span data-stu-id="8037d-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="8037d-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8037d-126">-FullUri</span></span>
<span data-ttu-id="8037d-127">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8037d-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="8037d-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8037d-128">-IPAddressOrRange</span></span>
<span data-ttu-id="8037d-129">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="8037d-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8037d-130">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="8037d-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="8037d-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8037d-131">-Name</span></span>
<span data-ttu-id="8037d-132">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8037d-132">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8037d-133">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="8037d-133">-Permission</span></span>
<span data-ttu-id="8037d-134">Задает разрешения для контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="8037d-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="8037d-135">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="8037d-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8037d-136">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="8037d-136">-Policy</span></span>
<span data-ttu-id="8037d-137">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="8037d-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="8037d-138">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="8037d-138">-Protocol</span></span>
<span data-ttu-id="8037d-139">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="8037d-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8037d-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8037d-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8037d-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8037d-141">HttpsOnly</span></span>
* <span data-ttu-id="8037d-142">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8037d-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="8037d-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8037d-143">-StartTime</span></span>
<span data-ttu-id="8037d-144">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="8037d-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="8037d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8037d-145">CommonParameters</span></span>
<span data-ttu-id="8037d-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8037d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8037d-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8037d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8037d-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8037d-148">INPUTS</span></span>

### <span data-ttu-id="8037d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8037d-149">System.String</span></span>

### <span data-ttu-id="8037d-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8037d-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8037d-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8037d-151">OUTPUTS</span></span>

### <span data-ttu-id="8037d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8037d-152">System.String</span></span>

## <span data-ttu-id="8037d-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="8037d-153">NOTES</span></span>

## <span data-ttu-id="8037d-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8037d-154">RELATED LINKS</span></span>

[<span data-ttu-id="8037d-155">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8037d-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
