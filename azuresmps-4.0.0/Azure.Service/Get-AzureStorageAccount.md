---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075549"
---
# <span data-ttu-id="61d41-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61d41-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="61d41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61d41-102">SYNOPSIS</span></span>
<span data-ttu-id="61d41-103">Возвращает учетные записи хранения для текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="61d41-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="61d41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61d41-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="61d41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d41-105">DESCRIPTION</span></span>
<span data-ttu-id="61d41-106">Командлет **Get-AzureStorageAccount** возвращает объект, содержащий сведения об учетных записях хранения для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="61d41-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="61d41-107">Если указан параметр *StorageAccountName* , возвращаются только сведения о указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="61d41-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="61d41-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61d41-108">EXAMPLES</span></span>

### <span data-ttu-id="61d41-109">Пример 1: возврат всех учетных записей хранения</span><span class="sxs-lookup"><span data-stu-id="61d41-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="61d41-110">Эта команда возвращает объект со всеми учетными записями хранения, связанными с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="61d41-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="61d41-111">Пример 2: возврат сведений об учетной записи для указанной учетной записи</span><span class="sxs-lookup"><span data-stu-id="61d41-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="61d41-112">Эта команда возвращает объект, содержащий только данные учетной записи ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="61d41-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="61d41-113">Пример 3: отображение таблицы учетных записей хранения</span><span class="sxs-lookup"><span data-stu-id="61d41-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="61d41-114">Эта команда возвращает объект со всеми учетными записями хранения, связанными с текущей подпиской, и выводит их в виде таблицы, в которой указано имя учетной записи, метка учетной записи и место хранения.</span><span class="sxs-lookup"><span data-stu-id="61d41-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="61d41-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61d41-115">PARAMETERS</span></span>

### <span data-ttu-id="61d41-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="61d41-116">-InformationAction</span></span>
<span data-ttu-id="61d41-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="61d41-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="61d41-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="61d41-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61d41-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="61d41-119">Continue</span></span>
- <span data-ttu-id="61d41-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="61d41-120">Ignore</span></span>
- <span data-ttu-id="61d41-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="61d41-121">Inquire</span></span>
- <span data-ttu-id="61d41-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="61d41-122">SilentlyContinue</span></span>
- <span data-ttu-id="61d41-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="61d41-123">Stop</span></span>
- <span data-ttu-id="61d41-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="61d41-124">Suspend</span></span>

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

### <span data-ttu-id="61d41-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="61d41-125">-InformationVariable</span></span>
<span data-ttu-id="61d41-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="61d41-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="61d41-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="61d41-127">-Profile</span></span>
<span data-ttu-id="61d41-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="61d41-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61d41-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61d41-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61d41-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="61d41-130">-StorageAccountName</span></span>
<span data-ttu-id="61d41-131">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="61d41-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="61d41-132">Если указан, этот командлет возвращает только указанный объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="61d41-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d41-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d41-133">CommonParameters</span></span>
<span data-ttu-id="61d41-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61d41-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d41-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d41-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d41-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61d41-136">INPUTS</span></span>

## <span data-ttu-id="61d41-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d41-137">OUTPUTS</span></span>

### <span data-ttu-id="61d41-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="61d41-138">ManagementOperationContext</span></span>

## <span data-ttu-id="61d41-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="61d41-139">NOTES</span></span>
* <span data-ttu-id="61d41-140">Введите `help node-dev` сведения о Node.js командлетах, связанных с разработкой.</span><span class="sxs-lookup"><span data-stu-id="61d41-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="61d41-141">Введите `help php-dev` справку по командлетам, связанным с разработкой PHP.</span><span class="sxs-lookup"><span data-stu-id="61d41-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="61d41-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61d41-142">RELATED LINKS</span></span>

[<span data-ttu-id="61d41-143">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61d41-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="61d41-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61d41-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


