---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7E1A3988-CEEA-49E1-B6F4-1EFA39E170C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06cc64eb67f1e338ff5be28712d1c183bfefd5ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076588"
---
# <span data-ttu-id="2198d-101">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2198d-101">Stop-AzureWebsite</span></span>

## <span data-ttu-id="2198d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2198d-102">SYNOPSIS</span></span>
<span data-ttu-id="2198d-103">Остановка указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="2198d-103">Stops the specified website.</span></span>

## <span data-ttu-id="2198d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2198d-104">SYNTAX</span></span>

```
Stop-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2198d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2198d-105">DESCRIPTION</span></span>
<span data-ttu-id="2198d-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2198d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2198d-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2198d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2198d-108">Командлет **Stop-AzureWebsite** останавливает указанный веб-сайт, размещенный в Azure.</span><span class="sxs-lookup"><span data-stu-id="2198d-108">The **Stop-AzureWebsite** cmdlet stops the specified website hosted in Azure.</span></span>

## <span data-ttu-id="2198d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2198d-109">EXAMPLES</span></span>

## <span data-ttu-id="2198d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2198d-110">PARAMETERS</span></span>

### <span data-ttu-id="2198d-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2198d-111">-Name</span></span>
<span data-ttu-id="2198d-112">Указывает имя веб-сайта, который нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="2198d-112">Specifies the name of the website to stop.</span></span>

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

### <span data-ttu-id="2198d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2198d-113">-PassThru</span></span>
<span data-ttu-id="2198d-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2198d-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2198d-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2198d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2198d-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="2198d-116">-Profile</span></span>
<span data-ttu-id="2198d-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2198d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2198d-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2198d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2198d-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="2198d-119">-Slot</span></span>
<span data-ttu-id="2198d-120">Указывает имя гнезда для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="2198d-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="2198d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2198d-121">CommonParameters</span></span>
<span data-ttu-id="2198d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2198d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2198d-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2198d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2198d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2198d-124">INPUTS</span></span>

## <span data-ttu-id="2198d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2198d-125">OUTPUTS</span></span>

## <span data-ttu-id="2198d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="2198d-126">NOTES</span></span>

## <span data-ttu-id="2198d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2198d-127">RELATED LINKS</span></span>

[<span data-ttu-id="2198d-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2198d-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="2198d-129">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2198d-129">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


