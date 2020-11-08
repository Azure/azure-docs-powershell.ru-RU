---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075607"
---
# <span data-ttu-id="415e1-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="415e1-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="415e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="415e1-102">SYNOPSIS</span></span>
<span data-ttu-id="415e1-103">Получает расширение домена облачной службы Active Directory (AD), которое применяется ко всем ролям или именованным ролям в указанном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="415e1-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="415e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="415e1-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="415e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="415e1-105">DESCRIPTION</span></span>
<span data-ttu-id="415e1-106">Командлет **Get-AzureServiceADDomainExtension** получает расширение доменной службы облачных служб, которое применяется ко всем ролям или именованным ролям в указанном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="415e1-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="415e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="415e1-107">EXAMPLES</span></span>

### <span data-ttu-id="415e1-108">Пример 1: получение расширения доменной рекламы для указанной службы</span><span class="sxs-lookup"><span data-stu-id="415e1-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="415e1-109">Эта команда получает расширение доменных имен AD для службы, указанной в $Svc.</span><span class="sxs-lookup"><span data-stu-id="415e1-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="415e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="415e1-110">PARAMETERS</span></span>

### <span data-ttu-id="415e1-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="415e1-111">-InformationAction</span></span>
<span data-ttu-id="415e1-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="415e1-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="415e1-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="415e1-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="415e1-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="415e1-114">Continue</span></span>
- <span data-ttu-id="415e1-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="415e1-115">Ignore</span></span>
- <span data-ttu-id="415e1-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="415e1-116">Inquire</span></span>
- <span data-ttu-id="415e1-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="415e1-117">SilentlyContinue</span></span>
- <span data-ttu-id="415e1-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="415e1-118">Stop</span></span>
- <span data-ttu-id="415e1-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="415e1-119">Suspend</span></span>

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

### <span data-ttu-id="415e1-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="415e1-120">-InformationVariable</span></span>
<span data-ttu-id="415e1-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="415e1-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="415e1-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="415e1-122">-Profile</span></span>
<span data-ttu-id="415e1-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="415e1-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="415e1-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="415e1-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="415e1-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="415e1-125">-ServiceName</span></span>
<span data-ttu-id="415e1-126">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="415e1-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="415e1-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="415e1-127">-Slot</span></span>
<span data-ttu-id="415e1-128">Указывает среду развертывания.</span><span class="sxs-lookup"><span data-stu-id="415e1-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="415e1-129">Допустимые значения этого параметра: "производственный" или "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="415e1-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415e1-130">CommonParameters</span></span>
<span data-ttu-id="415e1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="415e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415e1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415e1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415e1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="415e1-133">INPUTS</span></span>

## <span data-ttu-id="415e1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="415e1-134">OUTPUTS</span></span>

## <span data-ttu-id="415e1-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="415e1-135">NOTES</span></span>

## <span data-ttu-id="415e1-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="415e1-136">RELATED LINKS</span></span>

[<span data-ttu-id="415e1-137">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="415e1-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="415e1-138">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="415e1-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


