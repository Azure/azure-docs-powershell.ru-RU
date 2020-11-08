---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076375"
---
# <span data-ttu-id="2ea76-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ea76-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="2ea76-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ea76-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea76-103">Включает профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="2ea76-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="2ea76-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ea76-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ea76-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ea76-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea76-106">Командлет **Enable-AzureTrafficManagerProfile** включает профиль диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea76-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2ea76-107">Укажите параметр *PassThru* , чтобы показать, выполняется ли операция успешно.</span><span class="sxs-lookup"><span data-stu-id="2ea76-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="2ea76-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ea76-108">EXAMPLES</span></span>

### <span data-ttu-id="2ea76-109">Пример 1: включение профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="2ea76-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="2ea76-110">Эта команда включает профиль диспетчера трафика с именем отобразите.</span><span class="sxs-lookup"><span data-stu-id="2ea76-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="2ea76-111">Пример 2: включение профиля диспетчера трафика и отображение результатов</span><span class="sxs-lookup"><span data-stu-id="2ea76-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="2ea76-112">Эта команда включает профиль диспетчера трафика с именем отобразите и показывает, успешно ли была выполнена команда.</span><span class="sxs-lookup"><span data-stu-id="2ea76-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="2ea76-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ea76-113">PARAMETERS</span></span>

### <span data-ttu-id="2ea76-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ea76-114">-Name</span></span>
<span data-ttu-id="2ea76-115">Указывает имя профиля диспетчера трафика для включения.</span><span class="sxs-lookup"><span data-stu-id="2ea76-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="2ea76-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ea76-116">-PassThru</span></span>
<span data-ttu-id="2ea76-117">Возвращает $True, если операция выполнена успешно. в противном случае $False.</span><span class="sxs-lookup"><span data-stu-id="2ea76-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="2ea76-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2ea76-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ea76-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="2ea76-119">-Profile</span></span>
<span data-ttu-id="2ea76-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2ea76-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2ea76-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ea76-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ea76-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea76-122">CommonParameters</span></span>
<span data-ttu-id="2ea76-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ea76-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea76-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea76-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea76-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ea76-125">INPUTS</span></span>

## <span data-ttu-id="2ea76-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ea76-126">OUTPUTS</span></span>

### <span data-ttu-id="2ea76-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ea76-127">System.Boolean</span></span>
<span data-ttu-id="2ea76-128">Этот командлет создает $True или $False.</span><span class="sxs-lookup"><span data-stu-id="2ea76-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="2ea76-129">Если операция выполнена успешно и вы указываете параметр *PassThru* , этот командлет возвращает значение $true.</span><span class="sxs-lookup"><span data-stu-id="2ea76-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="2ea76-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ea76-130">NOTES</span></span>

## <span data-ttu-id="2ea76-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ea76-131">RELATED LINKS</span></span>

[<span data-ttu-id="2ea76-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ea76-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2ea76-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ea76-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2ea76-134">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ea76-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2ea76-135">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ea76-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2ea76-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ea76-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


