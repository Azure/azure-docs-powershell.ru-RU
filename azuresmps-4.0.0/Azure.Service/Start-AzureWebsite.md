---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075770"
---
# <span data-ttu-id="54878-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54878-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="54878-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54878-102">SYNOPSIS</span></span>
<span data-ttu-id="54878-103">Запуск указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="54878-103">Starts the specified website.</span></span>

## <span data-ttu-id="54878-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54878-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="54878-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54878-105">DESCRIPTION</span></span>
<span data-ttu-id="54878-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="54878-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="54878-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="54878-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="54878-108">Командлет **Start-AzureWebsite** запускает указанный веб-сайт, который работает в Azure.</span><span class="sxs-lookup"><span data-stu-id="54878-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="54878-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54878-109">EXAMPLES</span></span>

## <span data-ttu-id="54878-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54878-110">PARAMETERS</span></span>

### <span data-ttu-id="54878-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54878-111">-Name</span></span>
<span data-ttu-id="54878-112">Указывает имя веб-сайта, который нужно запустить.</span><span class="sxs-lookup"><span data-stu-id="54878-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="54878-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54878-113">-PassThru</span></span>
<span data-ttu-id="54878-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="54878-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="54878-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="54878-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54878-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="54878-116">-Profile</span></span>
<span data-ttu-id="54878-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="54878-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54878-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54878-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54878-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="54878-119">-Slot</span></span>
<span data-ttu-id="54878-120">Указывает имя гнезда для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="54878-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="54878-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54878-121">CommonParameters</span></span>
<span data-ttu-id="54878-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54878-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54878-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54878-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54878-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54878-124">INPUTS</span></span>

## <span data-ttu-id="54878-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54878-125">OUTPUTS</span></span>

## <span data-ttu-id="54878-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="54878-126">NOTES</span></span>

## <span data-ttu-id="54878-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54878-127">RELATED LINKS</span></span>

[<span data-ttu-id="54878-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54878-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="54878-129">Restarting-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54878-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="54878-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54878-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="54878-131">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54878-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="54878-132">Остановить-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54878-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


