---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075650"
---
# <span data-ttu-id="9cf81-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="9cf81-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="9cf81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cf81-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf81-103">Получение сведений о событиях, которые Azure инициирует для виртуальных машин и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="9cf81-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="9cf81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cf81-104">SYNTAX</span></span>

### <span data-ttu-id="9cf81-105">GetDeploymentEventBySlot (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9cf81-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9cf81-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="9cf81-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9cf81-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cf81-107">DESCRIPTION</span></span>
<span data-ttu-id="9cf81-108">Командлет **Get-AzureDeploymentEvent** получает сведения о событиях, которые Azure инициирует, чтобы влиять на виртуальные машины и облачные службы.</span><span class="sxs-lookup"><span data-stu-id="9cf81-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="9cf81-109">Эти события включают запланированные события обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9cf81-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="9cf81-110">Этот командлет возвращает список событий, которые определяют влияние экземпляра роли или виртуальной машины, причины воздействия и время начала события.</span><span class="sxs-lookup"><span data-stu-id="9cf81-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="9cf81-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cf81-111">EXAMPLES</span></span>

### <span data-ttu-id="9cf81-112">1:</span><span class="sxs-lookup"><span data-stu-id="9cf81-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="9cf81-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cf81-113">PARAMETERS</span></span>

### <span data-ttu-id="9cf81-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9cf81-114">-DeploymentName</span></span>
<span data-ttu-id="9cf81-115">Указывает имя развертывания, для которого этот командлет получает события.</span><span class="sxs-lookup"><span data-stu-id="9cf81-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9cf81-116">-EndTime</span></span>
<span data-ttu-id="9cf81-117">Указывает время окончания запланированных событий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cf81-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9cf81-118">-InformationAction</span></span>
<span data-ttu-id="9cf81-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="9cf81-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9cf81-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9cf81-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9cf81-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="9cf81-121">Continue</span></span>
- <span data-ttu-id="9cf81-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="9cf81-122">Ignore</span></span>
- <span data-ttu-id="9cf81-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="9cf81-123">Inquire</span></span>
- <span data-ttu-id="9cf81-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9cf81-124">SilentlyContinue</span></span>
- <span data-ttu-id="9cf81-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="9cf81-125">Stop</span></span>
- <span data-ttu-id="9cf81-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="9cf81-126">Suspend</span></span>

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

### <span data-ttu-id="9cf81-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9cf81-127">-InformationVariable</span></span>
<span data-ttu-id="9cf81-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="9cf81-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9cf81-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="9cf81-129">-Profile</span></span>
<span data-ttu-id="9cf81-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cf81-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9cf81-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9cf81-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9cf81-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9cf81-132">-ServiceName</span></span>
<span data-ttu-id="9cf81-133">Указывает имя размещенной службы, для которой этот командлет получает запланированные события.</span><span class="sxs-lookup"><span data-stu-id="9cf81-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

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

### <span data-ttu-id="9cf81-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="9cf81-134">-Slot</span></span>
<span data-ttu-id="9cf81-135">Указывает среду развертывания, для которой этот командлет получает запланированные события.</span><span class="sxs-lookup"><span data-stu-id="9cf81-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="9cf81-136">Допустимые значения: промежуточные и производственные.</span><span class="sxs-lookup"><span data-stu-id="9cf81-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="9cf81-137">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="9cf81-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9cf81-138">-StartTime</span></span>
<span data-ttu-id="9cf81-139">Указывает время начала запланированных событий, которое этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="9cf81-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf81-140">CommonParameters</span></span>
<span data-ttu-id="9cf81-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cf81-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf81-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf81-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf81-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cf81-143">INPUTS</span></span>

## <span data-ttu-id="9cf81-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cf81-144">OUTPUTS</span></span>

## <span data-ttu-id="9cf81-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cf81-145">NOTES</span></span>

## <span data-ttu-id="9cf81-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cf81-146">RELATED LINKS</span></span>

[<span data-ttu-id="9cf81-147">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="9cf81-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


