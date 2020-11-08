---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075548"
---
# <span data-ttu-id="d6da6-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="d6da6-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="d6da6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6da6-102">SYNOPSIS</span></span>
<span data-ttu-id="d6da6-103">Возвращает первичные и вторичные ключи учетной записи хранения для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="d6da6-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="d6da6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6da6-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d6da6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6da6-105">DESCRIPTION</span></span>
<span data-ttu-id="d6da6-106">Командлет **Get-AzureStorageKey** возвращает объект с именем учетной записи хранения Azure, основным ключом учетной записи и дополнительным ключом учетной записи хранения Azure в качестве свойств.</span><span class="sxs-lookup"><span data-stu-id="d6da6-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="d6da6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6da6-107">EXAMPLES</span></span>

### <span data-ttu-id="d6da6-108">Пример 1: получение объекта, содержащего основные и дополнительные ключи хранилища</span><span class="sxs-lookup"><span data-stu-id="d6da6-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="d6da6-109">Эта команда получает объект с основными и дополнительными ключами хранилища для учетной записи хранения ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="d6da6-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="d6da6-110">Пример 2: получение основного ключа учетной записи хранения и его хранение в переменной</span><span class="sxs-lookup"><span data-stu-id="d6da6-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="d6da6-111">Эта команда помещает основной ключ учетной записи хранения для учетной записи хранения ContosoStore01 в переменную $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="d6da6-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="d6da6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6da6-112">PARAMETERS</span></span>

### <span data-ttu-id="d6da6-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d6da6-113">-InformationAction</span></span>
<span data-ttu-id="d6da6-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d6da6-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d6da6-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d6da6-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6da6-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d6da6-116">Continue</span></span>
- <span data-ttu-id="d6da6-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d6da6-117">Ignore</span></span>
- <span data-ttu-id="d6da6-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d6da6-118">Inquire</span></span>
- <span data-ttu-id="d6da6-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d6da6-119">SilentlyContinue</span></span>
- <span data-ttu-id="d6da6-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="d6da6-120">Stop</span></span>
- <span data-ttu-id="d6da6-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="d6da6-121">Suspend</span></span>

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

### <span data-ttu-id="d6da6-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d6da6-122">-InformationVariable</span></span>
<span data-ttu-id="d6da6-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d6da6-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d6da6-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="d6da6-124">-Profile</span></span>
<span data-ttu-id="d6da6-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d6da6-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6da6-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6da6-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6da6-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d6da6-127">-StorageAccountName</span></span>
<span data-ttu-id="d6da6-128">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d6da6-128">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="d6da6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6da6-129">CommonParameters</span></span>
<span data-ttu-id="d6da6-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6da6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6da6-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6da6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6da6-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6da6-132">INPUTS</span></span>

## <span data-ttu-id="d6da6-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6da6-133">OUTPUTS</span></span>

## <span data-ttu-id="d6da6-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6da6-134">NOTES</span></span>
* <span data-ttu-id="d6da6-135">Чтобы получить справку по Node.js, используйте `help node-dev` команду.</span><span class="sxs-lookup"><span data-stu-id="d6da6-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="d6da6-136">Для получения справки по расширениям PHP используйте `help php-dev` команду.</span><span class="sxs-lookup"><span data-stu-id="d6da6-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="d6da6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6da6-137">RELATED LINKS</span></span>

[<span data-ttu-id="d6da6-138">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6da6-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="d6da6-139">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6da6-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="d6da6-140">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="d6da6-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="d6da6-141">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6da6-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="d6da6-142">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6da6-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


