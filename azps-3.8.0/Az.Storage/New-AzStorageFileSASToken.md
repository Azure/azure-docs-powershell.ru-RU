---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: b38f7d0463062f07e425decae98f8b6acba8c4ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074687"
---
# <span data-ttu-id="fe822-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="fe822-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="fe822-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe822-102">SYNOPSIS</span></span>
<span data-ttu-id="fe822-103">Создание маркера подписи общего доступа для файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe822-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="fe822-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe822-104">SYNTAX</span></span>

### <span data-ttu-id="fe822-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="fe822-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe822-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="fe822-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe822-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="fe822-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe822-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="fe822-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe822-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe822-109">DESCRIPTION</span></span>
<span data-ttu-id="fe822-110">Командлет **New-AzStorageFileSASToken** создает маркер подписи общего доступа для файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fe822-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="fe822-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe822-111">EXAMPLES</span></span>

### <span data-ttu-id="fe822-112">Пример 1: создание маркера подписи общего доступа с полными разрешениями для файлов</span><span class="sxs-lookup"><span data-stu-id="fe822-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="fe822-113">Эта команда создает маркер подписи общего доступа с полными разрешениями для файла с именем FilePath.</span><span class="sxs-lookup"><span data-stu-id="fe822-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="fe822-114">Пример 2: создание маркера подписи общего доступа с ограничением по времени</span><span class="sxs-lookup"><span data-stu-id="fe822-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="fe822-115">Первая команда создает объект **DateTime** с помощью командлета Get-Date.</span><span class="sxs-lookup"><span data-stu-id="fe822-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="fe822-116">В команде текущее время сохраняется в переменной $StartTime.</span><span class="sxs-lookup"><span data-stu-id="fe822-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="fe822-117">Вторая команда добавляет два часа к объекту в $StartTime, а затем сохраняет результат в переменной $EndTime.</span><span class="sxs-lookup"><span data-stu-id="fe822-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="fe822-118">Этот объект — это время в будущем за два часа.</span><span class="sxs-lookup"><span data-stu-id="fe822-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="fe822-119">Третья команда создает маркер подписи общего доступа с указанными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="fe822-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="fe822-120">Этот маркер становится действительным в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="fe822-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="fe822-121">Маркер действителен до тех пор, пока не будет сохранено в $EndTime.</span><span class="sxs-lookup"><span data-stu-id="fe822-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="fe822-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe822-122">PARAMETERS</span></span>

### <span data-ttu-id="fe822-123">-Context</span><span class="sxs-lookup"><span data-stu-id="fe822-123">-Context</span></span>
<span data-ttu-id="fe822-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fe822-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="fe822-125">Чтобы получить контекст, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fe822-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe822-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe822-126">-DefaultProfile</span></span>
<span data-ttu-id="fe822-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe822-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe822-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fe822-128">-ExpiryTime</span></span>
<span data-ttu-id="fe822-129">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="fe822-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="fe822-130">-Файл</span><span class="sxs-lookup"><span data-stu-id="fe822-130">-File</span></span>
<span data-ttu-id="fe822-131">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="fe822-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="fe822-132">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="fe822-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe822-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="fe822-133">-FullUri</span></span>
<span data-ttu-id="fe822-134">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="fe822-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="fe822-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="fe822-135">-IPAddressOrRange</span></span>
<span data-ttu-id="fe822-136">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="fe822-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="fe822-137">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="fe822-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="fe822-138">-Path</span><span class="sxs-lookup"><span data-stu-id="fe822-138">-Path</span></span>
<span data-ttu-id="fe822-139">Задает путь к файлу относительно общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="fe822-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe822-140">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="fe822-140">-Permission</span></span>
<span data-ttu-id="fe822-141">Задает разрешения для файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe822-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="fe822-142">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="fe822-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe822-143">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="fe822-143">-Policy</span></span>
<span data-ttu-id="fe822-144">Указывает политику сохраненного доступа для файла.</span><span class="sxs-lookup"><span data-stu-id="fe822-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe822-145">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="fe822-145">-Protocol</span></span>
<span data-ttu-id="fe822-146">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="fe822-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="fe822-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fe822-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="fe822-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="fe822-148">HttpsOnly</span></span>
* <span data-ttu-id="fe822-149">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="fe822-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="fe822-150">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="fe822-150">-ShareName</span></span>
<span data-ttu-id="fe822-151">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="fe822-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe822-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fe822-152">-StartTime</span></span>
<span data-ttu-id="fe822-153">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="fe822-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="fe822-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe822-154">CommonParameters</span></span>
<span data-ttu-id="fe822-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe822-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe822-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe822-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe822-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe822-157">INPUTS</span></span>

### <span data-ttu-id="fe822-158">System. String</span><span class="sxs-lookup"><span data-stu-id="fe822-158">System.String</span></span>

### <span data-ttu-id="fe822-159">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="fe822-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="fe822-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe822-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fe822-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe822-161">OUTPUTS</span></span>

### <span data-ttu-id="fe822-162">System. String</span><span class="sxs-lookup"><span data-stu-id="fe822-162">System.String</span></span>

## <span data-ttu-id="fe822-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe822-163">NOTES</span></span>

## <span data-ttu-id="fe822-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe822-164">RELATED LINKS</span></span>

[<span data-ttu-id="fe822-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe822-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fe822-166">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="fe822-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
