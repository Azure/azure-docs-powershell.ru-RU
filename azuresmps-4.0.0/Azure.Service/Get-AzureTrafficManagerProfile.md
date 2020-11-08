---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075536"
---
# <span data-ttu-id="2deaf-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2deaf-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="2deaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2deaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2deaf-103">Получает сведения о профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="2deaf-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="2deaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2deaf-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2deaf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2deaf-105">DESCRIPTION</span></span>
<span data-ttu-id="2deaf-106">Командлет **Get-AzureTrafficManagerProfile** получает сведения о профиле диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2deaf-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2deaf-107">Если параметр *Name* не указан, командлет выводит список профилей диспетчера трафика в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2deaf-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="2deaf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2deaf-108">EXAMPLES</span></span>

### <span data-ttu-id="2deaf-109">Пример 1: получение списка профилей диспетчера трафика в подписке</span><span class="sxs-lookup"><span data-stu-id="2deaf-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="2deaf-110">Эта команда получает список профилей диспетчера трафика в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="2deaf-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="2deaf-111">Пример 2: получение профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="2deaf-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="2deaf-112">Эта команда получает профиль диспетчера трафика с именем отобразите.</span><span class="sxs-lookup"><span data-stu-id="2deaf-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="2deaf-113">Пример 3: Добавление конечной точки в профиль диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="2deaf-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="2deaf-114">Эта команда добавляет конечную точку к профилю диспетчера трафика, а затем сохраняет профиль.</span><span class="sxs-lookup"><span data-stu-id="2deaf-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="2deaf-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2deaf-115">PARAMETERS</span></span>

### <span data-ttu-id="2deaf-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2deaf-116">-Name</span></span>
<span data-ttu-id="2deaf-117">Указывает имя профиля диспетчера трафика, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2deaf-117">Specifies the name of the Traffic Manager profile to get.</span></span>

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

### <span data-ttu-id="2deaf-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="2deaf-118">-Profile</span></span>
<span data-ttu-id="2deaf-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2deaf-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2deaf-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2deaf-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2deaf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2deaf-121">CommonParameters</span></span>
<span data-ttu-id="2deaf-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2deaf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2deaf-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2deaf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2deaf-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2deaf-124">INPUTS</span></span>

## <span data-ttu-id="2deaf-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2deaf-125">OUTPUTS</span></span>

### <span data-ttu-id="2deaf-126">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="2deaf-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="2deaf-127">Этот командлет создает объект или объекты профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="2deaf-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="2deaf-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2deaf-128">NOTES</span></span>

## <span data-ttu-id="2deaf-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2deaf-129">RELATED LINKS</span></span>

[<span data-ttu-id="2deaf-130">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2deaf-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="2deaf-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2deaf-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2deaf-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2deaf-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2deaf-133">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2deaf-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2deaf-134">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2deaf-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2deaf-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2deaf-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


