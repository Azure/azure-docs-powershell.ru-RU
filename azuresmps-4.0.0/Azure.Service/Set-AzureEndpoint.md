---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076057"
---
# <span data-ttu-id="2d4de-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d4de-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="2d4de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d4de-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4de-103">Изменяет конечную точку, назначенную виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2d4de-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="2d4de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d4de-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2d4de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d4de-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4de-106">Командлет **Set-AzureEndpoint** изменяет конечную точку, назначенную виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4de-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="2d4de-107">Вы можете указать изменения конечной точки, не связанные с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d4de-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="2d4de-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d4de-108">EXAMPLES</span></span>

### <span data-ttu-id="2d4de-109">Пример 1: изменение конечной точки для прослушивания порта</span><span class="sxs-lookup"><span data-stu-id="2d4de-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="2d4de-110">Эта команда извлекает конфигурацию виртуальной машины с именем VirtualMachine01 с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="2d4de-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="2d4de-111">Команда передается текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="2d4de-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2d4de-112">Этот командлет изменяет конечную точку "веб-имя" для прослушивания порта 443.</span><span class="sxs-lookup"><span data-stu-id="2d4de-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="2d4de-113">Команда передает объект виртуальной машины в командлет **Update-AzureVM** , который реализует ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="2d4de-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="2d4de-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d4de-114">PARAMETERS</span></span>

### <span data-ttu-id="2d4de-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="2d4de-115">-ACL</span></span>
<span data-ttu-id="2d4de-116">Задает объект конфигурации списка управления доступом (ACL), к которому применяется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2d4de-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="2d4de-117">-DirectServerReturn</span></span>
<span data-ttu-id="2d4de-118">Указывает, будет ли этот командлет включать прямой возврат сервера.</span><span class="sxs-lookup"><span data-stu-id="2d4de-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="2d4de-119">Укажите $True, которые нужно включить, или $False, чтобы отключить.</span><span class="sxs-lookup"><span data-stu-id="2d4de-119">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2d4de-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2d4de-121">Указывает тайм-аут простоя TCP для конечной точки (в минутах).</span><span class="sxs-lookup"><span data-stu-id="2d4de-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2d4de-122">-InformationAction</span></span>
<span data-ttu-id="2d4de-123">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="2d4de-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2d4de-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2d4de-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d4de-125">Продолжал</span><span class="sxs-lookup"><span data-stu-id="2d4de-125">Continue</span></span>
- <span data-ttu-id="2d4de-126">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="2d4de-126">Ignore</span></span>
- <span data-ttu-id="2d4de-127">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="2d4de-127">Inquire</span></span>
- <span data-ttu-id="2d4de-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2d4de-128">SilentlyContinue</span></span>
- <span data-ttu-id="2d4de-129">Остановить</span><span class="sxs-lookup"><span data-stu-id="2d4de-129">Stop</span></span>
- <span data-ttu-id="2d4de-130">Рвать</span><span class="sxs-lookup"><span data-stu-id="2d4de-130">Suspend</span></span>

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

### <span data-ttu-id="2d4de-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2d4de-131">-InformationVariable</span></span>
<span data-ttu-id="2d4de-132">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="2d4de-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2d4de-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="2d4de-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="2d4de-134">Указывает имя внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d4de-134">Specifies the name of the internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="2d4de-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="2d4de-136">Указывает алгоритм распространения подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d4de-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="2d4de-137">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2d4de-137">Valid values are:</span></span> 

- <span data-ttu-id="2d4de-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="2d4de-138">sourceIP.</span></span>
<span data-ttu-id="2d4de-139">Две сходствы кортежей: исходный IP-адрес, конечный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="2d4de-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="2d4de-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="2d4de-140">sourceIPProtocol.</span></span>
<span data-ttu-id="2d4de-141">Три сходства кортежей: исходный IP-адрес, IP-адрес назначения, протокол</span><span class="sxs-lookup"><span data-stu-id="2d4de-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="2d4de-142">ничего.</span><span class="sxs-lookup"><span data-stu-id="2d4de-142">none.</span></span>
<span data-ttu-id="2d4de-143">Пять сходств кортежей: исходный IP-адрес, порт источника, IP-адрес назначения, порт назначения, протокол</span><span class="sxs-lookup"><span data-stu-id="2d4de-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="2d4de-144">Значение по умолчанию — None (нет).</span><span class="sxs-lookup"><span data-stu-id="2d4de-144">The default value is none.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="2d4de-145">-LocalPort</span></span>
<span data-ttu-id="2d4de-146">Указывает локальный, частный порт, который использует эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2d4de-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="2d4de-147">Приложения на виртуальной машине прослушивают этот порт для запросов на входные данные для этой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d4de-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d4de-148">-Name</span></span>
<span data-ttu-id="2d4de-149">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d4de-149">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="2d4de-150">-Profile</span></span>
<span data-ttu-id="2d4de-151">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2d4de-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2d4de-152">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d4de-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2d4de-153">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="2d4de-153">-Protocol</span></span>
<span data-ttu-id="2d4de-154">Указывает протокол конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d4de-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="2d4de-155">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2d4de-155">Valid values are:</span></span> 

- <span data-ttu-id="2d4de-156">Номера</span><span class="sxs-lookup"><span data-stu-id="2d4de-156">tcp</span></span> 
- <span data-ttu-id="2d4de-157">трафика</span><span class="sxs-lookup"><span data-stu-id="2d4de-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="2d4de-158">-PublicPort</span></span>
<span data-ttu-id="2d4de-159">Указывает открытый порт, который использует конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2d4de-159">Specifies the public port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="2d4de-160">-VirtualIPName</span></span>
<span data-ttu-id="2d4de-161">Указывает имя виртуального IP-адреса, который Azure связывает с конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="2d4de-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="2d4de-162">Ваша служба может иметь несколько виртуальных IP – адресов.</span><span class="sxs-lookup"><span data-stu-id="2d4de-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="2d4de-163">Чтобы создать виртуальные IP-адреса, используйте командлет **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="2d4de-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-164">-VM</span><span class="sxs-lookup"><span data-stu-id="2d4de-164">-VM</span></span>
<span data-ttu-id="2d4de-165">Указывает виртуальную машину, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2d4de-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4de-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4de-166">CommonParameters</span></span>
<span data-ttu-id="2d4de-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d4de-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4de-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4de-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4de-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d4de-169">INPUTS</span></span>

## <span data-ttu-id="2d4de-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d4de-170">OUTPUTS</span></span>

### <span data-ttu-id="2d4de-171">System. Object</span><span class="sxs-lookup"><span data-stu-id="2d4de-171">System.Object</span></span>

## <span data-ttu-id="2d4de-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d4de-172">NOTES</span></span>

## <span data-ttu-id="2d4de-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d4de-173">RELATED LINKS</span></span>

[<span data-ttu-id="2d4de-174">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d4de-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="2d4de-175">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="2d4de-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="2d4de-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d4de-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="2d4de-177">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2d4de-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="2d4de-178">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d4de-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="2d4de-179">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2d4de-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


