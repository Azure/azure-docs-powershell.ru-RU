---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075884"
---
# <span data-ttu-id="3d011-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="3d011-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="3d011-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d011-102">SYNOPSIS</span></span>
<span data-ttu-id="3d011-103">Публикация удаленного приложения RemoteApp для Azure.</span><span class="sxs-lookup"><span data-stu-id="3d011-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="3d011-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d011-104">SYNTAX</span></span>

### <span data-ttu-id="3d011-105">Идентификатор приложения (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d011-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d011-106">Путь к приложению</span><span class="sxs-lookup"><span data-stu-id="3d011-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d011-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d011-107">DESCRIPTION</span></span>
<span data-ttu-id="3d011-108">Командлет **Publish-AzureRemoteAppProgram** публикует приложение Azure RemoteApp, которое становится доступным для пользователей коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3d011-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3d011-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d011-109">EXAMPLES</span></span>

### <span data-ttu-id="3d011-110">Пример 1: публикация программы в коллекции</span><span class="sxs-lookup"><span data-stu-id="3d011-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="3d011-111">Эта команда публикует программу в коллекции ContosoApps с указанным *StartMenuAppId* , чтобы добавить программу в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="3d011-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="3d011-112">Опубликованное приложение будет иметь отображаемое имя "Finance App".</span><span class="sxs-lookup"><span data-stu-id="3d011-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="3d011-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d011-113">PARAMETERS</span></span>

### <span data-ttu-id="3d011-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3d011-114">-CollectionName</span></span>
<span data-ttu-id="3d011-115">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3d011-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="3d011-116">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="3d011-116">-CommandLine</span></span>
<span data-ttu-id="3d011-117">Задает аргументы командной строки для программы, публикуемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3d011-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="3d011-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3d011-118">-DisplayName</span></span>
<span data-ttu-id="3d011-119">Указывает понятное имя, отображаемое пользователем Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3d011-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="3d011-120">Пользователи видят это имя приложения.</span><span class="sxs-lookup"><span data-stu-id="3d011-120">Users see this as the name of the application.</span></span>

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

### <span data-ttu-id="3d011-121">-FileVirtualPath</span><span class="sxs-lookup"><span data-stu-id="3d011-121">-FileVirtualPath</span></span>
<span data-ttu-id="3d011-122">Указывает путь программы в образе шаблона программы.</span><span class="sxs-lookup"><span data-stu-id="3d011-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d011-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d011-123">-Profile</span></span>
<span data-ttu-id="3d011-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d011-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d011-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d011-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d011-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="3d011-126">-StartMenuAppId</span></span>
<span data-ttu-id="3d011-127">Указывает идентификатор GUID, который используется этим командлетом для добавления программы в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="3d011-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d011-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d011-128">CommonParameters</span></span>
<span data-ttu-id="3d011-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d011-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d011-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d011-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d011-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d011-131">INPUTS</span></span>

## <span data-ttu-id="3d011-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d011-132">OUTPUTS</span></span>

## <span data-ttu-id="3d011-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d011-133">NOTES</span></span>

## <span data-ttu-id="3d011-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d011-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d011-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="3d011-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="3d011-136">Отмена публикации — AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="3d011-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


