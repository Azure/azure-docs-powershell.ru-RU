---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076455"
---
# <span data-ttu-id="c9992-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c9992-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="c9992-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9992-102">SYNOPSIS</span></span>
<span data-ttu-id="c9992-103">Удаляет существующий экземпляр надстройки.</span><span class="sxs-lookup"><span data-stu-id="c9992-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="c9992-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9992-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c9992-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9992-105">DESCRIPTION</span></span>
<span data-ttu-id="c9992-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9992-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c9992-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c9992-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c9992-108">Удаляет существующий экземпляр надстройки из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c9992-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="c9992-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9992-109">EXAMPLES</span></span>

### <span data-ttu-id="c9992-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9992-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="c9992-111">В этом примере удаляется надстройка с именем MyAddOn из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c9992-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="c9992-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9992-112">PARAMETERS</span></span>

### <span data-ttu-id="c9992-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9992-113">-Name</span></span>
<span data-ttu-id="c9992-114">Указывает имя удаляемого экземпляра надстройки.</span><span class="sxs-lookup"><span data-stu-id="c9992-114">Specifies the name of the add-on instance to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9992-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9992-115">-PassThru</span></span>
<span data-ttu-id="c9992-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c9992-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c9992-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c9992-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9992-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9992-118">-Profile</span></span>
<span data-ttu-id="c9992-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c9992-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9992-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9992-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9992-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9992-121">CommonParameters</span></span>
<span data-ttu-id="c9992-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9992-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9992-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9992-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9992-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9992-124">INPUTS</span></span>

## <span data-ttu-id="c9992-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9992-125">OUTPUTS</span></span>

## <span data-ttu-id="c9992-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9992-126">NOTES</span></span>

## <span data-ttu-id="c9992-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9992-127">RELATED LINKS</span></span>

[<span data-ttu-id="c9992-128">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c9992-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="c9992-129">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c9992-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="c9992-130">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c9992-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


