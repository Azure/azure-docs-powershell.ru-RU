---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075914"
---
# <span data-ttu-id="20bab-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="20bab-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="20bab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20bab-102">SYNOPSIS</span></span>
<span data-ttu-id="20bab-103">Создание конфигурации внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="20bab-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="20bab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20bab-104">SYNTAX</span></span>

### <span data-ttu-id="20bab-105">ServiceAndSlot (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20bab-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="20bab-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="20bab-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="20bab-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="20bab-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="20bab-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20bab-108">DESCRIPTION</span></span>
<span data-ttu-id="20bab-109">Командлет **New-AzureInternalLoadBalancerConfig** создает объект **InternalLoadBalancerConfig** .</span><span class="sxs-lookup"><span data-stu-id="20bab-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="20bab-110">Вы можете использовать конфигурацию внутренней подсистемы балансировки нагрузки, когда вы создаете развертывание виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="20bab-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="20bab-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20bab-111">EXAMPLES</span></span>

### <span data-ttu-id="20bab-112">Пример 1: создание конфигурации внутренней подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="20bab-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="20bab-113">Эта команда создает внутреннюю конфигурацию подсистемы балансировки нагрузки для подсети с именем FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="20bab-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="20bab-114">Команда хранит конфигурацию в переменной $IlbConfig, которую вы хотите использовать для развертывания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="20bab-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="20bab-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20bab-115">PARAMETERS</span></span>

### <span data-ttu-id="20bab-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="20bab-116">-InformationAction</span></span>
<span data-ttu-id="20bab-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="20bab-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="20bab-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="20bab-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20bab-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="20bab-119">Continue</span></span>
- <span data-ttu-id="20bab-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="20bab-120">Ignore</span></span>
- <span data-ttu-id="20bab-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="20bab-121">Inquire</span></span>
- <span data-ttu-id="20bab-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="20bab-122">SilentlyContinue</span></span>
- <span data-ttu-id="20bab-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="20bab-123">Stop</span></span>
- <span data-ttu-id="20bab-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="20bab-124">Suspend</span></span>

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

### <span data-ttu-id="20bab-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20bab-125">-InformationVariable</span></span>
<span data-ttu-id="20bab-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="20bab-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="20bab-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="20bab-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="20bab-128">Указывает имя внутренней подсистемы балансировки нагрузки, которое этот командлет включает в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="20bab-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="20bab-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="20bab-129">-Profile</span></span>
<span data-ttu-id="20bab-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="20bab-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20bab-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20bab-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20bab-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="20bab-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="20bab-133">Задает IP-адрес виртуальной сети для внутренней подсистемы балансировки нагрузки, которую этот командлет включает в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="20bab-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bab-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="20bab-134">-SubnetName</span></span>
<span data-ttu-id="20bab-135">Указывает имя подсети для внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="20bab-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20bab-136">CommonParameters</span></span>
<span data-ttu-id="20bab-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20bab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20bab-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20bab-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20bab-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20bab-139">INPUTS</span></span>

## <span data-ttu-id="20bab-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20bab-140">OUTPUTS</span></span>

### <span data-ttu-id="20bab-141">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="20bab-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="20bab-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="20bab-142">NOTES</span></span>

## <span data-ttu-id="20bab-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20bab-143">RELATED LINKS</span></span>

[<span data-ttu-id="20bab-144">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20bab-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="20bab-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20bab-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="20bab-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20bab-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="20bab-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20bab-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


