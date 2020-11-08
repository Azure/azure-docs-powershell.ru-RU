---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075850"
---
# <span data-ttu-id="97a39-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97a39-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="97a39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97a39-102">SYNOPSIS</span></span>
<span data-ttu-id="97a39-103">Обновляет свойства учетной записи хранения в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="97a39-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="97a39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97a39-104">SYNTAX</span></span>

### <span data-ttu-id="97a39-105">AccountType (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97a39-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="97a39-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="97a39-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="97a39-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97a39-107">DESCRIPTION</span></span>
<span data-ttu-id="97a39-108">Командлет **Set-AzureStorageAccount** обновляет свойства учетной записи хранения Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="97a39-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="97a39-109">Свойства, которые можно настроить: **Label** , **Description** , **Type** и **GeoReplicationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="97a39-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="97a39-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97a39-110">EXAMPLES</span></span>

### <span data-ttu-id="97a39-111">Пример 1: обновление метки для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="97a39-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="97a39-112">Эта команда обновляет свойства **Label** и **Description** для учетной записи хранения с именем ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="97a39-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="97a39-113">Пример 2: включение георепликации для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="97a39-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="97a39-114">Эта команда устанавливает для свойства **GeoReplicationEnabled** значение $false для учетной записи хранения с именем ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="97a39-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="97a39-115">Пример 3: отключение георепликации для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="97a39-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="97a39-116">Эта команда устанавливает для свойства **GeoReplicationEnabled** значение $true для учетной записи хранения с именем ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="97a39-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="97a39-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97a39-117">PARAMETERS</span></span>

### <span data-ttu-id="97a39-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="97a39-118">-Description</span></span>
<span data-ttu-id="97a39-119">Задает описание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="97a39-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="97a39-120">Описание может иметь длину до 1024 символов.</span><span class="sxs-lookup"><span data-stu-id="97a39-120">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="97a39-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="97a39-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="97a39-122">Указывает, будет ли создана учетная запись хранилища с включенной георепликацией.</span><span class="sxs-lookup"><span data-stu-id="97a39-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a39-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="97a39-123">-InformationAction</span></span>
<span data-ttu-id="97a39-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="97a39-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="97a39-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="97a39-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97a39-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="97a39-126">Continue</span></span>
- <span data-ttu-id="97a39-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="97a39-127">Ignore</span></span>
- <span data-ttu-id="97a39-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="97a39-128">Inquire</span></span>
- <span data-ttu-id="97a39-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="97a39-129">SilentlyContinue</span></span>
- <span data-ttu-id="97a39-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="97a39-130">Stop</span></span>
- <span data-ttu-id="97a39-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="97a39-131">Suspend</span></span>

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

### <span data-ttu-id="97a39-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="97a39-132">-InformationVariable</span></span>
<span data-ttu-id="97a39-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="97a39-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="97a39-134">-Label</span><span class="sxs-lookup"><span data-stu-id="97a39-134">-Label</span></span>
<span data-ttu-id="97a39-135">Указывает метку для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="97a39-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="97a39-136">Метка может иметь длину до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="97a39-136">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="97a39-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="97a39-137">-Profile</span></span>
<span data-ttu-id="97a39-138">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="97a39-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97a39-139">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97a39-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97a39-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="97a39-140">-StorageAccountName</span></span>
<span data-ttu-id="97a39-141">Указывает имя учетной записи хранения, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="97a39-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a39-142">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="97a39-142">-Type</span></span>
<span data-ttu-id="97a39-143">Указывает тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="97a39-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="97a39-144">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="97a39-144">Valid values are:</span></span> 

- <span data-ttu-id="97a39-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="97a39-145">Standard_LRS</span></span>
- <span data-ttu-id="97a39-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="97a39-146">Standard_ZRS</span></span>
- <span data-ttu-id="97a39-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="97a39-147">Standard_GRS</span></span>
- <span data-ttu-id="97a39-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="97a39-148">Standard_RAGRS</span></span>
- <span data-ttu-id="97a39-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="97a39-149">Premium_LRS</span></span>

<span data-ttu-id="97a39-150">Если этот параметр не указан, используется значение по умолчанию Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="97a39-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="97a39-151">Результат указания параметра *GeoReplicationEnabled* совпадает с указанием Standard_GRS в параметре *Type* .</span><span class="sxs-lookup"><span data-stu-id="97a39-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="97a39-152">Учетные записи Standard_ZRS и Premium_LRS нельзя изменить на другие типы, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="97a39-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a39-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a39-153">CommonParameters</span></span>
<span data-ttu-id="97a39-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97a39-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a39-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a39-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a39-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97a39-156">INPUTS</span></span>

## <span data-ttu-id="97a39-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97a39-157">OUTPUTS</span></span>

## <span data-ttu-id="97a39-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="97a39-158">NOTES</span></span>

## <span data-ttu-id="97a39-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97a39-159">RELATED LINKS</span></span>

[<span data-ttu-id="97a39-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97a39-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="97a39-161">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97a39-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="97a39-162">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97a39-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


