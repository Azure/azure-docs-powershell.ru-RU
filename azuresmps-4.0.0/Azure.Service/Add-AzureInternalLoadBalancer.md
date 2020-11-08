---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075724"
---
# <span data-ttu-id="cf18f-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf18f-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="cf18f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf18f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf18f-103">Добавляет внутренний балансировщик нагрузки в службу Azure.</span><span class="sxs-lookup"><span data-stu-id="cf18f-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="cf18f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf18f-104">SYNTAX</span></span>

### <span data-ttu-id="cf18f-105">ServiceAndSlot (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf18f-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf18f-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="cf18f-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cf18f-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="cf18f-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cf18f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf18f-108">DESCRIPTION</span></span>
<span data-ttu-id="cf18f-109">Командлет **Add-AzureInternalLoadBalancer** добавляет внутреннюю конфигурацию подсистемы балансировки нагрузки в службу Azure.</span><span class="sxs-lookup"><span data-stu-id="cf18f-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="cf18f-110">Для виртуальной сети вы можете указать подсеть или IP-адрес внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cf18f-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="cf18f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf18f-111">EXAMPLES</span></span>

### <span data-ttu-id="cf18f-112">Пример 1: добавление внутренней подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="cf18f-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="cf18f-113">Эта команда добавляет внутренний балансировщик нагрузки с именем ContosoILB в службу с именем ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="cf18f-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="cf18f-114">Пример 2: добавление внутренней подсистемы балансировки нагрузки для указанной подсети</span><span class="sxs-lookup"><span data-stu-id="cf18f-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="cf18f-115">Эта команда добавляет внутренний балансировщик нагрузки с именем ContosoILB в службу с именем ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="cf18f-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="cf18f-116">Команда задает подсеть с именем FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="cf18f-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="cf18f-117">Пример 3: добавление внутренней подсистемы балансировки нагрузки для указанной подсети и адреса</span><span class="sxs-lookup"><span data-stu-id="cf18f-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="cf18f-118">Эта команда добавляет внутренний балансировщик нагрузки с именем ContosoILB в службу с именем ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="cf18f-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="cf18f-119">Команда задает подсеть с именем FrontEndSubnet и статический адрес виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cf18f-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="cf18f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf18f-120">PARAMETERS</span></span>

### <span data-ttu-id="cf18f-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cf18f-121">-InformationAction</span></span>
<span data-ttu-id="cf18f-122">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="cf18f-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cf18f-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cf18f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cf18f-124">Продолжал</span><span class="sxs-lookup"><span data-stu-id="cf18f-124">Continue</span></span>
- <span data-ttu-id="cf18f-125">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="cf18f-125">Ignore</span></span>
- <span data-ttu-id="cf18f-126">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="cf18f-126">Inquire</span></span>
- <span data-ttu-id="cf18f-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cf18f-127">SilentlyContinue</span></span>
- <span data-ttu-id="cf18f-128">Остановить</span><span class="sxs-lookup"><span data-stu-id="cf18f-128">Stop</span></span>
- <span data-ttu-id="cf18f-129">Рвать</span><span class="sxs-lookup"><span data-stu-id="cf18f-129">Suspend</span></span>

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

### <span data-ttu-id="cf18f-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cf18f-130">-InformationVariable</span></span>
<span data-ttu-id="cf18f-131">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="cf18f-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cf18f-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="cf18f-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="cf18f-133">Указывает имя внутренней подсистемы балансировки нагрузки, которую добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cf18f-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cf18f-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="cf18f-134">-Profile</span></span>
<span data-ttu-id="cf18f-135">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cf18f-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cf18f-136">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf18f-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf18f-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cf18f-137">-ServiceName</span></span>
<span data-ttu-id="cf18f-138">Указывает имя службы, к которой этот командлет добавляет внутренний балансировщик нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cf18f-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

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

### <span data-ttu-id="cf18f-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="cf18f-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="cf18f-140">Задает IP-адрес виртуальной сети для внутреннего подсистемы балансировки нагрузки, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cf18f-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cf18f-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="cf18f-141">-SubnetName</span></span>
<span data-ttu-id="cf18f-142">Указывает имя подсети для внутреннего подсистемы балансировки нагрузки, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cf18f-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cf18f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf18f-143">CommonParameters</span></span>
<span data-ttu-id="cf18f-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf18f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf18f-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf18f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf18f-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf18f-146">INPUTS</span></span>

## <span data-ttu-id="cf18f-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf18f-147">OUTPUTS</span></span>

### <span data-ttu-id="cf18f-148">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="cf18f-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="cf18f-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf18f-149">NOTES</span></span>

## <span data-ttu-id="cf18f-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf18f-150">RELATED LINKS</span></span>

[<span data-ttu-id="cf18f-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf18f-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="cf18f-152">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="cf18f-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="cf18f-153">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf18f-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="cf18f-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cf18f-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


