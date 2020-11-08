---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075698"
---
# <span data-ttu-id="0a355-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="0a355-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="0a355-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a355-102">SYNOPSIS</span></span>
<span data-ttu-id="0a355-103">Копирует пользовательский диск пользователя из одной коллекции Azure RemoteApp в другую.</span><span class="sxs-lookup"><span data-stu-id="0a355-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="0a355-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a355-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0a355-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a355-105">DESCRIPTION</span></span>
<span data-ttu-id="0a355-106">Командлет **Copy-AzureRemoteAppUserDisk** копирует пользовательский диск пользователя из одной коллекции Azure RemoteApp в другую.</span><span class="sxs-lookup"><span data-stu-id="0a355-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="0a355-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a355-107">EXAMPLES</span></span>

### <span data-ttu-id="0a355-108">Пример 1: копирование диска пользователя</span><span class="sxs-lookup"><span data-stu-id="0a355-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="0a355-109">Эта команда копирует диск пользователя для Azure Active Directory, имеющий имя участника-пользователя PattiFuller@contoso.com из коллекции, Contoso01 с коллекцией Contoso02.</span><span class="sxs-lookup"><span data-stu-id="0a355-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="0a355-110">Если диск пользователя PattiFuller@contoso.com уже существует на Contoso02, эта команда перезапишет ее.</span><span class="sxs-lookup"><span data-stu-id="0a355-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="0a355-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a355-111">PARAMETERS</span></span>

### <span data-ttu-id="0a355-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="0a355-112">-DestinationCollectionName</span></span>
<span data-ttu-id="0a355-113">Указывает имя целевой коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="0a355-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a355-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="0a355-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="0a355-115">Указывает на то, что этот командлет перезапишет существующий диск пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a355-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

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

### <span data-ttu-id="0a355-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="0a355-116">-Profile</span></span>
<span data-ttu-id="0a355-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0a355-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a355-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a355-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a355-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0a355-119">-SourceCollectionName</span></span>
<span data-ttu-id="0a355-120">Указывает имя исходной коллекции RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="0a355-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a355-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="0a355-121">-UserUpn</span></span>
<span data-ttu-id="0a355-122">Указывает имя участника-пользователя (UPN), для которого этот командлет копирует диск.</span><span class="sxs-lookup"><span data-stu-id="0a355-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a355-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a355-123">CommonParameters</span></span>
<span data-ttu-id="0a355-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a355-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a355-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a355-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a355-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a355-126">INPUTS</span></span>

## <span data-ttu-id="0a355-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a355-127">OUTPUTS</span></span>

## <span data-ttu-id="0a355-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a355-128">NOTES</span></span>

## <span data-ttu-id="0a355-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a355-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a355-130">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="0a355-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


