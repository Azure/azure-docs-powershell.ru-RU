---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
ms.openlocfilehash: becdf63590b5c5abc5e7095b96e13586232311d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556216"
---
# <span data-ttu-id="d6a4f-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d6a4f-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="d6a4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a4f-103">Создание маркера SAS для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="d6a4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6a4f-104">SYNTAX</span></span>

### <span data-ttu-id="d6a4f-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="d6a4f-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d6a4f-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="d6a4f-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d6a4f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6a4f-107">DESCRIPTION</span></span>
<span data-ttu-id="d6a4f-108">Командлет **New-AzureStorageContainerSASToken** создает маркер подписи общего доступа (SAS) для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="d6a4f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6a4f-109">EXAMPLES</span></span>

### <span data-ttu-id="d6a4f-110">Пример 1: создание маркера безопасности контейнера с разрешениями полного контейнера</span><span class="sxs-lookup"><span data-stu-id="d6a4f-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="d6a4f-111">В этом примере создается маркер безопасности контейнера с разрешениями полного контейнера.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="d6a4f-112">Пример 2: создание маркера SAS с несколькими контейнерами с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="d6a4f-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="d6a4f-113">В этом примере создается несколько маркеров сопоставления безопасности контейнера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="d6a4f-114">Пример 3: создание маркера SAS контейнера с политикой общего доступа</span><span class="sxs-lookup"><span data-stu-id="d6a4f-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="d6a4f-115">В этом примере создается маркер SAS контейнера с политикой общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="d6a4f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6a4f-116">PARAMETERS</span></span>

### <span data-ttu-id="d6a4f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d6a4f-117">-Context</span></span>
<span data-ttu-id="d6a4f-118">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d6a4f-119">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d6a4f-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d6a4f-120">-ExpiryTime</span></span>
<span data-ttu-id="d6a4f-121">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="d6a4f-122">Если пользователь задает время начала, но не время окончания срока действия, в качестве времени окончания устанавливается время начала плюс один час.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="d6a4f-123">Если не задано ни время начала, ни время окончания срока действия, в качестве времени окончания устанавливается текущее время плюс один час.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="d6a4f-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d6a4f-124">-FullUri</span></span>
<span data-ttu-id="d6a4f-125">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="d6a4f-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d6a4f-126">-IPAddressOrRange</span></span>
<span data-ttu-id="d6a4f-127">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="d6a4f-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d6a4f-128">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="d6a4f-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6a4f-129">-Name</span></span>
<span data-ttu-id="d6a4f-130">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a4f-131">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="d6a4f-131">-Permission</span></span>
<span data-ttu-id="d6a4f-132">Задает разрешения для контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="d6a4f-133">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="d6a4f-133">-Policy</span></span>
<span data-ttu-id="d6a4f-134">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="d6a4f-135">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="d6a4f-135">-Protocol</span></span>
<span data-ttu-id="d6a4f-136">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d6a4f-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d6a4f-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d6a4f-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d6a4f-138">HttpsOnly</span></span>
* <span data-ttu-id="d6a4f-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="d6a4f-139">HttpsOrHttp</span></span>

<span data-ttu-id="d6a4f-140">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="d6a4f-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d6a4f-141">-StartTime</span></span>
<span data-ttu-id="d6a4f-142">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d6a4f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a4f-143">CommonParameters</span></span>
<span data-ttu-id="d6a4f-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a4f-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a4f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a4f-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6a4f-146">INPUTS</span></span>

## <span data-ttu-id="d6a4f-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6a4f-147">OUTPUTS</span></span>

## <span data-ttu-id="d6a4f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6a4f-148">NOTES</span></span>

## <span data-ttu-id="d6a4f-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6a4f-149">RELATED LINKS</span></span>

[<span data-ttu-id="d6a4f-150">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d6a4f-150">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
