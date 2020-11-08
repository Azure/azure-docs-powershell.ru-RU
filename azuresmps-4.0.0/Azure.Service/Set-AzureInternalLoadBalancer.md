---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075954"
---
# <span data-ttu-id="3d537-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d537-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="3d537-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d537-102">SYNOPSIS</span></span>
<span data-ttu-id="3d537-103">Изменение конфигурации внутренней подсистемы балансировки нагрузки в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="3d537-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="3d537-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d537-104">SYNTAX</span></span>

### <span data-ttu-id="3d537-105">ServiceAndSlot (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d537-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d537-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="3d537-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3d537-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="3d537-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3d537-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d537-108">DESCRIPTION</span></span>
<span data-ttu-id="3d537-109">Командлет **Set-AzureInternalLoadBalancer** изменяет конфигурацию внутренней подсистемы балансировки нагрузки в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="3d537-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="3d537-110">Для виртуальной сети вы можете указать подсеть или IP-адрес внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3d537-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="3d537-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d537-111">EXAMPLES</span></span>

### <span data-ttu-id="3d537-112">1:</span><span class="sxs-lookup"><span data-stu-id="3d537-112">1:</span></span>
```

```

## <span data-ttu-id="3d537-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d537-113">PARAMETERS</span></span>

### <span data-ttu-id="3d537-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3d537-114">-InformationAction</span></span>
<span data-ttu-id="3d537-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="3d537-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3d537-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d537-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d537-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="3d537-117">Continue</span></span>
- <span data-ttu-id="3d537-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="3d537-118">Ignore</span></span>
- <span data-ttu-id="3d537-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="3d537-119">Inquire</span></span>
- <span data-ttu-id="3d537-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3d537-120">SilentlyContinue</span></span>
- <span data-ttu-id="3d537-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="3d537-121">Stop</span></span>
- <span data-ttu-id="3d537-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="3d537-122">Suspend</span></span>

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

### <span data-ttu-id="3d537-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3d537-123">-InformationVariable</span></span>
<span data-ttu-id="3d537-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="3d537-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3d537-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3d537-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="3d537-126">Указывает имя внутренней подсистемы балансировки нагрузки, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d537-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d537-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d537-127">-Profile</span></span>
<span data-ttu-id="3d537-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d537-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d537-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d537-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d537-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3d537-130">-ServiceName</span></span>
<span data-ttu-id="3d537-131">Указывает имя службы, в которой этот командлет изменяет внутренний балансировщик нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3d537-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d537-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="3d537-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="3d537-133">Задает IP-адрес виртуальной сети для внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3d537-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d537-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3d537-134">-SubnetName</span></span>
<span data-ttu-id="3d537-135">Указывает имя подсети для внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3d537-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d537-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d537-136">CommonParameters</span></span>
<span data-ttu-id="3d537-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d537-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d537-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d537-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d537-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d537-139">INPUTS</span></span>

## <span data-ttu-id="3d537-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d537-140">OUTPUTS</span></span>

## <span data-ttu-id="3d537-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d537-141">NOTES</span></span>

## <span data-ttu-id="3d537-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d537-142">RELATED LINKS</span></span>

[<span data-ttu-id="3d537-143">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d537-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="3d537-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d537-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="3d537-145">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="3d537-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="3d537-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d537-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


