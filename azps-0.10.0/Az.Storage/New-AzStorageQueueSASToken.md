---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 4c3715a3c6228e45bfa52fd9a222be2cae84ef01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910721"
---
# <span data-ttu-id="820be-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="820be-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="820be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="820be-102">SYNOPSIS</span></span>
<span data-ttu-id="820be-103">Создание маркера подписи общего доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="820be-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="820be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="820be-104">SYNTAX</span></span>

### <span data-ttu-id="820be-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="820be-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="820be-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="820be-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="820be-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="820be-107">DESCRIPTION</span></span>
<span data-ttu-id="820be-108">Командлет **New-AzStorageQueueSASToken** создает маркер подписи общего доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="820be-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="820be-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="820be-109">EXAMPLES</span></span>

### <span data-ttu-id="820be-110">Пример 1: создание маркера SAS очереди с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="820be-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="820be-111">В этом примере создается маркер SAS очереди с полным разрешением.</span><span class="sxs-lookup"><span data-stu-id="820be-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="820be-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="820be-112">PARAMETERS</span></span>

### <span data-ttu-id="820be-113">-Context</span><span class="sxs-lookup"><span data-stu-id="820be-113">-Context</span></span>
<span data-ttu-id="820be-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="820be-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="820be-115">Вы можете создать его с помощью New-AzStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="820be-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="820be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="820be-116">-DefaultProfile</span></span>
<span data-ttu-id="820be-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="820be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="820be-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="820be-118">-ExpiryTime</span></span>
<span data-ttu-id="820be-119">Указывает, что подпись общего доступа больше не действительна.</span><span class="sxs-lookup"><span data-stu-id="820be-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="820be-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="820be-120">-FullUri</span></span>
<span data-ttu-id="820be-121">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="820be-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="820be-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="820be-122">-IPAddressOrRange</span></span>
<span data-ttu-id="820be-123">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="820be-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="820be-124">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="820be-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="820be-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="820be-125">-Name</span></span>
<span data-ttu-id="820be-126">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="820be-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="820be-127">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="820be-127">-Permission</span></span>
<span data-ttu-id="820be-128">Задает разрешения для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="820be-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="820be-129">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="820be-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="820be-130">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="820be-130">-Policy</span></span>
<span data-ttu-id="820be-131">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="820be-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="820be-132">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="820be-132">-Protocol</span></span>
<span data-ttu-id="820be-133">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="820be-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="820be-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="820be-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="820be-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="820be-135">HttpsOnly</span></span>
* <span data-ttu-id="820be-136">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="820be-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820be-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="820be-137">-StartTime</span></span>
<span data-ttu-id="820be-138">Указывает, когда подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="820be-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="820be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="820be-139">CommonParameters</span></span>
<span data-ttu-id="820be-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="820be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="820be-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="820be-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="820be-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="820be-142">INPUTS</span></span>

### <span data-ttu-id="820be-143">System. String</span><span class="sxs-lookup"><span data-stu-id="820be-143">System.String</span></span>

### <span data-ttu-id="820be-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="820be-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="820be-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="820be-145">OUTPUTS</span></span>

### <span data-ttu-id="820be-146">System. String</span><span class="sxs-lookup"><span data-stu-id="820be-146">System.String</span></span>

## <span data-ttu-id="820be-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="820be-147">NOTES</span></span>

## <span data-ttu-id="820be-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="820be-148">RELATED LINKS</span></span>
