---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076319"
---
# <span data-ttu-id="d4bb4-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="d4bb4-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="d4bb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="d4bb4-103">Получение свойств одной или нескольких опубликованных приложений Azure RemoteApp для коллекции.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="d4bb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4bb4-104">SYNTAX</span></span>

### <span data-ttu-id="d4bb4-105">FilterByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4bb4-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4bb4-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="d4bb4-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4bb4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4bb4-107">DESCRIPTION</span></span>
<span data-ttu-id="d4bb4-108">Командлет **Get-AzureRemoteAppProgram** извлекает свойства для одной или нескольких опубликованных приложений Azure RemoteApp для коллекции.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="d4bb4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4bb4-109">EXAMPLES</span></span>

### <span data-ttu-id="d4bb4-110">Пример 1: получение свойств программы</span><span class="sxs-lookup"><span data-stu-id="d4bb4-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="d4bb4-111">Эта команда отображает свойства удаленного приложения RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="d4bb4-112">Программа, именованное приложение "Финансы", находится в коллекции Azure RemoteApp с именем ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="d4bb4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4bb4-113">PARAMETERS</span></span>

### <span data-ttu-id="d4bb4-114">-Alias</span><span class="sxs-lookup"><span data-stu-id="d4bb4-114">-Alias</span></span>
<span data-ttu-id="d4bb4-115">Задает псевдоним программы, свойства которой требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4bb4-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d4bb4-116">-CollectionName</span></span>
<span data-ttu-id="d4bb4-117">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4bb4-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="d4bb4-118">-Profile</span></span>
<span data-ttu-id="d4bb4-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4bb4-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4bb4-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="d4bb4-121">-RemoteAppProgram</span></span>
<span data-ttu-id="d4bb4-122">Указывает имя программы, свойства которой требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d4bb4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4bb4-123">CommonParameters</span></span>
<span data-ttu-id="d4bb4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4bb4-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4bb4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4bb4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4bb4-126">INPUTS</span></span>

## <span data-ttu-id="d4bb4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4bb4-127">OUTPUTS</span></span>

## <span data-ttu-id="d4bb4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4bb4-128">NOTES</span></span>

## <span data-ttu-id="d4bb4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4bb4-129">RELATED LINKS</span></span>

[<span data-ttu-id="d4bb4-130">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="d4bb4-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="d4bb4-131">Отмена публикации — AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="d4bb4-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


