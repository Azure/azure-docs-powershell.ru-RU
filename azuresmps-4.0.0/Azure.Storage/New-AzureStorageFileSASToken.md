---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19d3017ffdff2ebc0f0c8d614b5b9c4d4b0514d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555904"
---
# <span data-ttu-id="1a4c2-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="1a4c2-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="1a4c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4c2-103">Создание маркера подписи общего доступа для файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="1a4c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a4c2-104">SYNTAX</span></span>

### <span data-ttu-id="1a4c2-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="1a4c2-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1a4c2-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="1a4c2-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1a4c2-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="1a4c2-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="1a4c2-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="1a4c2-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="1a4c2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a4c2-109">DESCRIPTION</span></span>
<span data-ttu-id="1a4c2-110">Командлет **New-AzureStorageFileSASToken** создает маркер подписи общего доступа для файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="1a4c2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a4c2-111">EXAMPLES</span></span>

### <span data-ttu-id="1a4c2-112">Пример 1: создание маркера подписи общего доступа с полными разрешениями для файлов</span><span class="sxs-lookup"><span data-stu-id="1a4c2-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="1a4c2-113">Эта команда создает маркер подписи общего доступа с полными разрешениями для файла с именем FilePath.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="1a4c2-114">Пример 2: создание маркера подписи общего доступа с ограничением по времени</span><span class="sxs-lookup"><span data-stu-id="1a4c2-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="1a4c2-115">Первая команда создает объект **DateTime** с помощью командлета Get-Date.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="1a4c2-116">В команде текущее время сохраняется в переменной $StartTime.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="1a4c2-117">Вторая команда добавляет два часа к объекту в $StartTime, а затем сохраняет результат в переменной $EndTime.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="1a4c2-118">Этот объект — это время в будущем за два часа.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="1a4c2-119">Третья команда создает маркер подписи общего доступа с указанными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="1a4c2-120">Этот маркер становится действительным в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="1a4c2-121">Маркер действителен до тех пор, пока не будет сохранено в $EndTime.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="1a4c2-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a4c2-122">PARAMETERS</span></span>

### <span data-ttu-id="1a4c2-123">-Context</span><span class="sxs-lookup"><span data-stu-id="1a4c2-123">-Context</span></span>
<span data-ttu-id="1a4c2-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1a4c2-125">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1a4c2-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1a4c2-126">-ExpiryTime</span></span>
<span data-ttu-id="1a4c2-127">Задает время, по истечении которого подпись общего доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="1a4c2-128">-Файл</span><span class="sxs-lookup"><span data-stu-id="1a4c2-128">-File</span></span>
<span data-ttu-id="1a4c2-129">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="1a4c2-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="1a4c2-130">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="1a4c2-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="1a4c2-131">-FullUri</span></span>
<span data-ttu-id="1a4c2-132">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="1a4c2-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1a4c2-133">-IPAddressOrRange</span></span>
<span data-ttu-id="1a4c2-134">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="1a4c2-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1a4c2-135">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="1a4c2-136">-Path</span><span class="sxs-lookup"><span data-stu-id="1a4c2-136">-Path</span></span>
<span data-ttu-id="1a4c2-137">Задает путь к файлу относительно общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-137">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="1a4c2-138">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="1a4c2-138">-Permission</span></span>
<span data-ttu-id="1a4c2-139">Задает разрешения для файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-139">Specifies the permissions for a Storage file.</span></span>

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

### <span data-ttu-id="1a4c2-140">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="1a4c2-140">-Policy</span></span>
<span data-ttu-id="1a4c2-141">Указывает политику сохраненного доступа для файла.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-141">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="1a4c2-142">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1a4c2-142">-Protocol</span></span>
<span data-ttu-id="1a4c2-143">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="1a4c2-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1a4c2-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="1a4c2-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1a4c2-145">HttpsOnly</span></span>
* <span data-ttu-id="1a4c2-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="1a4c2-146">HttpsOrHttp</span></span>

<span data-ttu-id="1a4c2-147">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="1a4c2-148">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="1a4c2-148">-ShareName</span></span>
<span data-ttu-id="1a4c2-149">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-149">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="1a4c2-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1a4c2-150">-StartTime</span></span>
<span data-ttu-id="1a4c2-151">Задает время, в течение которого подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="1a4c2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4c2-152">CommonParameters</span></span>
<span data-ttu-id="1a4c2-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a4c2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4c2-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a4c2-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4c2-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a4c2-155">INPUTS</span></span>

## <span data-ttu-id="1a4c2-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a4c2-156">OUTPUTS</span></span>

## <span data-ttu-id="1a4c2-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a4c2-157">NOTES</span></span>

## <span data-ttu-id="1a4c2-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a4c2-158">RELATED LINKS</span></span>

[<span data-ttu-id="1a4c2-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a4c2-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1a4c2-160">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="1a4c2-160">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
