---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076340"
---
# <span data-ttu-id="742c1-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="742c1-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="742c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="742c1-102">SYNOPSIS</span></span>
<span data-ttu-id="742c1-103">Получает сведения о конфигурации внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="742c1-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="742c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="742c1-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="742c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="742c1-105">DESCRIPTION</span></span>
<span data-ttu-id="742c1-106">Командлет **Get-AzureInternalLoadBalancer** получает сведения о конфигурации внутренней подсистемы балансировки нагрузки для службы Azure.</span><span class="sxs-lookup"><span data-stu-id="742c1-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="742c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="742c1-107">EXAMPLES</span></span>

### <span data-ttu-id="742c1-108">Пример 1: получение сведений для внутренней подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="742c1-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="742c1-109">Эта команда получает службу с именем ContosoService с помощью командлета **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="742c1-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="742c1-110">Команда передает эту службу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="742c1-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="742c1-111">Текущий командлет получает сведения о внутренней подсистеме балансировки нагрузки для этой службы.</span><span class="sxs-lookup"><span data-stu-id="742c1-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="742c1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="742c1-112">PARAMETERS</span></span>

### <span data-ttu-id="742c1-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="742c1-113">-InformationAction</span></span>
<span data-ttu-id="742c1-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="742c1-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="742c1-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="742c1-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="742c1-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="742c1-116">Continue</span></span>
- <span data-ttu-id="742c1-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="742c1-117">Ignore</span></span>
- <span data-ttu-id="742c1-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="742c1-118">Inquire</span></span>
- <span data-ttu-id="742c1-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="742c1-119">SilentlyContinue</span></span>
- <span data-ttu-id="742c1-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="742c1-120">Stop</span></span>
- <span data-ttu-id="742c1-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="742c1-121">Suspend</span></span>

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

### <span data-ttu-id="742c1-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="742c1-122">-InformationVariable</span></span>
<span data-ttu-id="742c1-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="742c1-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="742c1-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="742c1-124">-Profile</span></span>
<span data-ttu-id="742c1-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="742c1-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="742c1-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="742c1-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="742c1-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="742c1-127">-ServiceName</span></span>
<span data-ttu-id="742c1-128">Указывает имя службы, для которой этот командлет получает данные для внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="742c1-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742c1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742c1-129">CommonParameters</span></span>
<span data-ttu-id="742c1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="742c1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742c1-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742c1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742c1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="742c1-132">INPUTS</span></span>

## <span data-ttu-id="742c1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="742c1-133">OUTPUTS</span></span>

### <span data-ttu-id="742c1-134">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. InternalLoadBalancerContext</span><span class="sxs-lookup"><span data-stu-id="742c1-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="742c1-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="742c1-135">NOTES</span></span>

## <span data-ttu-id="742c1-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="742c1-136">RELATED LINKS</span></span>

[<span data-ttu-id="742c1-137">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="742c1-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="742c1-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="742c1-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="742c1-139">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="742c1-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="742c1-140">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="742c1-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="742c1-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="742c1-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


