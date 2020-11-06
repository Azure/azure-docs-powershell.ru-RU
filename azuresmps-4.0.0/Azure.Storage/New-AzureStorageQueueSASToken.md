---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac818fd403df9b159671f5889e068bda82a086d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555896"
---
# <span data-ttu-id="e8e61-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="e8e61-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="e8e61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8e61-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e61-103">Создание маркера подписи общего доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e61-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="e8e61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8e61-104">SYNTAX</span></span>

### <span data-ttu-id="e8e61-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="e8e61-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e8e61-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="e8e61-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e8e61-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8e61-107">DESCRIPTION</span></span>
<span data-ttu-id="e8e61-108">Командлет **New-AzureStorageQueueSASToken** создает маркер подписи общего доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e61-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="e8e61-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8e61-109">EXAMPLES</span></span>

### <span data-ttu-id="e8e61-110">Пример 1: создание маркера SAS очереди с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="e8e61-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="e8e61-111">В этом примере создается маркер SAS очереди с полным разрешением.</span><span class="sxs-lookup"><span data-stu-id="e8e61-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="e8e61-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8e61-112">PARAMETERS</span></span>

### <span data-ttu-id="e8e61-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e8e61-113">-Context</span></span>
<span data-ttu-id="e8e61-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e61-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e8e61-115">Вы можете создать его с помощью New-AzureStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="e8e61-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e8e61-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e8e61-116">-ExpiryTime</span></span>
<span data-ttu-id="e8e61-117">Указывает, что подпись общего доступа больше не действительна.</span><span class="sxs-lookup"><span data-stu-id="e8e61-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="e8e61-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e8e61-118">-FullUri</span></span>
<span data-ttu-id="e8e61-119">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e8e61-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e8e61-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e8e61-120">-IPAddressOrRange</span></span>
<span data-ttu-id="e8e61-121">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="e8e61-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e8e61-122">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="e8e61-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="e8e61-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8e61-123">-Name</span></span>
<span data-ttu-id="e8e61-124">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e61-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e61-125">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="e8e61-125">-Permission</span></span>
<span data-ttu-id="e8e61-126">Задает разрешения для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="e8e61-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="e8e61-127">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e8e61-127">-Policy</span></span>
<span data-ttu-id="e8e61-128">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e61-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="e8e61-129">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e8e61-129">-Protocol</span></span>
<span data-ttu-id="e8e61-130">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="e8e61-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e8e61-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e8e61-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e8e61-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e8e61-132">HttpsOnly</span></span>
* <span data-ttu-id="e8e61-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e8e61-133">HttpsOrHttp</span></span>

<span data-ttu-id="e8e61-134">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="e8e61-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="e8e61-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e8e61-135">-StartTime</span></span>
<span data-ttu-id="e8e61-136">Указывает, когда подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="e8e61-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="e8e61-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e61-137">CommonParameters</span></span>
<span data-ttu-id="e8e61-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8e61-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e61-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8e61-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e61-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8e61-140">INPUTS</span></span>

## <span data-ttu-id="e8e61-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8e61-141">OUTPUTS</span></span>

## <span data-ttu-id="e8e61-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8e61-142">NOTES</span></span>

## <span data-ttu-id="e8e61-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8e61-143">RELATED LINKS</span></span>

