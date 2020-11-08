---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076315"
---
# <span data-ttu-id="73bf3-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="73bf3-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="73bf3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="73bf3-103">Список программ меню "Пуск" в коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="73bf3-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="73bf3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73bf3-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73bf3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="73bf3-106">Командлет **Get-AzureRemoteAppStartMenuProgram** перечисляет программы меню "Пуск" в образе шаблона, используемом коллекцией RemoteApp в Azure.</span><span class="sxs-lookup"><span data-stu-id="73bf3-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="73bf3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="73bf3-108">Пример 1: список программ меню "Пуск" для коллекции</span><span class="sxs-lookup"><span data-stu-id="73bf3-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="73bf3-109">Эта команда возвращает список программ меню "Пуск" для коллекции ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="73bf3-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="73bf3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73bf3-110">PARAMETERS</span></span>

### <span data-ttu-id="73bf3-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="73bf3-111">-CollectionName</span></span>
<span data-ttu-id="73bf3-112">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="73bf3-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="73bf3-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="73bf3-113">-Profile</span></span>
<span data-ttu-id="73bf3-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="73bf3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73bf3-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73bf3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73bf3-116">-ProgramName</span><span class="sxs-lookup"><span data-stu-id="73bf3-116">-ProgramName</span></span>
<span data-ttu-id="73bf3-117">Указывает имя программы, сведения о которой требуется вывести.</span><span class="sxs-lookup"><span data-stu-id="73bf3-117">Specifies the name of a program for which to list information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="73bf3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bf3-118">CommonParameters</span></span>
<span data-ttu-id="73bf3-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73bf3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bf3-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bf3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bf3-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73bf3-121">INPUTS</span></span>

## <span data-ttu-id="73bf3-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73bf3-122">OUTPUTS</span></span>

## <span data-ttu-id="73bf3-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="73bf3-123">NOTES</span></span>

## <span data-ttu-id="73bf3-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73bf3-124">RELATED LINKS</span></span>

[<span data-ttu-id="73bf3-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="73bf3-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


