---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076244"
---
# <span data-ttu-id="e2406-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e2406-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="e2406-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2406-102">SYNOPSIS</span></span>
<span data-ttu-id="e2406-103">Заменяет развертывания между производственными и промежуточными.</span><span class="sxs-lookup"><span data-stu-id="e2406-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="e2406-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2406-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e2406-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2406-105">DESCRIPTION</span></span>
<span data-ttu-id="e2406-106">Командлет **Move-AzureDeployment** заменяет виртуальные IP-адреса развертываний в среде производства и промежуточных сред.</span><span class="sxs-lookup"><span data-stu-id="e2406-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="e2406-107">Этот командлет заменяет развертывание, которое в настоящее время выполняется в промежуточной среде, в производственную среду и развертывание, работающее в производственной среде, в промежуточную среду.</span><span class="sxs-lookup"><span data-stu-id="e2406-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="e2406-108">Если в промежуточной среде есть развертывание и отсутствует развертывание в рабочей среде, командлет переместит развертывание в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="e2406-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="e2406-109">При развертывании в рабочей среде и отсутствии развертывания в промежуточной среде командлет завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="e2406-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="e2406-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2406-110">EXAMPLES</span></span>

### <span data-ttu-id="e2406-111">Пример 1: переключение развертываний для службы</span><span class="sxs-lookup"><span data-stu-id="e2406-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="e2406-112">Эта команда заменяет развертывания службы с именем ContosoService между производственными и промежуточными средами.</span><span class="sxs-lookup"><span data-stu-id="e2406-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="e2406-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2406-113">PARAMETERS</span></span>

### <span data-ttu-id="e2406-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e2406-114">-InformationAction</span></span>
<span data-ttu-id="e2406-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="e2406-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e2406-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e2406-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2406-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="e2406-117">Continue</span></span>
- <span data-ttu-id="e2406-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="e2406-118">Ignore</span></span>
- <span data-ttu-id="e2406-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="e2406-119">Inquire</span></span>
- <span data-ttu-id="e2406-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e2406-120">SilentlyContinue</span></span>
- <span data-ttu-id="e2406-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="e2406-121">Stop</span></span>
- <span data-ttu-id="e2406-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="e2406-122">Suspend</span></span>

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

### <span data-ttu-id="e2406-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e2406-123">-InformationVariable</span></span>
<span data-ttu-id="e2406-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="e2406-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e2406-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="e2406-125">-Profile</span></span>
<span data-ttu-id="e2406-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e2406-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2406-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2406-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2406-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e2406-128">-ServiceName</span></span>
<span data-ttu-id="e2406-129">Указывает имя службы, для которой этот командлет заменяет производственные и промежуточные развертывания.</span><span class="sxs-lookup"><span data-stu-id="e2406-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="e2406-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2406-130">CommonParameters</span></span>
<span data-ttu-id="e2406-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2406-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2406-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2406-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2406-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2406-133">INPUTS</span></span>

## <span data-ttu-id="e2406-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2406-134">OUTPUTS</span></span>

### <span data-ttu-id="e2406-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e2406-135">ManagementOperationContext</span></span>

## <span data-ttu-id="e2406-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2406-136">NOTES</span></span>

## <span data-ttu-id="e2406-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2406-137">RELATED LINKS</span></span>

[<span data-ttu-id="e2406-138">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e2406-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="e2406-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="e2406-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="e2406-140">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e2406-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="e2406-141">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e2406-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="e2406-142">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e2406-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


