---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076091"
---
# <span data-ttu-id="c6aff-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6aff-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="c6aff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6aff-102">SYNOPSIS</span></span>
<span data-ttu-id="c6aff-103">Удаление профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="c6aff-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="c6aff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6aff-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6aff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6aff-105">DESCRIPTION</span></span>
<span data-ttu-id="c6aff-106">Командлет **Remove-AzureTrafficManagerProfile** удаляет профиль диспетчера трафика Microsoft Azure из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c6aff-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="c6aff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6aff-107">EXAMPLES</span></span>

### <span data-ttu-id="c6aff-108">Пример 1: Удаление профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="c6aff-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="c6aff-109">Эта команда удаляет профиль диспетчера трафика с именем отобразите.</span><span class="sxs-lookup"><span data-stu-id="c6aff-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="c6aff-110">Пример 2: Удаление профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="c6aff-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="c6aff-111">Эта команда удаляет профиль диспетчера трафика с именем отобразите без запроса подтверждения и возвращает результаты.</span><span class="sxs-lookup"><span data-stu-id="c6aff-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="c6aff-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6aff-112">PARAMETERS</span></span>

### <span data-ttu-id="c6aff-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c6aff-113">-Force</span></span>
<span data-ttu-id="c6aff-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6aff-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c6aff-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6aff-115">-Name</span></span>
<span data-ttu-id="c6aff-116">Указывает имя профиля диспетчера трафика, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c6aff-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="c6aff-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6aff-117">-PassThru</span></span>
<span data-ttu-id="c6aff-118">Возвращает $True, если операция выполнена успешно. в противном случае $False.</span><span class="sxs-lookup"><span data-stu-id="c6aff-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="c6aff-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c6aff-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6aff-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="c6aff-120">-Profile</span></span>
<span data-ttu-id="c6aff-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c6aff-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c6aff-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6aff-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6aff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6aff-123">CommonParameters</span></span>
<span data-ttu-id="c6aff-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6aff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6aff-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6aff-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6aff-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6aff-126">INPUTS</span></span>

## <span data-ttu-id="c6aff-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6aff-127">OUTPUTS</span></span>

### <span data-ttu-id="c6aff-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6aff-128">System.Boolean</span></span>
<span data-ttu-id="c6aff-129">Этот командлет создает $True или $False.</span><span class="sxs-lookup"><span data-stu-id="c6aff-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="c6aff-130">Если операция выполнена успешно и вы указываете параметр *PassThru* , этот командлет возвращает значение $true.</span><span class="sxs-lookup"><span data-stu-id="c6aff-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="c6aff-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6aff-131">NOTES</span></span>

## <span data-ttu-id="c6aff-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6aff-132">RELATED LINKS</span></span>

[<span data-ttu-id="c6aff-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6aff-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c6aff-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6aff-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c6aff-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6aff-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c6aff-136">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6aff-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c6aff-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6aff-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


