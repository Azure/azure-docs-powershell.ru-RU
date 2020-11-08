---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076571"
---
# <span data-ttu-id="c69da-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="c69da-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="c69da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c69da-102">SYNOPSIS</span></span>
<span data-ttu-id="c69da-103">Получает виртуальные машины в коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c69da-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c69da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c69da-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c69da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c69da-105">DESCRIPTION</span></span>
<span data-ttu-id="c69da-106">Командлет **Get-AzureRemoteAppVM** получает виртуальные машины, созданные в коллекции Azure RemoteApp для размещения сеансов.</span><span class="sxs-lookup"><span data-stu-id="c69da-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="c69da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c69da-107">EXAMPLES</span></span>

### <span data-ttu-id="c69da-108">Пример 1: отображение виртуальных машин в коллекции</span><span class="sxs-lookup"><span data-stu-id="c69da-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="c69da-109">Эта команда отображает виртуальные машины, используемые для размещения сеансов, в коллекции Azure RemoteApp с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="c69da-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="c69da-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c69da-110">PARAMETERS</span></span>

### <span data-ttu-id="c69da-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="c69da-111">-CollectionName</span></span>
<span data-ttu-id="c69da-112">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c69da-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69da-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="c69da-113">-Profile</span></span>
<span data-ttu-id="c69da-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c69da-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c69da-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c69da-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c69da-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69da-116">CommonParameters</span></span>
<span data-ttu-id="c69da-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c69da-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69da-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69da-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69da-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c69da-119">INPUTS</span></span>

## <span data-ttu-id="c69da-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c69da-120">OUTPUTS</span></span>

## <span data-ttu-id="c69da-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="c69da-121">NOTES</span></span>

## <span data-ttu-id="c69da-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c69da-122">RELATED LINKS</span></span>

[<span data-ttu-id="c69da-123">Restarting-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="c69da-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


