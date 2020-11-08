---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076203"
---
# <span data-ttu-id="67867-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="67867-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="67867-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67867-102">SYNOPSIS</span></span>
<span data-ttu-id="67867-103">Повторное создание ключей хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="67867-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="67867-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67867-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="67867-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67867-105">DESCRIPTION</span></span>
<span data-ttu-id="67867-106">Командлет **New-AzureStorageKey** заново создает первичный или вторичный ключ для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="67867-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="67867-107">Функция возвращает объект, который включает в себя имя учетной записи хранения, первичный ключ и вторичный ключ в качестве свойств.</span><span class="sxs-lookup"><span data-stu-id="67867-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="67867-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67867-108">EXAMPLES</span></span>

### <span data-ttu-id="67867-109">Пример 1: повторное создание основного ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="67867-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="67867-110">Эта команда повторно создает основной ключ хранилища для учетной записи хранения ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="67867-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="67867-111">Пример 2: повторное создание дополнительного ключа хранилища и его сохранение в переменной</span><span class="sxs-lookup"><span data-stu-id="67867-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="67867-112">Эта команда повторно создает вторичный ключ хранилища для учетной записи хранения ContosoStore01 и сохраняет обновленные сведения о ключе учетной записи хранения в $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="67867-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="67867-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67867-113">PARAMETERS</span></span>

### <span data-ttu-id="67867-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="67867-114">-InformationAction</span></span>
<span data-ttu-id="67867-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="67867-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="67867-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="67867-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67867-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="67867-117">Continue</span></span>
- <span data-ttu-id="67867-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="67867-118">Ignore</span></span>
- <span data-ttu-id="67867-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="67867-119">Inquire</span></span>
- <span data-ttu-id="67867-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="67867-120">SilentlyContinue</span></span>
- <span data-ttu-id="67867-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="67867-121">Stop</span></span>
- <span data-ttu-id="67867-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="67867-122">Suspend</span></span>

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

### <span data-ttu-id="67867-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="67867-123">-InformationVariable</span></span>
<span data-ttu-id="67867-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="67867-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="67867-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="67867-125">-KeyType</span></span>
<span data-ttu-id="67867-126">Указывает, какой ключ нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="67867-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="67867-127">Допустимые значения: Primary и Secondary.</span><span class="sxs-lookup"><span data-stu-id="67867-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67867-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="67867-128">-Profile</span></span>
<span data-ttu-id="67867-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="67867-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67867-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="67867-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67867-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="67867-131">-StorageAccountName</span></span>
<span data-ttu-id="67867-132">Указывает имя учетной записи хранилища Azure, для которой необходимо повторно создать ключ.</span><span class="sxs-lookup"><span data-stu-id="67867-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67867-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67867-133">CommonParameters</span></span>
<span data-ttu-id="67867-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67867-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67867-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67867-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67867-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67867-136">INPUTS</span></span>

## <span data-ttu-id="67867-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67867-137">OUTPUTS</span></span>

### <span data-ttu-id="67867-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="67867-138">StorageServiceKeys</span></span>

## <span data-ttu-id="67867-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="67867-139">NOTES</span></span>

## <span data-ttu-id="67867-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67867-140">RELATED LINKS</span></span>

[<span data-ttu-id="67867-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="67867-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


