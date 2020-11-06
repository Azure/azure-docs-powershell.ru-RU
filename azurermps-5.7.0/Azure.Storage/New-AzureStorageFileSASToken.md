---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
ms.openlocfilehash: e5e4eaf5fa6808432dfdb04120bf9ef92a98452b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565072"
---
# <span data-ttu-id="4f656-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="4f656-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="4f656-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f656-102">SYNOPSIS</span></span>
<span data-ttu-id="4f656-103">Создание маркера подписи общего доступа для файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="4f656-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f656-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f656-104">SYNTAX</span></span>

### <span data-ttu-id="4f656-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="4f656-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="4f656-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="4f656-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="4f656-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="4f656-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="4f656-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="4f656-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="4f656-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f656-109">DESCRIPTION</span></span>
<span data-ttu-id="4f656-110">Командлет **New-AzureStorageFileSASToken** создает маркер подписи общего доступа для файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4f656-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="4f656-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f656-111">EXAMPLES</span></span>

### <span data-ttu-id="4f656-112">Пример 1: создание маркера подписи общего доступа с полными разрешениями для файлов</span><span class="sxs-lookup"><span data-stu-id="4f656-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="4f656-113">Эта команда создает маркер подписи общего доступа с полными разрешениями для файла с именем FilePath.</span><span class="sxs-lookup"><span data-stu-id="4f656-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="4f656-114">Пример 2: создание маркера подписи общего доступа с ограничением по времени</span><span class="sxs-lookup"><span data-stu-id="4f656-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="4f656-115">Первая команда создает объект **DateTime** с помощью командлета Get-Date.</span><span class="sxs-lookup"><span data-stu-id="4f656-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="4f656-116">В команде текущее время сохраняется в переменной $StartTime.</span><span class="sxs-lookup"><span data-stu-id="4f656-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="4f656-117">Вторая команда добавляет два часа к объекту в $StartTime, а затем сохраняет результат в переменной $EndTime.</span><span class="sxs-lookup"><span data-stu-id="4f656-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="4f656-118">Этот объект — это время в будущем за два часа.</span><span class="sxs-lookup"><span data-stu-id="4f656-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="4f656-119">Третья команда создает маркер подписи общего доступа с указанными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="4f656-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="4f656-120">Этот маркер становится действительным в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="4f656-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="4f656-121">Маркер действителен до тех пор, пока не будет сохранено в $EndTime.</span><span class="sxs-lookup"><span data-stu-id="4f656-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="4f656-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f656-122">PARAMETERS</span></span>

### <span data-ttu-id="4f656-123">-Context</span><span class="sxs-lookup"><span data-stu-id="4f656-123">-Context</span></span>
<span data-ttu-id="4f656-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4f656-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4f656-125">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4f656-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f656-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4f656-126">-ExpiryTime</span></span>
<span data-ttu-id="4f656-127">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="4f656-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="4f656-128">-Файл</span><span class="sxs-lookup"><span data-stu-id="4f656-128">-File</span></span>
<span data-ttu-id="4f656-129">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="4f656-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="4f656-130">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="4f656-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f656-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="4f656-131">-FullUri</span></span>
<span data-ttu-id="4f656-132">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="4f656-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="4f656-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4f656-133">-IPAddressOrRange</span></span>
<span data-ttu-id="4f656-134">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="4f656-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4f656-135">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="4f656-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="4f656-136">-Path</span><span class="sxs-lookup"><span data-stu-id="4f656-136">-Path</span></span>
<span data-ttu-id="4f656-137">Задает путь к файлу относительно общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="4f656-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f656-138">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="4f656-138">-Permission</span></span>
<span data-ttu-id="4f656-139">Задает разрешения для файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="4f656-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f656-140">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="4f656-140">-Policy</span></span>
<span data-ttu-id="4f656-141">Указывает политику сохраненного доступа для файла.</span><span class="sxs-lookup"><span data-stu-id="4f656-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f656-142">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="4f656-142">-Protocol</span></span>
<span data-ttu-id="4f656-143">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="4f656-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="4f656-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4f656-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="4f656-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4f656-145">HttpsOnly</span></span>
* <span data-ttu-id="4f656-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="4f656-146">HttpsOrHttp</span></span>

<span data-ttu-id="4f656-147">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="4f656-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="4f656-148">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="4f656-148">-ShareName</span></span>
<span data-ttu-id="4f656-149">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="4f656-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f656-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4f656-150">-StartTime</span></span>
<span data-ttu-id="4f656-151">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="4f656-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="4f656-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f656-152">CommonParameters</span></span>
<span data-ttu-id="4f656-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f656-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f656-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f656-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f656-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f656-155">INPUTS</span></span>

### <span data-ttu-id="4f656-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f656-156">IStorageContext</span></span>

<span data-ttu-id="4f656-157">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4f656-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4f656-158">CloudFile</span><span class="sxs-lookup"><span data-stu-id="4f656-158">CloudFile</span></span>

<span data-ttu-id="4f656-159">Параметр "файл" принимает значение типа "CloudFile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4f656-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="4f656-160">Подстрок</span><span class="sxs-lookup"><span data-stu-id="4f656-160">String</span></span>

<span data-ttu-id="4f656-161">Параметр "путь" принимает значение типа "String" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4f656-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="4f656-162">Подстрок</span><span class="sxs-lookup"><span data-stu-id="4f656-162">String</span></span>

<span data-ttu-id="4f656-163">Параметр ShareName принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4f656-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4f656-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f656-164">OUTPUTS</span></span>

### <span data-ttu-id="4f656-165">System. String</span><span class="sxs-lookup"><span data-stu-id="4f656-165">System.String</span></span>

## <span data-ttu-id="4f656-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f656-166">NOTES</span></span>

## <span data-ttu-id="4f656-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f656-167">RELATED LINKS</span></span>

[<span data-ttu-id="4f656-168">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f656-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4f656-169">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="4f656-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
