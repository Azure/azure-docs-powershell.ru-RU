---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076579"
---
# <span data-ttu-id="62c12-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="62c12-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="62c12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62c12-102">SYNOPSIS</span></span>
<span data-ttu-id="62c12-103">Получение сведений об изображениях шаблонов Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="62c12-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="62c12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62c12-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="62c12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62c12-105">DESCRIPTION</span></span>
<span data-ttu-id="62c12-106">Командлет **Get-AzureRemoteAppTemplateImage** извлекает сведения об изображениях шаблонов Azure RemoteApp в Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="62c12-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="62c12-107">Этот командлет возвращает объект, содержащий сведения об указанном изображении шаблона.</span><span class="sxs-lookup"><span data-stu-id="62c12-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="62c12-108">Если вы не указали изображение шаблона, оно извлекает сведения обо всех его изображениях в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="62c12-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="62c12-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62c12-109">EXAMPLES</span></span>

### <span data-ttu-id="62c12-110">Пример 1: получение списка всех изображений шаблонов</span><span class="sxs-lookup"><span data-stu-id="62c12-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="62c12-111">Эта команда возвращает список всех изображений шаблонов.</span><span class="sxs-lookup"><span data-stu-id="62c12-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="62c12-112">Пример 2: получение сведений об указанном образе шаблона</span><span class="sxs-lookup"><span data-stu-id="62c12-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="62c12-113">Эта команда извлекает сведения об изображении шаблона с именем ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="62c12-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="62c12-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62c12-114">PARAMETERS</span></span>

### <span data-ttu-id="62c12-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="62c12-115">-ImageName</span></span>
<span data-ttu-id="62c12-116">Указывает имя образа шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="62c12-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="62c12-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="62c12-117">-Profile</span></span>
<span data-ttu-id="62c12-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="62c12-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62c12-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62c12-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62c12-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c12-120">CommonParameters</span></span>
<span data-ttu-id="62c12-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62c12-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c12-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c12-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c12-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62c12-123">INPUTS</span></span>

## <span data-ttu-id="62c12-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62c12-124">OUTPUTS</span></span>

## <span data-ttu-id="62c12-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="62c12-125">NOTES</span></span>

## <span data-ttu-id="62c12-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62c12-126">RELATED LINKS</span></span>

[<span data-ttu-id="62c12-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="62c12-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="62c12-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="62c12-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


