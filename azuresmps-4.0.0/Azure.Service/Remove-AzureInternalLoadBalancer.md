---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076475"
---
# <span data-ttu-id="c6094-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6094-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="c6094-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6094-102">SYNOPSIS</span></span>
<span data-ttu-id="c6094-103">Удаляет конфигурацию внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c6094-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="c6094-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6094-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c6094-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6094-105">DESCRIPTION</span></span>
<span data-ttu-id="c6094-106">Командлет **Remove-AzureInternalLoadBalancer** удаляет конфигурацию внутренней подсистемы балансировки нагрузки из службы Azure.</span><span class="sxs-lookup"><span data-stu-id="c6094-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="c6094-107">Если какая – либо конечная точка на данный момент ссылается на внутренний балансировщик нагрузки, этот командлет не может удалить конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="c6094-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="c6094-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6094-108">EXAMPLES</span></span>

### <span data-ttu-id="c6094-109">Пример 1: Удаление конфигурации внутренней подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="c6094-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="c6094-110">Эта команда удаляет конфигурацию внутренней подсистемы балансировки нагрузки для службы с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="c6094-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="c6094-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6094-111">PARAMETERS</span></span>

### <span data-ttu-id="c6094-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c6094-112">-InformationAction</span></span>
<span data-ttu-id="c6094-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c6094-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c6094-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c6094-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6094-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c6094-115">Continue</span></span>
- <span data-ttu-id="c6094-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c6094-116">Ignore</span></span>
- <span data-ttu-id="c6094-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c6094-117">Inquire</span></span>
- <span data-ttu-id="c6094-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c6094-118">SilentlyContinue</span></span>
- <span data-ttu-id="c6094-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="c6094-119">Stop</span></span>
- <span data-ttu-id="c6094-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="c6094-120">Suspend</span></span>

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

### <span data-ttu-id="c6094-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c6094-121">-InformationVariable</span></span>
<span data-ttu-id="c6094-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c6094-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c6094-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="c6094-123">-Profile</span></span>
<span data-ttu-id="c6094-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c6094-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6094-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6094-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6094-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c6094-126">-ServiceName</span></span>
<span data-ttu-id="c6094-127">Указывает имя службы, из которой этот командлет удаляет внутренний балансировщик нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c6094-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

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

### <span data-ttu-id="c6094-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6094-128">CommonParameters</span></span>
<span data-ttu-id="c6094-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6094-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6094-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6094-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6094-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6094-131">INPUTS</span></span>

## <span data-ttu-id="c6094-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6094-132">OUTPUTS</span></span>

### <span data-ttu-id="c6094-133">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="c6094-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="c6094-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6094-134">NOTES</span></span>

## <span data-ttu-id="c6094-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6094-135">RELATED LINKS</span></span>

[<span data-ttu-id="c6094-136">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6094-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="c6094-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6094-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="c6094-138">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="c6094-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="c6094-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6094-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


