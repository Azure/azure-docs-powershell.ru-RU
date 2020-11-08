---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075800"
---
# <span data-ttu-id="7d4b3-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7d4b3-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="7d4b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4b3-103">Добавляет или изменяет правило сетевой безопасности в группе безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="7d4b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d4b3-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7d4b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d4b3-105">DESCRIPTION</span></span>
<span data-ttu-id="7d4b3-106">Командлет **Set-AzureNetworkSecurityRule** добавляет или изменяет правило сетевой безопасности Azure в сетевой группе безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="7d4b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d4b3-107">EXAMPLES</span></span>

## <span data-ttu-id="7d4b3-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d4b3-108">PARAMETERS</span></span>

### <span data-ttu-id="7d4b3-109">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="7d4b3-109">-Action</span></span>
<span data-ttu-id="7d4b3-110">Задает действие для правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="7d4b3-111">Допустимые значения: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-111">Valid values are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7d4b3-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="7d4b3-113">Указывает IP-адрес (но не классического междоменной маршрутизации (CIDR) для диапазона конечных диапазонов для правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="7d4b3-114">Звездочка (\*) задает IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-114">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="7d4b3-115">-DestinationPortRange</span></span>
<span data-ttu-id="7d4b3-116">Указывает диапазон портов назначения для правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="7d4b3-117">Допустимые значения состоят из целых чисел от 0 до 65535.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="7d4b3-118">Вы можете задать отдельное значение или задать диапазон в формате LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="7d4b3-119">Два значения отделяются дефисом.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-119">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d4b3-120">-Name</span></span>
<span data-ttu-id="7d4b3-121">Указывает имя для правила сетевой безопасности, которое добавляет или изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d4b3-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7d4b3-123">Указывает сетевую группу безопасности, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="7d4b3-124">Чтобы получить объект **INetworkSecurityGroup** , используйте командлет Get-AzureNetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-125">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="7d4b3-125">-Priority</span></span>
<span data-ttu-id="7d4b3-126">Задает приоритет для правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="7d4b3-127">Допустимые значения: целые числа от 100 до 4096.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="7d4b3-128">-Profile</span></span>
<span data-ttu-id="7d4b3-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7d4b3-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d4b3-131">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="7d4b3-131">-Protocol</span></span>
<span data-ttu-id="7d4b3-132">Задает протокол для правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="7d4b3-133">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="7d4b3-133">Valid values are:</span></span> 

- <span data-ttu-id="7d4b3-134">Номера</span><span class="sxs-lookup"><span data-stu-id="7d4b3-134">TCP</span></span> 
- <span data-ttu-id="7d4b3-135">ТРАФИКА</span><span class="sxs-lookup"><span data-stu-id="7d4b3-135">UDP</span></span> 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7d4b3-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="7d4b3-137">Задает адрес CIDR диапазона IP-адресов источника для правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="7d4b3-138">Звездочка (\*) задает IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-138">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="7d4b3-139">-SourcePortRange</span></span>
<span data-ttu-id="7d4b3-140">Указывает диапазон портов источника для правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="7d4b3-141">Допустимые значения состоят из целых чисел от 0 до 65535.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="7d4b3-142">Вы можете задать отдельное значение или задать диапазон в формате LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="7d4b3-143">Два значения отделяются дефисом.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-143">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-144">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="7d4b3-144">-Type</span></span>
<span data-ttu-id="7d4b3-145">Указывает тип подключения для правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="7d4b3-146">Допустимые значения: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-146">Valid values are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4b3-147">CommonParameters</span></span>
<span data-ttu-id="7d4b3-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d4b3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4b3-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d4b3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4b3-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d4b3-150">INPUTS</span></span>

## <span data-ttu-id="7d4b3-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d4b3-151">OUTPUTS</span></span>

## <span data-ttu-id="7d4b3-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d4b3-152">NOTES</span></span>

## <span data-ttu-id="7d4b3-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d4b3-153">RELATED LINKS</span></span>

[<span data-ttu-id="7d4b3-154">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7d4b3-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


