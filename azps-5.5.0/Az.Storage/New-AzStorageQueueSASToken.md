---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 17a7e32d0686e68b70f2129edfbb617661057218
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229801"
---
# <span data-ttu-id="7e7f3-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="7e7f3-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="7e7f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7f3-103">Создает маркер подписи общего доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="7e7f3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e7f3-104">SYNTAX</span></span>

### <span data-ttu-id="7e7f3-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="7e7f3-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e7f3-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="7e7f3-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e7f3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e7f3-107">DESCRIPTION</span></span>
<span data-ttu-id="7e7f3-108">**Новый-AzStorageQueueSASToken** создает маркер подписи общего доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="7e7f3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e7f3-109">EXAMPLES</span></span>

### <span data-ttu-id="7e7f3-110">Пример 1. Создание маркера SAS в очереди с полными разрешениями</span><span class="sxs-lookup"><span data-stu-id="7e7f3-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="7e7f3-111">В этом примере создается маркер SAS в очереди с полными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="7e7f3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e7f3-112">PARAMETERS</span></span>

### <span data-ttu-id="7e7f3-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="7e7f3-113">-Context</span></span>
<span data-ttu-id="7e7f3-114">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7e7f3-115">Его можно создать с помощью New-AzStorageContext- или New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7e7f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7f3-116">-DefaultProfile</span></span>
<span data-ttu-id="7e7f3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e7f3-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7e7f3-118">-ExpiryTime</span></span>
<span data-ttu-id="7e7f3-119">Указывает, когда подпись общего доступа не является действительной.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="7e7f3-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="7e7f3-120">-FullUri</span></span>
<span data-ttu-id="7e7f3-121">Указывает на то, что этот cmdlet возвращает полный URI BLOB-приложений и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="7e7f3-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7e7f3-122">-IPAddressOrRange</span></span>
<span data-ttu-id="7e7f3-123">Указывает IP-адрес или диапазон IP-адресов, с которых нужно принимать запросы, например 168.1.5.65 или 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="7e7f3-124">Диапазон включительно.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="7e7f3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7e7f3-125">-Name</span></span>
<span data-ttu-id="7e7f3-126">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="7e7f3-127">-Permission</span><span class="sxs-lookup"><span data-stu-id="7e7f3-127">-Permission</span></span>
<span data-ttu-id="7e7f3-128">Определяет разрешения для очереди хранения.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="7e7f3-129">Важно отметить, что это строка (для `rwd` чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="7e7f3-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7e7f3-130">-Политика</span><span class="sxs-lookup"><span data-stu-id="7e7f3-130">-Policy</span></span>
<span data-ttu-id="7e7f3-131">Определяет политику хранимого доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="7e7f3-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7e7f3-132">-Protocol</span></span>
<span data-ttu-id="7e7f3-133">Определяет протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="7e7f3-134">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="7e7f3-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="7e7f3-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7e7f3-135">HttpsOnly</span></span>
* <span data-ttu-id="7e7f3-136">По умолчанию httpsOrHttp имеет значение httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="7e7f3-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7e7f3-137">-StartTime</span></span>
<span data-ttu-id="7e7f3-138">Указывает, когда подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="7e7f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7f3-139">CommonParameters</span></span>
<span data-ttu-id="7e7f3-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e7f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7f3-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e7f3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7f3-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e7f3-142">INPUTS</span></span>

### <span data-ttu-id="7e7f3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7e7f3-143">System.String</span></span>

### <span data-ttu-id="7e7f3-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e7f3-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7e7f3-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e7f3-145">OUTPUTS</span></span>

### <span data-ttu-id="7e7f3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7e7f3-146">System.String</span></span>

## <span data-ttu-id="7e7f3-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e7f3-147">NOTES</span></span>

## <span data-ttu-id="7e7f3-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e7f3-148">RELATED LINKS</span></span>
