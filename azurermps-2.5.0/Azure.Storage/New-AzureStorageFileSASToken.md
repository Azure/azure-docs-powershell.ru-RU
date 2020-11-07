---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
ms.openlocfilehash: 7c1b29cdb420ed0af4be8ce8ff07c73db179cabe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913702"
---
# <span data-ttu-id="ab052-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="ab052-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="ab052-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab052-102">SYNOPSIS</span></span>
<span data-ttu-id="ab052-103">Создание маркера подписи общего доступа для файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="ab052-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab052-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab052-104">SYNTAX</span></span>

### <span data-ttu-id="ab052-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="ab052-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab052-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="ab052-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab052-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="ab052-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab052-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="ab052-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab052-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab052-109">DESCRIPTION</span></span>
<span data-ttu-id="ab052-110">Командлет **New-AzureStorageFileSASToken** создает маркер подписи общего доступа для файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ab052-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="ab052-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab052-111">EXAMPLES</span></span>

### <span data-ttu-id="ab052-112">Пример 1: создание маркера подписи общего доступа с полными разрешениями для файлов</span><span class="sxs-lookup"><span data-stu-id="ab052-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="ab052-113">Эта команда создает маркер подписи общего доступа с полными разрешениями для файла с именем FilePath.</span><span class="sxs-lookup"><span data-stu-id="ab052-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="ab052-114">Пример 2: создание маркера подписи общего доступа с ограничением по времени</span><span class="sxs-lookup"><span data-stu-id="ab052-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="ab052-115">Первая команда создает объект **DateTime** с помощью командлета Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ab052-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="ab052-116">В команде текущее время сохраняется в переменной $StartTime.</span><span class="sxs-lookup"><span data-stu-id="ab052-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="ab052-117">Вторая команда добавляет два часа к объекту в $StartTime, а затем сохраняет результат в переменной $EndTime.</span><span class="sxs-lookup"><span data-stu-id="ab052-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="ab052-118">Этот объект — это время в будущем за два часа.</span><span class="sxs-lookup"><span data-stu-id="ab052-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="ab052-119">Третья команда создает маркер подписи общего доступа с указанными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="ab052-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="ab052-120">Этот маркер становится действительным в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="ab052-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="ab052-121">Маркер действителен до тех пор, пока не будет сохранено в $EndTime.</span><span class="sxs-lookup"><span data-stu-id="ab052-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="ab052-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab052-122">PARAMETERS</span></span>

### <span data-ttu-id="ab052-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ab052-123">-Context</span></span>
<span data-ttu-id="ab052-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ab052-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ab052-125">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ab052-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ab052-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab052-126">-DefaultProfile</span></span>
<span data-ttu-id="ab052-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab052-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab052-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ab052-128">-ExpiryTime</span></span>
<span data-ttu-id="ab052-129">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="ab052-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="ab052-130">-Файл</span><span class="sxs-lookup"><span data-stu-id="ab052-130">-File</span></span>
<span data-ttu-id="ab052-131">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="ab052-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ab052-132">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="ab052-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab052-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ab052-133">-FullUri</span></span>
<span data-ttu-id="ab052-134">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="ab052-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="ab052-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ab052-135">-IPAddressOrRange</span></span>
<span data-ttu-id="ab052-136">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="ab052-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ab052-137">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="ab052-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="ab052-138">-Path</span><span class="sxs-lookup"><span data-stu-id="ab052-138">-Path</span></span>
<span data-ttu-id="ab052-139">Задает путь к файлу относительно общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="ab052-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="ab052-140">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="ab052-140">-Permission</span></span>
<span data-ttu-id="ab052-141">Задает разрешения для файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="ab052-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="ab052-142">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="ab052-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ab052-143">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="ab052-143">-Policy</span></span>
<span data-ttu-id="ab052-144">Указывает политику сохраненного доступа для файла.</span><span class="sxs-lookup"><span data-stu-id="ab052-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="ab052-145">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="ab052-145">-Protocol</span></span>
<span data-ttu-id="ab052-146">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="ab052-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ab052-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ab052-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ab052-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ab052-148">HttpsOnly</span></span>
* <span data-ttu-id="ab052-149">HttpsOrHttp значение по умолчанию — HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="ab052-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ab052-150">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="ab052-150">-ShareName</span></span>
<span data-ttu-id="ab052-151">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="ab052-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="ab052-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ab052-152">-StartTime</span></span>
<span data-ttu-id="ab052-153">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="ab052-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="ab052-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab052-154">CommonParameters</span></span>
<span data-ttu-id="ab052-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab052-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab052-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab052-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab052-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab052-157">INPUTS</span></span>

### <span data-ttu-id="ab052-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ab052-158">System.String</span></span>

### <span data-ttu-id="ab052-159">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="ab052-159">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="ab052-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab052-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>
<span data-ttu-id="ab052-161">Параметры: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab052-161">Parameters: Context (ByValue)</span></span>

## <span data-ttu-id="ab052-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab052-162">OUTPUTS</span></span>

### <span data-ttu-id="ab052-163">System. String</span><span class="sxs-lookup"><span data-stu-id="ab052-163">System.String</span></span>

## <span data-ttu-id="ab052-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab052-164">NOTES</span></span>

## <span data-ttu-id="ab052-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab052-165">RELATED LINKS</span></span>

[<span data-ttu-id="ab052-166">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab052-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ab052-167">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="ab052-167">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
