---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076309"
---
# <span data-ttu-id="7c077-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="7c077-101">Get-AzureService</span></span>

## <span data-ttu-id="7c077-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c077-102">SYNOPSIS</span></span>
<span data-ttu-id="7c077-103">Возвращает объект со сведениями о облачных службах для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="7c077-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="7c077-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c077-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7c077-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c077-105">DESCRIPTION</span></span>
<span data-ttu-id="7c077-106">Командлет **Get-AzureService** возвращает объект List со всеми облачными службами Azure, связанными с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="7c077-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="7c077-107">Если указан параметр *ServiceName* , **Get-AzureService** возвращает сведения только о соответствующей службе.</span><span class="sxs-lookup"><span data-stu-id="7c077-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="7c077-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c077-108">EXAMPLES</span></span>

### <span data-ttu-id="7c077-109">Пример 1: получение сведений обо всех службах</span><span class="sxs-lookup"><span data-stu-id="7c077-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="7c077-110">Эта команда возвращает объект, содержащий сведения обо всех службах Azure, связанных с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="7c077-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="7c077-111">Пример 2: получение сведений об указанной службе</span><span class="sxs-lookup"><span data-stu-id="7c077-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="7c077-112">Эта команда возвращает сведения о службе $MySvc.</span><span class="sxs-lookup"><span data-stu-id="7c077-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="7c077-113">Пример 3: Отображение доступных методов и свойств</span><span class="sxs-lookup"><span data-stu-id="7c077-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="7c077-114">Эта команда отображает свойства и методы, доступные из командлета **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="7c077-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="7c077-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c077-115">PARAMETERS</span></span>

### <span data-ttu-id="7c077-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7c077-116">-InformationAction</span></span>
<span data-ttu-id="7c077-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="7c077-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7c077-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7c077-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c077-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="7c077-119">Continue</span></span>
- <span data-ttu-id="7c077-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="7c077-120">Ignore</span></span>
- <span data-ttu-id="7c077-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="7c077-121">Inquire</span></span>
- <span data-ttu-id="7c077-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7c077-122">SilentlyContinue</span></span>
- <span data-ttu-id="7c077-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="7c077-123">Stop</span></span>
- <span data-ttu-id="7c077-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="7c077-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c077-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7c077-125">-InformationVariable</span></span>
<span data-ttu-id="7c077-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="7c077-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c077-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="7c077-127">-Profile</span></span>
<span data-ttu-id="7c077-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7c077-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c077-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c077-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c077-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c077-130">-ServiceName</span></span>
<span data-ttu-id="7c077-131">Указывает имя службы, для которой требуется возвратить сведения.</span><span class="sxs-lookup"><span data-stu-id="7c077-131">Specifies the name of a service on which to return information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c077-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c077-132">CommonParameters</span></span>
<span data-ttu-id="7c077-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c077-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c077-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c077-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c077-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c077-135">INPUTS</span></span>

## <span data-ttu-id="7c077-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c077-136">OUTPUTS</span></span>

### <span data-ttu-id="7c077-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="7c077-137">HostedServiceContext</span></span>

## <span data-ttu-id="7c077-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c077-138">NOTES</span></span>

## <span data-ttu-id="7c077-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c077-139">RELATED LINKS</span></span>

[<span data-ttu-id="7c077-140">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="7c077-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="7c077-141">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="7c077-141">Set-AzureService</span></span>](./Set-AzureService.md)


