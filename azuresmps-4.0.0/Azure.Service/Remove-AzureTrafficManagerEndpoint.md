---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076092"
---
# <span data-ttu-id="aeabf-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aeabf-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="aeabf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aeabf-102">SYNOPSIS</span></span>
<span data-ttu-id="aeabf-103">Удаляет конечную точку из профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="aeabf-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="aeabf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aeabf-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aeabf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeabf-105">DESCRIPTION</span></span>
<span data-ttu-id="aeabf-106">Командлет **Remove-AzureTrafficManagerEndpoint** удаляет конечную точку из профиля диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aeabf-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="aeabf-107">После удаления конечной точки передайте результат командлету **Set-AzureTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="aeabf-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aeabf-108">Этот командлет подключается к Azure, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="aeabf-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="aeabf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aeabf-109">EXAMPLES</span></span>

### <span data-ttu-id="aeabf-110">Пример 1: Удаление конечной точки из профиля</span><span class="sxs-lookup"><span data-stu-id="aeabf-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="aeabf-111">Первая команда использует командлет **Get-AzureTrafficManagerProfile** для получения профиля с именем ContosoProfile, а затем сохраняет его в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="aeabf-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="aeabf-112">Вторая команда удаляет конечную точку с доменным именем Contoso02App.cloudapp.net из профиля диспетчера трафика, который хранится в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="aeabf-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="aeabf-113">Команда передает объект Profile командлету **Set-AzureTrafficManagerProfile** для подключения к Azure, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="aeabf-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="aeabf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aeabf-114">PARAMETERS</span></span>

### <span data-ttu-id="aeabf-115">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="aeabf-115">-DomainName</span></span>
<span data-ttu-id="aeabf-116">Указывает доменное имя конечной точки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="aeabf-116">Specifies the domain name of the endpoint to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aeabf-117">-Force</span></span>
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

### <span data-ttu-id="aeabf-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="aeabf-118">-Profile</span></span>
<span data-ttu-id="aeabf-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aeabf-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="aeabf-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aeabf-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aeabf-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aeabf-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="aeabf-122">Указывает объект профиля диспетчера трафика, из которого нужно удалить конечную точку.</span><span class="sxs-lookup"><span data-stu-id="aeabf-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeabf-123">CommonParameters</span></span>
<span data-ttu-id="aeabf-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aeabf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeabf-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeabf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeabf-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aeabf-126">INPUTS</span></span>

## <span data-ttu-id="aeabf-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeabf-127">OUTPUTS</span></span>

### <span data-ttu-id="aeabf-128">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="aeabf-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="aeabf-129">Этот командлет создает объект профиля диспетчера трафика, содержащий сведения об обновленном профиле.</span><span class="sxs-lookup"><span data-stu-id="aeabf-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="aeabf-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="aeabf-130">NOTES</span></span>

## <span data-ttu-id="aeabf-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aeabf-131">RELATED LINKS</span></span>

[<span data-ttu-id="aeabf-132">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aeabf-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="aeabf-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aeabf-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="aeabf-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aeabf-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="aeabf-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aeabf-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


