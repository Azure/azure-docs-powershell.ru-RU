---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076458"
---
# <span data-ttu-id="73d79-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73d79-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="73d79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73d79-102">SYNOPSIS</span></span>
<span data-ttu-id="73d79-103">Удаление указанной учетной записи хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="73d79-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="73d79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73d79-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="73d79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73d79-105">DESCRIPTION</span></span>
<span data-ttu-id="73d79-106">Командлет **Remove-AzureStorageAccount** удаляет учетную запись из подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="73d79-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="73d79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73d79-107">EXAMPLES</span></span>

### <span data-ttu-id="73d79-108">Пример 1: Удаление учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="73d79-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="73d79-109">Эта команда удаляет учетную запись хранения ContosoStore01 из указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="73d79-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="73d79-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73d79-110">PARAMETERS</span></span>

### <span data-ttu-id="73d79-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="73d79-111">-InformationAction</span></span>
<span data-ttu-id="73d79-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="73d79-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="73d79-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="73d79-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73d79-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="73d79-114">Continue</span></span>
- <span data-ttu-id="73d79-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="73d79-115">Ignore</span></span>
- <span data-ttu-id="73d79-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="73d79-116">Inquire</span></span>
- <span data-ttu-id="73d79-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="73d79-117">SilentlyContinue</span></span>
- <span data-ttu-id="73d79-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="73d79-118">Stop</span></span>
- <span data-ttu-id="73d79-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="73d79-119">Suspend</span></span>

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

### <span data-ttu-id="73d79-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="73d79-120">-InformationVariable</span></span>
<span data-ttu-id="73d79-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="73d79-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="73d79-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="73d79-122">-Profile</span></span>
<span data-ttu-id="73d79-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="73d79-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73d79-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73d79-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73d79-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="73d79-125">-StorageAccountName</span></span>
<span data-ttu-id="73d79-126">Указывает имя учетной записи хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="73d79-126">Specifies the name of the storage account to remove.</span></span>

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

### <span data-ttu-id="73d79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d79-127">CommonParameters</span></span>
<span data-ttu-id="73d79-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73d79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d79-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73d79-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d79-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73d79-130">INPUTS</span></span>

## <span data-ttu-id="73d79-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73d79-131">OUTPUTS</span></span>

## <span data-ttu-id="73d79-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="73d79-132">NOTES</span></span>

## <span data-ttu-id="73d79-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73d79-133">RELATED LINKS</span></span>

[<span data-ttu-id="73d79-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73d79-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="73d79-135">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73d79-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="73d79-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73d79-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


