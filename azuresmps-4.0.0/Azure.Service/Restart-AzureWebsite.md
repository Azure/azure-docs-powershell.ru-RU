---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075470"
---
# <span data-ttu-id="2f961-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2f961-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="2f961-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f961-102">SYNOPSIS</span></span>
<span data-ttu-id="2f961-103">Останавливает и перезапускает указанный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="2f961-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="2f961-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f961-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f961-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f961-105">DESCRIPTION</span></span>
<span data-ttu-id="2f961-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f961-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2f961-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2f961-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2f961-108">Командлет **restart-AzureWebsite** останавливает и перезапускает указанный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="2f961-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="2f961-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f961-109">EXAMPLES</span></span>

### <span data-ttu-id="2f961-110">Пример 1: перезагрузка веб-сайта</span><span class="sxs-lookup"><span data-stu-id="2f961-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="2f961-111">В этом примере перезапускается веб-сайт с именем MyWebsite.</span><span class="sxs-lookup"><span data-stu-id="2f961-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="2f961-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f961-112">PARAMETERS</span></span>

### <span data-ttu-id="2f961-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f961-113">-Name</span></span>
<span data-ttu-id="2f961-114">Указывает имя веб-сайта Azure для перезапуска.</span><span class="sxs-lookup"><span data-stu-id="2f961-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="2f961-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f961-115">-PassThru</span></span>
<span data-ttu-id="2f961-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2f961-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f961-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2f961-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f961-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="2f961-118">-Profile</span></span>
<span data-ttu-id="2f961-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f961-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f961-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f961-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f961-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="2f961-121">-Slot</span></span>
<span data-ttu-id="2f961-122">Указывает имя гнезда для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="2f961-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="2f961-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f961-123">CommonParameters</span></span>
<span data-ttu-id="2f961-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f961-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f961-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f961-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f961-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f961-126">INPUTS</span></span>

## <span data-ttu-id="2f961-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f961-127">OUTPUTS</span></span>

## <span data-ttu-id="2f961-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f961-128">NOTES</span></span>

## <span data-ttu-id="2f961-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f961-129">RELATED LINKS</span></span>

[<span data-ttu-id="2f961-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2f961-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="2f961-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2f961-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="2f961-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2f961-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="2f961-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2f961-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


