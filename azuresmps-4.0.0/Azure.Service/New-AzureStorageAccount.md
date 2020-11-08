---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076204"
---
# <span data-ttu-id="6875a-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6875a-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="6875a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6875a-102">SYNOPSIS</span></span>
<span data-ttu-id="6875a-103">Создание новой учетной записи хранения в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6875a-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="6875a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6875a-104">SYNTAX</span></span>

### <span data-ttu-id="6875a-105">ParameterSetAffinityGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6875a-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6875a-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="6875a-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6875a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6875a-107">DESCRIPTION</span></span>
<span data-ttu-id="6875a-108">Командлет **New-AzureStorageAccount** создает учетную запись, которая предоставляет доступ к службам хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6875a-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="6875a-109">Учетная запись хранения — это глобальный уникальный ресурс в системе хранения данных.</span><span class="sxs-lookup"><span data-stu-id="6875a-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="6875a-110">Учетная запись является родительским пространством для BLOB-объектов, очереди и служб таблиц.</span><span class="sxs-lookup"><span data-stu-id="6875a-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="6875a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6875a-111">EXAMPLES</span></span>

### <span data-ttu-id="6875a-112">Пример 1: создание учетной записи хранения для указанной территориальной группы</span><span class="sxs-lookup"><span data-stu-id="6875a-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="6875a-113">Эта команда создает учетную запись хранения для указанной территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="6875a-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="6875a-114">Пример 2: создание учетной записи хранения в указанном расположении</span><span class="sxs-lookup"><span data-stu-id="6875a-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="6875a-115">Эта команда создает учетную запись хранения в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="6875a-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="6875a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6875a-116">PARAMETERS</span></span>

### <span data-ttu-id="6875a-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="6875a-117">-AffinityGroup</span></span>
<span data-ttu-id="6875a-118">Указывает имя существующей территориальной группы в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="6875a-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="6875a-119">Вы можете указать либо параметр *Location* , либо *AffinityGroup* , но не оба.</span><span class="sxs-lookup"><span data-stu-id="6875a-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6875a-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="6875a-120">-Description</span></span>
<span data-ttu-id="6875a-121">Задает описание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6875a-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="6875a-122">Описание может иметь длину до 1024 символов.</span><span class="sxs-lookup"><span data-stu-id="6875a-122">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6875a-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6875a-123">-InformationAction</span></span>
<span data-ttu-id="6875a-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6875a-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6875a-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6875a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6875a-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6875a-126">Continue</span></span>
- <span data-ttu-id="6875a-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6875a-127">Ignore</span></span>
- <span data-ttu-id="6875a-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6875a-128">Inquire</span></span>
- <span data-ttu-id="6875a-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6875a-129">SilentlyContinue</span></span>
- <span data-ttu-id="6875a-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="6875a-130">Stop</span></span>
- <span data-ttu-id="6875a-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="6875a-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6875a-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6875a-132">-InformationVariable</span></span>
<span data-ttu-id="6875a-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6875a-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6875a-134">-Label</span><span class="sxs-lookup"><span data-stu-id="6875a-134">-Label</span></span>
<span data-ttu-id="6875a-135">Указывает метку для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6875a-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="6875a-136">Метка может иметь длину до 100 знаков.</span><span class="sxs-lookup"><span data-stu-id="6875a-136">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6875a-137">-Location</span><span class="sxs-lookup"><span data-stu-id="6875a-137">-Location</span></span>
<span data-ttu-id="6875a-138">Указывает расположение центра обработки данных Azure, в котором создана учетная запись хранения.</span><span class="sxs-lookup"><span data-stu-id="6875a-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="6875a-139">Вы можете включить параметр *Location* или *AffinityGroup* , но не оба.</span><span class="sxs-lookup"><span data-stu-id="6875a-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6875a-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="6875a-140">-Profile</span></span>
<span data-ttu-id="6875a-141">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6875a-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6875a-142">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6875a-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6875a-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6875a-143">-StorageAccountName</span></span>
<span data-ttu-id="6875a-144">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6875a-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="6875a-145">Имя учетной записи хранения должно быть уникальным для Azure и должно составлять от 3 до 24 символов и использовать только строчные буквы и цифры.</span><span class="sxs-lookup"><span data-stu-id="6875a-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6875a-146">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="6875a-146">-Type</span></span>
<span data-ttu-id="6875a-147">Указывает тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6875a-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="6875a-148">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6875a-148">Valid values are:</span></span>

- <span data-ttu-id="6875a-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="6875a-149">Standard_LRS</span></span>
- <span data-ttu-id="6875a-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="6875a-150">Standard_ZRS</span></span>
- <span data-ttu-id="6875a-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="6875a-151">Standard_GRS</span></span>
- <span data-ttu-id="6875a-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="6875a-152">Standard_RAGRS</span></span>
- <span data-ttu-id="6875a-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="6875a-153">Premium_LRS</span></span>

<span data-ttu-id="6875a-154">Если этот параметр не указан, используется значение по умолчанию Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="6875a-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="6875a-155">Учетные записи Standard_ZRS и Premium_LRS нельзя изменить на другие типы, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="6875a-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

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

### <span data-ttu-id="6875a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6875a-156">CommonParameters</span></span>
<span data-ttu-id="6875a-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6875a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6875a-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6875a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6875a-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6875a-159">INPUTS</span></span>

## <span data-ttu-id="6875a-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6875a-160">OUTPUTS</span></span>

## <span data-ttu-id="6875a-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="6875a-161">NOTES</span></span>

## <span data-ttu-id="6875a-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6875a-162">RELATED LINKS</span></span>

[<span data-ttu-id="6875a-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6875a-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="6875a-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6875a-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


