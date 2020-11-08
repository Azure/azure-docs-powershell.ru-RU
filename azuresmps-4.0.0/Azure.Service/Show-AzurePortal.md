---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075948"
---
# <span data-ttu-id="c7e80-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="c7e80-101">Show-AzurePortal</span></span>

## <span data-ttu-id="c7e80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7e80-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e80-103">Показать портал управления Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e80-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="c7e80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7e80-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7e80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7e80-105">DESCRIPTION</span></span>
<span data-ttu-id="c7e80-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c7e80-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c7e80-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c7e80-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c7e80-108">Командлет **Show-AzurePortal** показывает портал управления Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e80-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="c7e80-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7e80-109">EXAMPLES</span></span>

### <span data-ttu-id="c7e80-110">Пример 1: отображение сведений о веб-сайте</span><span class="sxs-lookup"><span data-stu-id="c7e80-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="c7e80-111">В этом примере открывается браузер на портале Azure, в котором отображаются сведения о веб-сайте с именем "мой сайт".</span><span class="sxs-lookup"><span data-stu-id="c7e80-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="c7e80-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7e80-112">PARAMETERS</span></span>

### <span data-ttu-id="c7e80-113">-Environment</span><span class="sxs-lookup"><span data-stu-id="c7e80-113">-Environment</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7e80-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7e80-114">-Name</span></span>
<span data-ttu-id="c7e80-115">Указывает имя веб-сайта, который будет отображаться на портале.</span><span class="sxs-lookup"><span data-stu-id="c7e80-115">Specifies the name of the website to show in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7e80-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="c7e80-116">-Profile</span></span>
<span data-ttu-id="c7e80-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c7e80-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7e80-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7e80-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7e80-119">-Realm</span><span class="sxs-lookup"><span data-stu-id="c7e80-119">-Realm</span></span>
<span data-ttu-id="c7e80-120">Указывает идентификатор организации, который будет использоваться для федеративной проверки подлинности при отображении портала Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e80-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7e80-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e80-121">CommonParameters</span></span>
<span data-ttu-id="c7e80-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7e80-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e80-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e80-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e80-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7e80-124">INPUTS</span></span>

## <span data-ttu-id="c7e80-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7e80-125">OUTPUTS</span></span>

## <span data-ttu-id="c7e80-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7e80-126">NOTES</span></span>

## <span data-ttu-id="c7e80-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7e80-127">RELATED LINKS</span></span>

[<span data-ttu-id="c7e80-128">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c7e80-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


